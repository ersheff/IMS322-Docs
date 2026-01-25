# Coding Style & Requirements

This guide was designed to help you write well-organized code that is easier to read, edit, and troubleshoot for functional and responsive designs. Although it includes many widely adopted conventions, it is by no means intended to be the universal "best" or "correct" approach. After taking this class, you may consider other styles based on personal preference or professional expectations. However, keep in mind that much of the criteria below directly impacts your project grades.

This page is divided into two sections:

- **[General Requirements](#general-requirements)**: These requirements apply to all projects and will be assessed by the instructor according to the associated rubric in Canvas. They will be provided in every project description, as well.

- **[Suggestions](#suggestions)**: This section includes other miscellaneous suggestions. While they do not directly affect your assignment grades, implementing these suggestions may help improve your results.

---

## General Requirements

**All projects are expected to meet the following criteria.**

### Naming Conventions

- Name `class` and `id` attributes in HTML and CSS using the "kebab-case" convention, where lowercase words are separated by hyphens.
- Name `functions` and `variables` in JavaScript using the "camelCase" convention, where each word (except the first) begins with a capital letter and contains no spaces or hyphens.
- Do not use spaces or special characters in file names other than hyphens `-` or underscores `_`. Rename long or cryptic file names as needed. For example, `dog.jpeg`, not `neom-9E9NsEiUGxg-unsplash.jpeg`.

```html
<p class="kebab-case">Blah blah blah.</p>
```

```js
const camelCase = 'apple';
```

### Files and Images

- Each project submission must include at minimum an `index.html`, `style.css`, and `main.js` file. These are provided in the template repository, so do not delete or rename them.
- All images must be in `jpeg` or `webp` format with a resolution no larger than `3840` pixels in width or `2160` pixels in height. Logos, icons, or other vector drawings may be in `svg` format. Use [Squoosh](https://squoosh.app/) or another image editor to resize or compress images before adding them to your project.
- All image files must be stored inside an `images` folder.

_This:_

```html
<img src="images/dog.webp" alt="Dog" />
```

_Not this:_

```html
<img src="dog.webp" alt="Dog" />
```

### Comments

- Use comments to explain and organize your code. At a minimum, comments should be used to separate code into logical sections.

### HTML

- Do not change the provided `<link>` or `<script>` tags in the `<head>` of `index.html`. These are already configured to correctly load `style.css` and `main.js`. You may add additional `<link>` or `<script>` tags in the `<head>` if needed (e.g., to load external fonts).
- Do not write any styling or scripting in your HTML. This includes:
  - Inline `style` or event attributes (such as `onclick`)
  - `<style>` tags
  - `<script>` tags outside of the `<head>`
  - `<script>` tags that do not reference a `src` file

_This:_

```css
button {
  color: #ff0000;
}
```

```js
const counterButton = document.getElementById('counter-button');
counterButton.addEventListener('click', addCount);
```

_Not this:_

```html
<button style="color: #ff0000;" onclick="addCount()">Click Me</button>
```

### CSS

- All colors should use HEX or RGB values taken directly from wireframe designs. Minor variations are acceptable.
  - Example HEX code: `#e9967a`
  - Example RGB code: `rgb(233, 150, 122)`
- Always specify font families. If you are not using a "[web safe font](https://fonts.google.com/knowledge/glossary/system_font_web_safe_font)," make sure the font is properly loaded in your project. If you are using a single font family for all elements, apply it globally in the `main` selector.
- Layouts should adapt to any window width from `320px` and above. A default media query breakpoint at `640px` is provided in `style.css` to make size and layout adjustments as needed for wider windows.

### JavaScript

- Use the keywords `let` or `const` when declaring variables in JavaScript. Do not use `var`.
- Do not use a `DOMContentLoaded` event listener or `window.onload` property. Many online examples may suggest these, but they are unnecessary and may cause conflicts in later projects.
- Do not use the ternary `?` operator for conditionals. This is often suggested in AI-generated code. Use `if` statements instead.

_This:_

```js
let message = '';
const birthYear = 1981;

if (birthYear < 2000) {
  message = 'No spring chicken!';
}
```

_Not this:_

```js
var favoriteFruit = 'apple';
var birthYear = 1981;
message = birthYear < 2000 ? 'No spring chicken!' : '';
```

---

## Suggestions

### Formatting

In both CodePen and VS Code, [js-beautify](https://beautifier.io) is used for HTML formatting and [Prettier](https://prettier.io) is used for CSS and JavaScript formatting. Formatting occurs automatically on save if both platforms are configured according to the [Setup](../setup) guide.

Provided your code is completely and properly structured (e.g., not missing tags or brackets), the following formatting should apply:

- Blank lines and indentation
- Proper spacing around operators, parentheses, and curly brackets
- Semicolons at the end of statements in JavaScript
- Double quotes `"` replaced with single quotes `'` in JavaScript

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
let favoriteFruit = 'apple';

if (favoriteFruit === 'apple') {
  declareLove();
}

function declareLove() {
  console.log('I like apples, too!');
}
```

### Relative Units

Prioritize using relative units in CSS whenever possible to improve responsiveness and consistency in sizing and spacing. Common examples of relative units include:

- `%` - Percentage relative to the parent element.
- `ch` - The width of a character in the element's font size.
- `rem` - Relative to the root element's font size (the browser default).

When using absolute units, such as `px`, aim for consistent and logical increments e.g., multiples of 2 or 10. Adopting CSS variables can help with this by allowing you to define and adjust size denominations in one place.

You can read more about valid absolute and relative units in this [MDN Web Docs reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages).

### CSS Style Selectors

Use element and class selectors, as well as CSS nesting, instead of id selectors in CSS. This approach helps reinforce a "separation of concerns" by reserving id attributes for assigning HTML elements to variables in JavaScript.

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
