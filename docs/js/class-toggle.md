---
title: Class Toggle
---

Now that we can add event listeners to HTML elements, let's design a simple interaction that actually changes something on the page!

If your goal is to change the appearance of a page element (as opposed to the content), one simple way to do so is by toggling a class on or off. Let's start by creating a button that toggles the color of some text between black (the default) and red.

Since we will need to reference both the interactive element `<button>` AND the changing element `<p>`, they will both need unique id attributes.

```html
<button id="color-toggle-btn">Click Me</button>

<p id="changing-text">Hello, world.</p>
```

In CSS, create a class that describes the style changes that should occur on the element `<p>` when the button is clicked.

```css
.red-text {
  color: red;
}
```

In JavaScript, we have 2 new concepts:

1. When writing the function, start by creating variables that reference the element(s) that will change when the function runs. In this case, we will be changing the color of the text in the `<p>` element.
2. We will use the new method `classList.toggle()` to add/remove the `.red-text` class.

```js
let colorToggleBtn = document.querySelector("#color-toggle-btn");

colorToggleBtn.addEventListener("click", colorToggle);

function colorToggle() {
  let changingText = document.querySelector("#changing-text");
  changingText.classList.toggle("red-text");
}
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qBgevNq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevNq">
  Class Toggle 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Active/Inactive States
One useful application of `classList.toggle()` is to think of elements having "active" and "inactive" states. There is nothing new to the code in this approach - rather, it's just a way for you as the developer to mentally model the interaction states.

Let's start by created a text drawer that opens and closes when a button is clicked. This type of interaction may be used to show and hide text that will not be visible all the time.

In CSS, define a default or "active" state for the element. Here, `background-color` is applied for illustrative purposes (it will make it easier to see the changes). A `transition` is applied so that the change will occur gradually rather than immediately. Finally, the `overflow: hidden` property prevents text from spilling out of the drawer when closed.

```css
.open-drawer {
  background-color: lightblue;
  max-height: 1.2rem;
  transition: 0.5s;
  overflow: hidden;
}
```

To close the drawer, all we have to do is set its `max-height` to 0.

```css
.closed-drawer {
  max-height: 0;
}
```

**Why are we using max-height instead of height?**
Usually, you would not need to specify a height value for a `<p>` element as it would be set automatically by the browser. However, in order to have a transition, the element _needs a value to transition to/from_ - `auto` will not work for this. The reason that we are using `max-height` instead of `height` is because then we don't need to be too precise - `1.2rem` as an approximation is sufficient for displaying all of the text content without creating extra empty space.

The rest of the HTML and JavaScript code is essentially the same as the previous example.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WNPVmxL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNPVmxL">
  Class Toggle 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
