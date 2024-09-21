# Variables

A variable is a named container for data. The name of the variable is up to you (take a look at naming guidelines in the [Style Guide](../../style-guide#naming-conventions)), but ideally, it should be easy to write and remember while also providing context for the data being stored.

To declare a variable, start with the keyword `const` (for values that will not change) or `let` (for values that may change) and assign the value using `=`.

```js
const profName = "Eric"; // will never change
let profCity = "Oxford"; // may change in the future
const x = 2021; // terrible variable name, what is it for?
const year = 2021; // not a great variable name, too generic
const yearHired = 2021; // better variable name
```

_When using the console with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and then clicking the **Console** button in the CodePen editor._

<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="RwvXpWd" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwvXpWd">
  Variables (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
