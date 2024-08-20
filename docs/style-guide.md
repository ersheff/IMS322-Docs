# Style Guide

The IMS322 Style Guide was designed to help you write well-organized code that is easier to read, edit, and troubleshoot for functional and responsive designs. Although it includes many widely adopted conventions, it is by no means intended to be the universal "best" or "correct" approach. After taking this class, you may consider other styles based on personal preference or professional expectations. However, keep in mind that much of the criteria below directly impacts your assignment grades.

This page is divided into 3 sections:

- **[Autograded Requirements](#autograded-requirements)**: The requirements in this section will be autograded by GitHub Actions during the final sync with your project's repository. You can read more about how to initiate this process and review the results on the [Setup](../setup/#autograding) page.

- **[Manually Graded Requirements](#manually-graded-requirements)**: The requirements in this section will be reviewed by the instructor after submission.

- **[Other Suggestions](#other-suggestions)**: This section includes other miscellaneous style suggestions. Although they do not directly impact your assignment grades, implementing these suggestions will likely help you improve results.

---

## Autograded Requirements

### Default Files

Every assignment should start with the following three files:

- `index.html`
- `style.css`
- `script.js`

These will be provided for you in each assignment template. Do not delete or rename them.

### Separation of Concerns

There are multiple aspects to this concept. Put simply, the goal is to only put HTML, CSS, and JavaScript in their respective files. By keeping these concerns separate, you can work on structure, style, and behavior independently.

These specific items will be checked during the autograding workflow:

- Write all CSS in the `style.css` file, which should be referenced in the `<head>` element using `<link>` tags. Do not write any CSS as inline `style` attributes or in `<style>` tags.
- Write all JavaScript in the `script.js` file, which should be referenced in the `<head>` element using `<script>` tags with the `defer` keyword. Do not write any JavaScript code inside of `<script>` tags.
- On a related note, do not use a `DOMContentLoaded` event listener or `window.onload` property in your JavaScript file. This may cause issues with some projects and is unnecessary if the `defer` keyword is used in the `<script>` tags.
- Run JavaScript functions from event listeners defined in the `script.js` file, not HTML attributes.

_This:_

```js
const counterButton = document.getElementById("counter-button");
myButton.addEventListener("click", addCount);
```

_Not this:_

```html
<button onclick="addCount()">Click Me</button>
```

### Image Compression, Resolution, and Organization

All images used in your projects should be in the WebP format with a maximum resolution of 2200px in either dimension. Use [Squoosh](https://squoosh.app) or another preferred image editing application that can export `.webp` files to prepare your images before adding them to your project.

Store image files in an "images" folder to help keep the file browser organized. Keep in mind, this means that the folder name will need to be part of the path to the file.

_This:_

```html
<img src="images/dog.webp" alt="Dog" />
```

_Not this:_

```html
<img src="dog.webp" alt="Dog" />
```

### CSS Color Syntax

All CSS colors should be in the HEX or RGB format. This will help ensure that you can directly translate colors from your wireframe designs.

- Example HEX code: `#e9967a`
- Example RGB code: `rgb(233, 150, 122)`

There are multiple color utilities to help you choose and convert color codes on the [Utilities](../ref/utilities) page.

### Modern Javascript Variable Declarations

Use the keywords `let` (for values that will change) and `const` (for values that will not change) when declaring variables in JavaScript. Although it is still technically valid, do not use the outdated `var`.

_This:_

```js
let favoriteFruit = "apple";
const birthYear = 1986;
```

_Not this:_

```js
var favoriteFruit = "apple";
var birthYear = 1986;
```

---

## Manually Graded Requirements

### Font Selection and Loading

[Web safe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) are fonts that you can safely assume are already installed on a user's computer:

- Arial (sans-serif)
- Verdana (sans-serif)
- Tahoma (sans-serif)
- Trebuchet MS (sans-serif)
- Times New Roman (serif)
- Georgia (serif)
- Courier New (monospace)
- Brush Script MT (cursive)

If you use any other font in your designs, you must include it as a resource by either adding the font file to the project folder and importing it in CSS, or embedding `<link>` tags from a hosted source in the `<head>` element.

### Naming Conventions

- Rename long or cryptic image files whenever necessary. For example, `dog.webp` is much easier to type and identify than `neom-9E9NsEiUGxg-unsplash.webp`.
- Write concise, searchable, and meaningful names for classes, ids, functions, and variables. Only use common, easy-to-remember abbreviations if a name becomes excessively long.
- Class and id attributes in HTML and CSS should always be named using the "kebab-case" convention in which lowercase words are separated by hyphens.
- Functions and variables in JavaScript should be named using the "camelCase" convention in which each word (except the first) starts with a capital letter (without spaces or hyphens).
- Keep in mind that you may find yourself writing both kebab-case and camelCase in your JavaScript file when assigning HTML elements to variables. This is still valid because the id name was created in the HTML file.

```html
<p class="kebab-case" id="kebab-case">Blah blah blah.</p>
```

```js
const camelCase = "apple";
```

```js
// camelCase variable name, kebab-case id

const counterButton = document.querySelector("#counter-button");
```

### Display Size Targets and General Layout

Your project layouts will need to work at the following window widths (based on [MDN Web Docs recommendations](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries)):

- `480px` (mobile)
- `800px` (tablet, narrow laptop/desktop windows)
- `1100px` (wide laptop/desktop windows)

This means that text content and images are not too small nor overflowing the visible area.

The following CSS has been created for you in the assignment templates to help achieve these general layout requirements:

- By default, the `<body>` element should be centered within the browser window with a maximum width of `1100px`.
- Large paragraphs should not exceed a width of `80ch` to improve readability.
- Elements may need to be rearranged or resized using media queries at `480px` and/or `800px`.

_Default assignment template CSS:_

```css
* {
  box-sizing: border-box;
}

body {
  max-width: 1100px;
  margin: auto;
}

p {
  max-width: 80ch;
}

img {
  width: 100%;
}

@media (max-width: 800px) {
}

@media (max-width: 480px) {
}
```

---

## Other Suggestions

### Formatting

In both CodePen and VS Code, [js-beautify](https://beautifier.io) is used for HTML formatting and [Prettier](https://prettier.io) is used for CSS and JavaScript formatting. Formatting occurs automatically on save if both platforms are configured as described in the [Setup](../setup) guide.

As long as your code is not missing tags or brackets, the following should apply:

- Blank lines and indentation
- Proper spacing around operators, parentheses, and curly brackets
- Semicolons at the end of statements in JavaScript
- Single quotes `'` replaced with double quotes `"` in JavaScript

_HTML_

```html
<body>
  <header>
    <h1>My Big Project</h1>
  </header>

  <main>
    <p>Tons of great content here.</p>
    <img src="headshot.webp" alt="Headshot" />
  </main>

  <footer>
    <p>Like and subscribe!</p>
  </footer>
</body>
```

_CSS_

```css
h1 {
  color: #ff0000;
}

p {
  color: #0000ff;
}
```

_JavaScript_

```js
let favoriteFruit = "apple";

if (favoriteFruit === "apple") {
  declareLove();
}

function declareLove() {
  console.log("I like apples, too!");
}
```

### Relative Units

Try to prioritize relative units in CSS whenever possible to improve responsiveness and consistency in sizing and spacing. Common examples of relative units include:

- `%` - Percentage relative to the parent element.
- `ch` - The width of a character in the element's font size.
- `rem` - Relative to the height of the default browser font size.

When you do use absolute units, like `px`, try to do so in a consistent and logical manner e.g. in multiples of 2 or 10. Adopting CSS variables can help with this since you can create your own definitions for size denominations in one place.

You can read more about all the valid absolute and relative units in this [MDN Web Docs reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages).

### CSS Style Selectors

Use element and class selectors and CSS nesting instead of id selectors in CSS. This can also help reinforce the [separation of concerns](#separation-of-concerns) by reserving id attributes for assigning HTML elements to variables in JavaScript.

```css
/* element selector */
h2 {
  color: #0000ff;
}

/* class selector with nesting */
.warning {
  color: #ff0000;
  font-weight: bold;

  button {
    background-color: #ff9999;
  }
}
```
