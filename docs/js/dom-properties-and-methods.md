---
title: DOM Properties and Methods
---

The Document Object Model (DOM) is the "representation of the objects that comprise the structure and content of a document on the web." It represents the page in a way that programs, like JavaScript, can manipulate the document structure, style, and content.

The DOM defines:

**HTML elements _as objects_** (i.e., how an HTML element is represented when assigned to a variable).

```js
const mainHeading = document.querySelector("#main-heading");
```

**The _properties_ of HTML element objects**, which are similar to attributes in HTML.

Properties can be set:

```js
headshotImage.src = "images/headshot.webp";
```

Properties can also be read:

```js
const volume = sliderInput.value;
```

**The _methods_ (actions) that can be performed on or by HTML element objects.** Methods are like functions defined within an object (notice that they have parentheses). Many (but not all) methods require arguments inside the `()`.

```js
primaryButton.classList.toggle("active");
```

**The _events_ that can be triggered by HTML elements.**

```js
primaryButton.addEventListener("click", toggleState);
```

## Getting Started with Properties

Here are some common examples of setting and reading properties in JavaScript.

### innerText

To change the text displayed in an HTML element via JavaScript, assign a value to the `innerText` property:

```js
element.innerText = "Hello!";
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="poGMYEX" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYEX">
  innerText (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

### value

`<input>` elements have a `value` attribute that can be read or assigned in JavaScript.

In the example below, four sliders each have a different initial value set in the HTML (as an attribute), which is why they start at different positions (sliders default to a range of 0 to 100).

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="OJdKqbw" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/OJdKqbw">
  Input Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

These values can be read in JavaScript by listening for the `input` event (e.g., in response to user ineraction), or set programmatically.

<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="abXeMBZ" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abXeMBZ">
  Getting and Setting Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Getting Started with Methods

Some methods - like `document.querySelector()`, `console.log()`, `.addEventListener()`, and `classList.toggle()` - are used so frequently that they become second nature. At times, you might need to reference online documentation to explore more methods (or properties and events) associated with an object. For example, the `play()` method is described in the [Basic Usage](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement#basic_usage) section of the MDN Web Docs article on HTML Audio Elements.

<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="vYPGjPy" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPGjPy">
  Audio Element Methods (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
