---
title: Data Types
---

Values stored in [variables](variables) are always of a certain _type_. Being aware of these types is important when developing your code as they determine what you can do with that data.

If you were prompted to "add 40 and 2 in your head," you could easily do so because 40 and 2 are both of the type "number." However, a request to "add 40 and elephant" does not have an obvious response. Outside of creative nonsense answers - "uhh... fortyphant?" - it doesn't make any sense.

In JavaScript, if you try to manipulate data in a way that is expected _given the types_ (e.g. add two numbers together), you should get a logical response. If you try to manipulate data in ways that are not expected _given the types_ (e.g. add numbers to words), then you will either receive an unexpected answer or an error.

While you need to be aware of data types, you don't have to specify type when declaring variables. JavaScript is a "dynamically typed" language, which means that types are automatically assigned when code is run based on the how the value was assigned.

There are 8 different data types in JavaScript:

1. Number
2. BigInt
3. String
4. Boolean
5. Null
6. Undefined
7. Symbol
8. Object

For this class, you will be working directly with the Number, String, Boolean, and Object types. You should also know about the Null and Undefined types since they may appear when troubleshooting. The BigInt and Symbol types are a bit more esoteric and will likely not be relevant to your work in this class, though they are included below for comprehensiveness.

## Number

```js
let myNumber = 42;
```

## BigInt

As the name suggests, the BigInt type is used to store very large integer values.
Accurate up to 15 digits. Change to BigInt using n.

```js
let largeNumber = 999999999999999; // 15 digits
console.log(largeNumber); // logs 999999999999999

let wrongNumber = 9999999999999999; // 16 digits
console.log(wrongNumber); // logs 10000000000000000, no longer accurate

let bigNumber = 9999999999999999n; // 16 digits with an n which sets type as BigInt
console.log(bigNumber); // logs 9999999999999999n

console.log(bigNumber + 1); // causes a TypeError since we're trying to add a BigInt and a number

console.log(bigNumber + 1n); // logs 10000000000000000n
```

## String

A _string_ is a sequence of one or more text characters. When declaring a variable that is intended to be a string, surround the value with single quotes, as seen below.

```js
let myMessage = "Hello, my name is Eric.";
```

## Boolean

The _boolean_ type has only 2 possible values - `true` or `false`. Since these are not strings, they do not require single quotes around the value.

```js
let isRaining = false;

let isSunny = true;
```

Try changing the variable values in the JavaScript below - remember, you'll need to open the console in order to see the results.

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="poGMYym" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYym">
  Data Types (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Null

_Null_ represents an empty or unknown value.

```js
let myElement = document.querySelector("#does-not-exist");

console.log(myElement); // logs null
```

## Undefined

_Undefined_ often occurs if a variable is declared but has not been assigned a value.

```js
let myVariable;

console.log(myVariable); // logs "undefined"
```

## Symbol

## Object

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
