---
title: 'Working with objects in Javascript'
description: 'if you master objects in Javascript, then you have mastered half of Javascript'
date: '2017-12-30'
tags: ['programming', 'javascript', 'objects']
ShowToc: true
---

Based on experience when I started learning JavaScript, understanding objects is something fundamental. The essence of JavaScript is on the object data type. If we have studied Java or .Net programming, we must be familiar with integer, float, char, and string as primitive data types. In the JavaScript — not only has primitive data types — it also has complex data types, namely object as reference data types.

---

## What is object?

An object is a list of primitive data types (sometimes also reference data types) that store values with the concept of name-value pairs. Each item (which is better known as a variable) is called a property, and a function is called a method.

This is a simple example of an object:

```javascript
var people  = {
  firstName : 'Rizal',
  lastName : 'Asrul Pambudi',
};
```

We already know that objects store data in name-value pairs. Based on the example above, `firstName` and `lastName` including property whose values are `Rizal` and `Asrul Pambudi`.

The property name can be a string or a number, but if the property name is a number, it is accessed in a different way. This is an example.

```javascript
var people = {
  name : 'Rizal Asrul Pambudi',
  93 : 'My weight',
};

console.log(people.93) // This will throw an error
console.log(people['93']) // Correct. This will display 'My weight'

// The best way to avoid number as a property name is using square bracket notation.
```

## Reference and primitive data types

One of the main differences between reference and primitive data types is the value. The value of the reference data type is the address of the variable being filled in, while the value of the primitive data type is the value itself. What does it mean?

Here is the primitive data type.

```javascript
// Primitive data type number is stored as value
var age = 24;
var age2 = age; // age's value stored in age2

age2 = 20; // aUmur's value changed

console.log(age)  // 20
console.log(age2) // 24
```

Let's compare it with the object data type, which is the reference data type.

```javascript
// Reference data type is stored as reference
var laptop = { brand : 'Toshiba' };
var newLaptop = laptop;

laptop.brand = 'HP';

console.log(newLaptop.brand); // HP
console.log(laptop.brand); // HP
```

So, there is a difference in the results, right? That's because the value of `laptop` is stored as a reference and not the value itself. When we change the `laptop` property to `HP`, the `newLaptop` also changes.

## Two common ways to create objects

The most common and easiest way to create objects is to use **the object literal** technique.

```javascript
// This is an empty object initialized using object literal notation
var emptyObject = {};

// This is an object with 4 items using object literal notation too
var banana = {
  color : 'yellow',
  shape : 'long',
  price : 5000,
  flavour : function() { // This is the example of create method in object
    console.log('so sweet!');
  },
};
```

The second way is with **the object constructor** technique. Constructor is a function that is used to initialize a new object, and we use the `new` keyword to use it.

```javascript
// This is an empty object initialized using object constructor notation
var banana = new Object();

// And then we initialize it with 4 items
banana.warna = 'yellow';
banana.bentuk = 'long';
banana.harga = 5000;
banana.flavour = function() {
  console.log('so sweet!');
};
```

## Conclusion

The core of JavaScript — the most used and the most fundamental — data types are objects. One major difference between primitive and reference data types is that the reference data type uses the address as the value of the data, while the primitive data type uses the value itself. There are two general ways to create objects: object literals and constructors.
