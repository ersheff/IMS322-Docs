# Data Types

Data stored in [variables](../variables) are always of a certain _type_. When operating on data in JavaScript, results will depend on the types of the operands (the variables on either side of the operator) used in the expression.

Given the prompt "add 40 and 2," the results are predictable because the operands 40 and 2 are both of the type _number_. However, a request to "add 40 and elephant" may not have an obvious response, because... "elephant" is obviously not a number.

While it is important to be aware of these data types, you do not have to specify the type when declaring variables in JavaScript, which is required in some other languages. JavaScript is a _dynamically typed_ language, which means that types are automatically inferred based on the assigned value.

There are 8 different data types in JavaScript:

1. [Number](#number)
2. [String](#string)
3. [Boolean](#boolean)
4. [Object](#object)
5. [Null](#null)
6. [Undefined](#undefined)
7. [BigInt](#bigint)
8. [Symbol](#symbol)

For this class, you will be working directly with the first four - _Number_, _String_, _Boolean_, and _Object_.

You should also know about the _Null_ and _Undefined_ types since they may appear in error messages when troubleshooting.

The _BigInt_ and _Symbol_ types are a bit more esoteric and will likely not be relevant to your work in this class, though they are included below for comprehensiveness.

## Number

```js
const myNumber = 42;
```

## String

A _string_ is a sequence of one or more text characters. When declaring a variable that is intended to be a string, surround the value with double quotes, as seen below.

```js
const myMessage = "Hello, my name is Eric.";
```

## Boolean

The _boolean_ type has only 2 possible values - `true` or `false`. Since these values are not strings, they do not require double quotes around the value.

```js
const isRaining = false;

const isSunny = true;
```

## Object

An _object_ stores collections of data in _key:value_ pairs. Objects can be very complex and powerful, but a very basic example might describe the properties of an item, like a car or laptop. In this case, each _key_ on the left describes the category of the stored _value_ on the right.

```js
const myLaptop = {
  manufacturer: "Apple",
  model: "MacBook Air",
  year: 2020,
  processor: "M1",
  color: "Space Gray"
};
```

Notice the following characteristics that are crucial for declaring objects:

- The key:value pairs are enclosed by curly braces `{}`.
- Each key is named, but they not require double quotes since they are not technically strings.
- The key and value are separated by a colon `:`.
- Each key:value pair is separared by a comma `,`.

You can reference the individual values of an object using _dot notation_.

```js
myLaptop.manufacturer; // returns "Apple"
myLaptop.year; // returns 2020
```

## Null

_Null_ represents an empty or unknown value.

```html
<button id="play-button">Play</button>

<p>Lorem ipsum blah blah blah.</p>
```

```js
const myElement = document.querySelector("#does-not-exist");

console.log(myElement); // logs null
```

## Undefined

_Undefined_ often occurs if a variable is declared but has not been assigned a value.

```js
const myVariable;

console.log(myVariable); // logs "undefined"
```

## BigInt

As the name suggests, the _BigInt_ type is used to store very large integer values. The standard number type is only accurate up to 15 digits, so BigInt is required for larger values. To declare a BigInt, add an `n` to the end of the value.

```js
const largeNumber = 999999999999999; // 15 digits
console.log(largeNumber); // logs 999999999999999

const wrongNumber = 9999999999999999; // 16 digits
console.log(wrongNumber); // logs 10000000000000000, no longer accurate

const bigNumber = 9999999999999999n; // 16 digits with an n at the end declares as BigInt
console.log(bigNumber); // logs 9999999999999999n, which is accurate

console.log(bigNumber + 1); // causes a TypeError since we're trying to add a BigInt and a number

console.log(bigNumber + 1n); // logs 10000000000000000n, which is accurate
```

## Symbol

_Symbols_ are a relatively new primitive data type in JavaScript. Every symbol is unique, even if they are created with the same description.

```js
const symbol1 = Symbol("hello");
const symbol2 = Symbol("hello");
// symbol1 is not equal to symbol2
```

Symbols are often used to prevent clashes between property names (the keys) in objects. They will likely not be useful for your work in this class nor appear in any example code.

## Example Code

Try changing the variable values in the JavaScript below.

_When using the console with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and then clicking the **Console** button in the CodePen editor._

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="poGMYym" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYym">
  Data Types (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
