# Functions

**Functions** are reusable blocks of code designed to perform a specific task or group of related tasks. You can accomplish a lot without writing your own functions, but they can help reduce redundancies and are crucial for some of the workflows in this class.

## Declaring Functions

To use a cooking analogy... think of the function writing process kind of like training a fellow cook on a recipe.

First, you would need to define and teach them the individual steps in the process:

1. Chop stuff.
2. Sauté and simmer.
3. Season to taste.

Then, in the future, you could simply ask: _Can you please make some marinara sauce?_

Start your function declaration with the `function` keyword and a name (using the naming conventions from our [Style Guide](../../style-guide#naming-conventions)), then follow with parentheses and curly braces. The individual steps of your function go inside of the curly braces.

```js
function makeSauce() {
  console.log("Chop stuff");
  console.log("Sauté and simmer");
  console.log("Season to taste");
}
```

Function declarations can go anywhere in your JavaScript, though I recommend putting them at the bottom of your `script.js` file for consistency.

## Calling Functions

Declaring a function does not actually run the code in the function. To execute a function, call it using the function name and parentheses:

```js
makeSauce();
```

_When using the console with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and then clicking the **Console** button in the CodePen editor._

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="oNVvYBv" data-pen-title="Function Declaration (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/oNVvYBv">
  Function Declaration (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
