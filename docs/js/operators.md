# Operators

In other examples, you have probably already seen two operators that have fairly obvious functions: `+` for addition and `=` for assigning values, as seen in the expression:

```js
let y = x + 10;
```

Many other JavaScript operators are similarly self-explanatory, though there are a few useful ones that may require additional explanation.

## Arithmetic Operators

The standard arithmetic operators are

- Addition `+`
- Subtraction `-`
- Multiplication `*`
- Division `/`

Some other useful arithmetic operators in JavaScript include:

- Modulo `%` (returns the remainder of dividing two numbers)
- Increment `++` (increases avalue by 1)
- Decrement `--` (decreases a value by 1)

```js
const x = 24 % 7; // x is 3
x++; // x is now 4
x--; // x is now 3 again
```

## Assignment Operators

Assignment operators execute an arithmetic operation and assignment in one step.

```js
let x = 7;
x += 3; // x is now 10
```

Other assignment operators include:

- Subtraction assignment `-=`
- Multiplication assignment `*=`
- Division assignment `/=`
- Remainder assignment `%=`

## String Concatenation

When working with strings, `+` is the concatenation operator, joining strings together. String concatenation is useful for inserting variable values into longer messages.

```js
const myName = "Eric";
const welcomeMessage = "Welcome, " + myName + ".";
console.log(welcomeMessage); // logs "Welcome, Eric." to the console
```

_When using the console with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and then clicking the **Console** button in the CodePen editor._

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="RwzgYXB" data-pen-title="Operators 1 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwzgYXB">
  Operators 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br>
<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="WNmeoZX" data-pen-title="Operators 2 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNmeoZX">
  Operators 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
