# Style Guide - XXX

Automatic checks:
File names - index.html, style.css, script.js
No CSS or JavaScript in the HTML file
Kebab-case in HTML and CSS
Script tags in head with defer keyword
JavaScript functions run from event listeners, not HTML attributes
CSS colors in HEX or rgb
Variable declarations with let and const, not var
No DOMContentLoaded or window.onload events
Image files in webp format
Image files in images folder
Image files are not larger than 2200px

Manual checks:
Image file names are apporpriate
Font is loaded correctly
Layout works at 480px, 800px, and 1100px window widths
Body is centered within the window and limited to 1100px width

Many companies, large and small (e.g. Google, Airbnb, and more), adopt style guides to ensure that everyone creates similar well-organized code and aesthetically consistent designs.

The **IMS322 Style Guide** has been assembled from excerpts from reputable sources and observations of best practices. Although it includes many widely adopted conventions, it is by no means intended to be the "best" or "correct" approach — after taking this class, you might consider other coding styles based on personal or professional preference.

This guide is divided into 2 sections:

- **[Expectations](#expectations)**: These are the "specifications" for all content produced in IMS322 - how to organize files, which file types and formats to use, layout requirements, etc. The conditions in this section will be referenced while reviewing submissions and have a direct impact on your grade.
- **[Formatting](#formatting)**: These are the guidelines for how your code should look in terms of spacing and indentation. While you should review this information, for the most part, formatting is done automatically in CodePen and VS Code.

---

## Expectations

### General

#### **Default filenames**

- `index.html`
- `style.css`
- `script.js`

#### **Separation of concerns**

Do not enter any CSS in `<style>` tags or JavaScript in `<script>` tags in your HTML file. Reference files as needed in the `<head>` and write all CSS in the `style.css` file and JavaScript in the `script.js` file.

#### **Fonts**

Choose only from the following [web safe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) or a selection from [Google Fonts](https://fonts.google.com/) :

- Arial (sans-serif)
- Verdana (sans-serif)
- Tahoma (sans-serif)
- Trebuchet MS (sans-serif)
- Times New Roman (serif)
- Georgia (serif)
- Courier New (monospace)
- Brush Script MT (cursive)

The web safe fonts listed above should already be installed on your computer, but you may need to download and install fonts from Google Fonts to use in your wireframing application. Always include [fallback fonts](https://www.w3schools.com/cssref/css_fonts_fallbacks.php) in your CSS.

#### **Image names, compression, and organization**

Rename long or cryptic image files whenever necessary. For example, `dog.webp` is much easier to type and identify than `neom-9E9NsEiUGxg-unsplash.webp`.

All images used in your projects should be in the "WebP" format.

When working with multiple image files, put them all in an "images" folder to help keep the file browser organized. Keep in mind, this means that the `src` attribute of your `<img>` elements will needs to include the folder as part of the file name e.g. `images/dog.webp`.

#### **Naming conventions**

Write concise, searchable, and meaningful names. Only use common, easy-to-remember abbreviations if a name becomes excessively long.

Class and ID attributes should always be written using the the "kebab-case" convention in which lowercase words are separated by hyphens.

```html
<p class="kebab-case" id="kebab-case">Blah blah blah.</p>
```

Variables and functions should be written using the "camelCase" convention in which each word (except the first) starts with a capital letter (without spaces or hyphens).

```js
const favoriteFruit = "apple";
```

### CSS

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

#### **Media queries and display size targets**

Your project layouts will need to work at the following window widths (based on [MDN Web Docs recommendations](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries)):

- `480px` (mobile)
- `800px` (tablet, narrow laptop/desktop windows)
- `1100px` (wide laptop/desktop windows)

Content in the `<body>` should not exceed the `1100px` maximum width, though background color extending outside that area is acceptable. Media queries for `480px` and `800px` widths will be pre-configured for you in every project's `style.css` file to use as needed.

#### **Center your content area**

All content should be constrained to one main column centered within the browser window. This can be accomplished by styling the `<body>` as a flexbox column or styling the primary content areas like `<header>` and `<main>` as flexbox columns.

##### This:

<div style="display: flex; justify-content: center;">
  <figure style="max-width: 500px;">
	  <img src="images/centered.webp" style="width: 100%;">
  </figure>
</div>
##### Not this:
<div style="display: flex; justify-content: center;">
  <figure style="max-width: 500px;">
	  <img src="images/not-centered.webp" style="width: 100%;">
  </figure>
</div>

#### **Do not use _margin_**

The `margin` property affects content _outside_ the element on which it is applied, which [can cause problems in component-based layouts](https://youtu.be/KVQMoEFUee8?si=Ak_jRbCx06SrTCgH). Use `padding`, flexbox `justify-content` and/or `gap`, or [padding elements](https://youtu.be/KVQMoEFUee8?si=rme5Z9FIMF6Rvpwo&t=467) to add space or adjust alignment in your layouts.

#### **Use relative units by default**

Recommended relative units:

- `%` - Percentage relative to the parent element.
- `ch` - The width of the number "0" of the element's font.
- `rem` - Relative to the default browser font size.

In some cases, you may still find that the absolute unit `px` is the best fit. Some examples:

- If you want to ensure that a small image in a flexible container never stretches beyond its original resolution, set a `max-width` property in `px`.
- If you want to have specific control over the roundness of box corners, set `border-radius` in `px`.

You can read more about all the valid absolute and relative units in this [MDN Web Docs reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages).

#### **Only use HEX or RGB color syntax**

This will help ensure consistency with your wireframe application colors.

- Example HEX code: `#E9967A`
- Example RGB code: `rgb(233, 150, 122)`

There are multiple color helpers on the [Utilities](utilities) page.

#### **Do not style with ID selectors**

Use element and class selectors and CSS nesting to avoid using ID selectors in CSS.

##### This:

```css
h2 {
  color: #0000ff;
}

.warning {
  color: #ff0000;
  font-weight: bold;

  button {
    background-color: #ff9999;
  }
}
```

##### Not this:

```css
#warning {
  color: #ff0000;
  font-weight: bold;
}
```

### JavaScript

#### **Loading JavaScript files**

Always put your `<script>` tags in the `<head>` element with the added `defer` keyword (not required when working in CodePen).

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="style.css" />
  <script src="script.js" defer></script>
  <title>IMS322</title>
</head>
```

#### **Declare variables with _let_ or _const_, not _var_**

Use the keywords `let` (for values that will change) and `const` (for values that will not change) when declaring variables. Although it is still technically valid, do not use the outdated `var`.

```js
let favoriteFruit = "apple";
const birthYear = 1986;
```

#### **Always use === instead of == in _if_ statements**

```js
if (name === "John") {
  // stuff
}
```

---

## Formatting

In both CodePen and VS Code, [js-beautify](https://beautifier.io) is used for HTML formatting and [Prettier](https://prettier.io) is used for CSS and JavaScript formatting.

To automatically format code in CodePen, go to the Editor Preferences in your account settings and check the "Format on Save" option under Editor Options. You can also manually format from the menu in each editor.

The IMS322 VS Code profile that has been provided for you has "Format on Save" enabled by default. You can also manually format by right-clicking in any HTML, CSS, or JavaScript file and choosing "Format Document."

As long as your code is well-formed (i.e. not missing tags or brackets), all of the guidelines described below will be applied for you when using the built-in formatting tools in CodePen and VS Code.

### General Code Organization

Organize HTML, CSS, and JavaScript with blank lines and indentations.

##### This:

```html
<body>
  <header>
    <h1>My Big Project</h1>
  </header>

  <main>
    <p>Tons of great content here.</p>
  </main>

  <footer>
    <p>Like and subscribe!</p>
  </footer>
</body>
```

```css
h2 {
  font-size: 2.4rem;
}

h3 {
  text-shadow: 1px 1px 2px red;
  font-size: 2rem;
}
```

```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}

function declareLove() {
  console.log("I love everything!");
}
```

##### Not this:

```html
<body>
  <header>
    <h1>My Big Project</h1>
  </header>
  <main>
    <p>Tons of great content here.</p>
  </main>
  <footer>
    <p>Like and subscribe!</p>
  </footer>
</body>
```

```css
h2 {
  font-size: 2.4rem;
}
h3 {
  text-shadow: 1px 1px 2px red;
  font-size: 2rem;
}
```

```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}
function declareLove() {
  console.log("I love everything!");
}
```

### HTML

#### **Do not use spaces around equals signs for attributes**

```html
<img src="headshot.webp" alt="Headshot" />
```

### JavaScript

#### **Use semicolons at the end of every statement**

```js
let favoriteFruit = "apple";
```

#### **Use double quotes for strings**

```js
console.log("hello");
```

#### **Add a space around operators and equals signs**

```js
const exampleOperation = exampleNumber * 2;
```

#### **Do not use extra spaces inside parentheses**

```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}
```

#### **Curly brace spacing**

When using curly braces (e.g. in `if` statements and `function` declarations), the opening brace should be on the same line as the corresponding keyword. There should also be a space before the opening bracket.

```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}

function declareLove() {
  console.log("I love everything!");
}
```
