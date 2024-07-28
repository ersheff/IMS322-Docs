---
title: Conditionals
---

Conditionals give you the ability to make decisions in your code. Perhaps you want to change a visual theme based on the time of day, or display a "Game Over" screen when the player has run out of lives.

## If Statements

With an if statement, you can evaluate whether or not a condition is true and, if so, run a specific section of code.

```js
if (condition) {
  // do this stuff if true
}
```

You can require multiple conditions with `&&` or allow for either/or with `||`.

```js
if (condition1 && condition2) {
  // do this stuff only if both conditions are true
}

if (condition1 || condition2) {
  // do this stuff if either condition1 or condition2 is true
}
```

You can also create multiple branches with `else` or `else if`.

```js
if (condition) {
  // do this stuff if true
} else {
  // do this stuff if not
}

if (condition1) {
  // do this stuff if condition1 is true
} else if (condition2) {
  // do this stuff if condition2 is true
} else {
  // do this stuff if neither condition1 or condition2 is true
}
```

## Comparison Operators

You can specify your conditions for if statements using the following comparison operators.

| Operator                   | Description                                                                       |
| -------------------------- | --------------------------------------------------------------------------------- |
| Strict equal `===`         | Returns `true` if the operands are equal and of the same type.                    |
| Not equal `!=`             | Returns `true` if the operands are not equal.                                     |
| Greater than `>`           | Returns `true` if the left operand is greater than the right operand.             |
| Greater than or equal `>=` | Returns `true` if the left operand is greater than or equal to the right operand. |
| Less than `<`              | Returns `true` if the left operand is less than the right operand.                |
| Less than or equal `<=`    | Returns `true` if the left operand is less than or equal to the right operand.    |

For example, this tests whether or not the variable is greater than 10:

```js
let x = 11;

if (x > 10) {
  console.log("You win!");
}
```

This checks to see whether the string variable is exactly "Eric":

```js
let myName = "Eric";

if (myName === "Eric") {
  console.log("Hey, that is my name, too!");
}
```

Try changing the comparison operators and operands of the conditionals in the `script.js` below and see if the result matches your expectations.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="rNPXRMV" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/rNPXRMV">
  Conditionals (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
