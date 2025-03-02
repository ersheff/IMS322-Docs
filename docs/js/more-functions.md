# More Functions

Functions become much more powerful and flexible when they are designed to take input data or return soume output data.

## Parameters

Here is a function that doubles a value and logs it to the console:

```js
function doubleValue() {
  const x = 10;
  console.log(x * 2);
}
```

You can probably guess that calling `doubleValue()` will log `20` to the console. However, this function is very limited because it always doubles the hard-coded number `10`.

To make it more flexible, we will include a parameter in its definition. Then, when the new function is called, a value can be passed as an argument and used as a local variable inside the function. In the example below, `x` is the parameter.

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="vEYxYba" data-pen-title="Function Parameters (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vEYxYba">
  Function Parameters (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Returning Values

The `doubleValue()` function would be much more useful if we could use the result elsewhere in the code instead of just logging it to the console. This can be accomplished using the `return` keyword. The returned value can then be assigned to a variable and used outside of the function.

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="bNGqGZP" data-pen-title="Function Return (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/bNGqGZP">
  Function Parameters (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Here is a more sophisticated example with two functions: one that converts Fahrenheit to Celsius and another that does the reverse.

<p class="codepen" data-height="420" data-default-tab="js" data-slug-hash="xbxqxeL" data-pen-title="Function Return (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 420px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/xbxqxeL">
  Function Return Temperature (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<script async src="https://public.codepenassets.com/embed/index.js"></script>
