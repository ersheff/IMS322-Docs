# Arrays

In JavaScript, an _array_ is a type of variable used to store sequences of values or a series of objects. Declare an array using square brackets, with items separated by commas.

```js
const quickArray = [12, 34, 56, 78];
```

To access a single value in the array, use bracket notation with the _index_ number, which indicates the item's position within the array, starting at 0. For example, given `quickArray` above:

```js
quickArray[0];
```

would return the first value, `12`.

An array can be populated with other variables.

```js
const x = 10;
const y = 11;
const z = 12;

const coordinates = [x, y, z];
```

When writing objects directly into an array, ensure that square and curly brackets are properly organized.

```js
const classes = [
  {
    courseNo: "IMS322",
    credits: 3
  },
  {
    courseNo: "MUS100Z",
    credits: 1
  }
];
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="PoVMLNe" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLNe">
  Arrays (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
```
