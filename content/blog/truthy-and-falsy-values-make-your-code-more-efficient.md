---
title: 'Truthy and false values: make your code more efficient'
date: '2018-08-18'
tags: ['programming', 'javascript', 'truthy', 'falsy']
ShowToc: true
---

I decided to write about truthy and false values as the topic this time, after yesterday there was a long pause. I took this topic because I was greatly helped by truthy and false values, especially in terms of the efficiency of writing lines of code.

---

## What are truthy and falsy values?

The developers who have been using javascript for a long time will be familiar with the terms *truthy* and *falsy*. But for those new to javascript, myself included, the term can be a little confusing.

If we say that a value is truthy, it does not mean that the value is true. Rather, what it means is that the value is forced to be true when evaluated in a boolean context.

To make it easy to understand, let's look at the code below.

```javascript
function logTruthiness(val) {
  if (val) {
    console.log('Truthy!');
  }
  else {
    console.log('Falsy!');
  }
}
```

The function above takes a `val` parameter and evaluates it into a boolean context (see the `if` condition statement). To prove whether a value is truthy or false, we will fill the `val` parameter not only with boolean values (true and false).

```javascript
// Output: 'Truthy!'
logTruthiness(true);

// Output: 'Truthy!'
logTruthiness({});

// Output: 'Truthy!'
logTruthiness([]);

// Output: 'Truthy!'
logTruthiness('sebuah string');

// Output: 'Truthy!'
logTruthiness(3.14);

// Output: 'Truthy!'
logTruthiness(new Date());
```

Have you tried the codes above? How is the result? Yes, the result is `Truthy!`. In other words, the value of the parameter we enter will be executed in the `if` block, where the parameter is read (as if) as `true`. From this experiment, the values that we use as parameters are truthy values.

Then what about false values? Let's do another experiment.

```javascript
// Output: 'Falsy!'
logTruthiness(false);

// Output: 'Falsy!'
logTruthiness(null);

// Output: 'Falsy!'
logTruthiness(undefined);

// Output: 'Falsy!'
logTruthiness(NaN);

// Output: 'Falsy!'
logTruthiness(0);

// Output: 'Falsy!'
logTruthiness('');
```

If we execute the code above, the resulting output is `Falsy!`. In other words, the value we pass as a parameter will be executed in the `else` block, where the parameter is (as it were) read as `false`. From the experiment earlier, the value of these parameters can be said to be false values.

As the title of this article suggests, truthy and false values can make your coding more efficient. Because we can use it to reduce the use of conditional statements (`if`, `else-if`, `else`) and replace them with logical expressions (`||`, `&&`). But before that, let's refresh our memory about short-circuit evaluation.

## Short-circuit Evaluation

A logical expression is always read from left to right. Every time it reads, logical expressions are always tested whether they can be short-circuited or not, using the following rules:

* `false && (anything)` will evaluate to false.
* `true || (anything)` will evaluate to true.

The meaning of the above rule is that when a logical expression `&&` and the value on the left is `false`, then the result of the logical expression is directly `false` and the block (anything) will not be executed. The same applies to logical expressions `||`.

After we understand about how short circuit evaluation works, the next question is: how can truthy and falsy values make our code cleaner and more efficient? Here's how.

Go straight to the case study below.

```javascript
function setErrorMessage(error) {
  if (error) { 
    return error;
  } else {
    return '-';
  }
}
```

The code above is intended to create a function to display an error message thrown from the function's parameters. The condition is that when the `error` has a value (in this case a string value), the function will return the value of the error. But if the error is an empty string, then the return value of the function is a dash character.

With the help of truthy and false values, the code will become this concise.

```javascript
function setErrorMessage(error) {
  return error || '-';
}
```

See how they differ? Significant enough right? By utilizing logical expressions with short-circuit evaluation properties, we can make the inverse of the function above as if it is truthy or falsy.

## Logical AND (`&&`)

To help understand, the code below is an example of using logical AND in relation to truthy and falsy values.

```javascript
a1 = true  && true       // t && t returns true
a2 = true  && false      // t && f returns false
a3 = false && true       // f && t returns false
a4 = false && (3 == 4)   // f && f returns false
a5 = 'Cat' && 'Dog'      // t && t returns "Dog"
a6 = false && 'Cat'      // f && t returns false
a7 = 'Cat' && false      // t && f returns false
a8 = ''    && false      // f && f returns ""
a9 = false && ''         // f && f returns false
```

## Logical OR (`||`)

```javascript
o1 = true  || true       // t || t returns true
o2 = false || true       // f || t returns true
o3 = true  || false      // t || f returns true
o4 = false || (3 == 4)   // f || f returns false
o5 = 'Cat' || 'Dog'      // t || t returns "Cat"
o6 = false || 'Cat'      // f || t returns "Cat"
o7 = 'Cat' || false      // t || f returns "Cat"
o8 = ''    || false      // f || f returns false
o9 = false || ''         // f || f returns ""
```
