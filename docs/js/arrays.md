# Arrays - XXX

Individual pieces of data can gain more meaning when they are presented in context with other related data. For example, the latitude of the Miami University campus location is **39.511047326918174**. Without the corresponding longitude of **-84.72907894440365**, you might have to traverse the entire planet to find it .

<iframe src="https://www.google.com/maps/embed?pb=!1m17!1m12!1m3!1d3078.15251853712!2d-84.7316538236989!3d39.51104727159965!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m2!1m1!2zMznCsDMwJzM5LjgiTiA4NMKwNDMnNDQuNyJX!5e0!3m2!1sen!2sus!4v1705417684172!5m2!1sen!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

Similarly, if you want to analyze [trends in enrollment at Miami University](https://miamioh.edu/oir/data/factbook/enrollment-undergraduate/index.html), you'll need to look at several years' worth of data in order to get a clear picture.

<img alt="Miami enrollment" src="https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Fa&#47;FactBook-UndergraduateEnrollment&#47;Campus&#47;1_rss.png" width="500px" />

In JavaScript, an _array_ is a type of variable used to store sequences of values. Declare an array using the keyword `const`. The values in the array are surrounded by square brackets and separated by commas.

```js
const myArray = [12, 34, 56, 78];
```

To read out a single value from the array, you refer to it by the _index_, which is the location within the array, starting at 0. For example, given myArray above:

```js
myArray[0];
```

would return the first value: `12`.

**Why `const`?**

Typically, `let` is used to declare variables that can be updated while `const` is for variables that cannot be reassigned.

```js
let x = 10;
x = 11; // This is OK - x is now 11.

const y = 10;
y = 11; // This is not OK - it will throw an error.
```

Many [style guide conventions](https://github.com/airbnb/javascript#references--prefer-const) suggest using `const` whenever possible as it can help prevent bugs and improve code readability. In fact, there have been many instances in previous class examples and projects where `const`could have been used - for example, when assigning a variable to an HTML element using `document.querySelector()`.

```js
const textReadout = document.querySelector("#text-readout");
```

Even when declared using `const`, it is still possible to change the values within an array if needed.

```js
const myArray = [12, 34, 56, 78];
myArray[0] = 99; // This is OK.
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="PoVMLNe" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLNe">
  Arrays (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
