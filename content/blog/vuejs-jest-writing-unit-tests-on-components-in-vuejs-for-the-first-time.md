---
title: 'VueJS + Jest. Write unit tests on components in the VueJS for the first time'
date: '2019-06-25'
tags: ['programming', 'javascript', 'unit test', 'jest', 'vuejs']
ShowToc: true
---

In my office, the engineers are being encouraged to write a unit test of the code they are writing. As a software engineer, this is my first experience to write unit tests in the components that I create. I will share a little about how I make unit tests in the Vue component.

I use Jest as a framework to write unit tests in Vue components. Besides that, I also use [vue-test-utils](https://github.com/vuejs/vue-test-utils) as a testing library.

A little information, I use Jest because I think it has some interesting features, such as:

* (Almost) no configuration.
* Can run tests in parallel.
* Have code coverage.
* Testing snapshots.
* Module mocking utilities.

And of course the main reason I use Jest is because almost all the frontend engineers in the office also use it.

But if you want to use other tools, I can recommend using [karma](https://karma-runner.github.io/latest/index.html), [mocha](https://mochajs.org/), or [chai](https://www.chaijs.com/).

---

## Set up a vue-test sample project

Let's start by creating a simple project using vue-cli and answer NO to each question.

```sh
npm install -g vue-cli
vue init webpack vue-test
cd vue-test
```

Then we need to install some dependencies:

```sh
# Install dependencies
npm i -D jest vue-jest babel-jest
```

The `jest-vue-preprocessor` is used to let Jest know about `.vue` files, and `babel-jest` is used for integration with Babel.

Then, install `vue-test-utils`.

```sh
npm i -D vue-test-utils
```

After that, you can add standard configuration in `package.json`.

```json
...
...
"jest": {
  "moduleNameMapper": {
    "^vue$": "vue/dist/vue.common.js"
  },
  "moduleFileExtensions": [
    "js",
    "vue"
  ],
  "transform": {
    "^.+\\.js$": "<rootDir>/node_modules/babel-jest",
    ".*\\.(vue)$": "<rootDir>/node_modules/vue-jest"
  }
}
...
...
```

The `moduleFileExtensions` will tell Jest which extension to look for, and change the preprocessor to use for that file extension.

Final configuration, add `test` script to `package.json`.

```json
{
  "scripts": {
    "test": "jest",
    ...
  },
  ...
}
```

## Testing a component

Assume we create a simple component `NegoButton.vue` in the `src/components` directory:

```vue
<template>
  <button
    :disabled="idDisabled"
    :class="{'is-active': isTransacting}"
    class="c-btn c-btn--block c-btn--red c-btn--large c-btn--spinner"
    style="height: 58px;"
    @click.prevent="pay">
    <i class="c-btn--spinner__icon"></i>
    <span class="c-btn--spinner__text u-txt--fair">Yuk Nego</span>
  </button>
</template>

<script>
export default {
  name: 'NegoButton',
  props: {
    idDisabled: {
      type: Boolean,
      default: false,
    },
    isTransacting: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    pay() {
      /* do a logic bidding */
    },
  },
};
</script>
```

Then, we will create unit tests for that component. For the location of the unit test file, there will be various versions. There are those whose unit test files are placed at the same level as the component files. There are also those who create a `tests` folder in the root directory and put all the unit test files there. But in post, I will put the unit test file in the test folder, which I put at the level of the component. You can refer to [this article](https://medium.com/@JeffLombardJr/organizing-tests-in-jest-17fc431ff850) to add references.

Create a unit test file `NegoButton.spec.js` which is placed in `src/components/test`.

```javascript
import MainComponent from '../NegoButton';

describe('NegoButton.vue', () => {
  it('should have "NegoButton" as name', () => {
    expect(MainComponent.name).toBe('NegoButton');
  });
});
```

Currently, if we run `npm run test` (or `yarn test` for yarn users), our unit test should run and pass our scenario.

The `describe()` and `it()` functions are built-in functions in Jest. The `describe()` is used to create blocks that group together several related test scenarios. Whereas `it()` is the test scenario we want to test. You can check [here](https://jestjs.io/docs/en/api) for more details.

When writing unit tests, we need to check if the values being tested meet certain conditions. The `expect()` function provides access to a number of matchers functions that allow us to validate things. In the example above, we use `toBe()` as the matcher function. You can check the complete API [here](https://jestjs.io/docs/en/expect.html).

## Testing a component with `vue-test-utils`

One of the highlights of this library is **shallow rendering**. Shallow rendering is a technique that ensures our components are rendered without child components. This is useful for:

* Test only the components you want to test.
* Avoiding the side effects of child components, such as HTTP calls, calling the store, etc.

From the previous unit test code, we will do a snapshot test with the help of shallow rendering.

```javascript
import { shallowMount } from '@vue/test-utils';
import MainComponent from '../NegoButton';

describe('NegoButton.vue', () => {
  it('should have "NegoButton" as name', () => {
    expect(MainComponent.name).toBe('NegoButton');
  });

  it('should render correctly', () => {    
    const wrapper = shallowMount(MainComponent);
    expect(wrapper.element).toMatchSnapshot();
  });
});
```

Snapshot tests are very useful for UI tests of components based on the component's HTML syntax. If the UI of our component changes, the test case will fail. But if there is an intentional UI change, we can run the test with the command `npm run test -u` or `yarn test -u`.

In the unit test code, several checks can also be included, such as whether the button from the `NegoButton.vue` component is running properly, or whether the button when it is still disabled cannot be clicked.
