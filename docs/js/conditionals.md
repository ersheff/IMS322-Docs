# Conditionals

Conditionals (aka "if statements") allow you to make decisions in your code. With an `if` statement, you can evaluate whether a condition is true and, if so, run a specific section of code.

```js
if (condition) {
  // do this stuff if the condition is true
}
```

You can require multiple conditions using `&&` (and) or allow for either/or scenarios with `||` (or).

```js
if (condition1 && condition2) {
  // do this stuff only if BOTH conditions are true
}

if (condition1 || condition2) {
  // do this stuff if EITHER condition1 OR condition2 is true
}
```

You can also create multiple branches using `else` or `else if`.

```js
if (condition1) {
  // do this stuff if condition1 is true
} else if (condition2) {
  // do this stuff if condition2 is true
} else {
  // do this stuff if neither condition1 nor condition2 is true
}
```

## Comparison Operators

You can specify conditions in `if` statements using the following comparison operators:

- Strict equal `===`
- Not equal `!=`
- Greater than `>`
- Greater than or equal `>=`
- Less than `<`
- Less than or equal `<=`

For example, this tests whether the variable `x` is greater than 10:

```js
const x = 11;

if (x > 10) {
  console.log("You win!");
}
```

This checks if the string variable exactly matches "Eric":

```js
const myName = "Eric";

if (myName === "Eric") {
  console.log("Hey, that is my name, too!");
}
```

Try changing the comparison operators and operands in the examples below to see if the results match your expectations.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="rNPXRMV" data-pen-title="Conditionals 1 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/rNPXRMV">
  Conditionals 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br>
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="xxvqEXe" data-pen-title="Conditionals 2 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/xxvqEXe">
  Conditionals 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
