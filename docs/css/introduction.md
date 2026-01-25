# CSS

**CSS** stands for "Cascading Style Sheets." It is the language used to specify the appearance and layout of a web document. In other words, you use CSS to describe what you want your HTML to look like beyond the default styling.

## Selectors and Properties

CSS is written by selecting which elements you want to style, then describing the properties that you want to change. For example, in the snippet below, `h1` is the **selector**, and `color` is the **property** being set to the value `#ff0000` (the HEX code for pure red). This will change the text color of all `<h1>` elements in the linked HTML document.

```css
h1 {
  color: #ff0000;
}
```

If you want to be more selective about which elements you're styling (e.g., not ALL instances of an element type) or you want to apply a set of properties to a group of elements, use the **class** selector, which begins with a `.`. This requires that the targeted HTML elements also have a `class` attribute with the same name.

In this snippet, only the first `<p>` will be red.

```html
<p class="warning">Beware!</p>
<p>Just kidding.</p>
```

```css
.warning {
  color: #ff0000;
}
```

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="QwEqgvr" data-pen-title="CSS Selectors and Properties (IMS322 Docs)" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
      <span>See the Pen <a href="https://codepen.io/ersheff/pen/QwEqgvr">
  CSS Selectors and Properties (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Cascading, Specificity, and Inheritance

The **cascading** of CSS refers to how the browser interprets and applies styling rules.

First, styles defined by the author in a CSS file (that's you) will take precedence over those defined by the browser (the defaults).

Second, styling rules are read from top to bottom of the CSS file. If an element or class selector appears multiple times (which is not recommended), the last one will overwrite any conflicting properties from the previous selectors.

In the snippet below, the second `color` property will take precedence. So, all `<h1>` elements will be blue.

```css
h1 {
  color: #ff0000;
}

h1 {
  color: #0000ff;
}
```

If there is a conflict between multiple types of selectors, then the one with a higher **specificity** will take precedence. For example a **class** selector is _more specific_ than an **element** selector.

In the snippet below, the `<p>` element will be red because `.warning` is more specific, even though the `p` selector appears later.

```html
<p class="warning">Lorem ipsum</p>
```

```css
.warning {
  color: #ff0000;
}

p {
  color: #0000ff;
}
```

If styling properties are not specified for an element, it will take on some properties of its parent through the process of **inheritance**. This is a smart way to apply styling consistently and concisely. For example, if you want all of the text elements inside of `<main>` to be the same color, you can apply the color once to the `main` selector. All other child elements inside of `<main>` will inherit that property.

```html
<main>
  <h1>Welcome</h1>
  <h2>To Jurassic Park</h2>
  <p>Life... uhhhh... finds a way.</p>
</main>
```

```css
main {
  color: #ff0000;
}
```

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="LEZzLLV" data-pen-title="CSS Inheritance (IMS322 Docs)" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
      <span>See the Pen <a href="https://codepen.io/ersheff/pen/LEZzLLV">
  CSS Inheritance (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<script async src="https://public.codepenassets.com/embed/index.js"></script>
