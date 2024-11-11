# For Loops

For loops are used to execute a block of code a specified number of times. They are structured using 3 expressions:

```js
for (expression 1; expression 2; expression 3) {
  // code block to be executed
}
```

1. Expression 1 is executed once before code block in the curly brackets runs. Typically, this is used to initialize a counter variable, usually named `i`, and set to `0`.
2. Expression 2 defines the condition for running the code block. Essentially, it determines the how many times the code block will execute.
3. Expression 3 runs after each execution of the code block, typically written as `i++` to increment the counter variable.

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="OJGwpoJ" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/OJGwpoJ">
  For Loops (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

The counter variable can be used in arithmetic expressions like any other number.

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="eYojvPG" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/eYojvPG">
  For Loops Accumulator (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

The counter variable can be also be used as an index number to lookup each value in an array.

<p class="codepen" data-height="400" data-default-tab="js" data-slug-hash="KKYBWxN" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKYBWxN">
  For Loops and Arrays (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

# For Of Loops

Arrays are an example of something that is _iterable_, meaning that we can loop over each value (iterate) using a special `for...of` loop.

```js
for (const variable of iterable) {
  // do something multiple time, once for each value in the sequence
}
```

In this structure, the placeholder `iterable` is replaced by the source of the sequence (the name of the array). The placeholder `variable` becomes a temporary variable within the loop, holding a new value from the sequence in each iteration.

To clarify, let's go through an example:

```js
const quickArray = [12, 34, 56, 78];

for (const q of myArray) {
  console.log(q);
}
```

Here, `quickArray` is the source. The `for of` loop runs four times because there are four values in `quickArray`. Each time the loop runs, `q` represents each successive value in the array, starting at `12`, then `34`, then `56`, and so on.

Why did we call the temporary variable `q`? Any name is valid, though it is common to see the first letter of the array name used as the temporary variable. Or, in the case of an array with a plural variable name, the singular form may be used as the name for the temporary variable.

```js
const months = [
  "January",
  "February",
  "March",
  "April",
  "May",
  "June",
  "July",
  "August",
  "September",
  "October",
  "November",
  "December"
];

for (const month of months) {
  console.log(month);
}
```

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="poYzNNa" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poYzNNa">
  For Of Loops (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
