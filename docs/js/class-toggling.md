# Class Toggling

If your goal is simply to change the _appearance_ of an element on the page (as opposed to its _content_), a convenient method is toggling a class on or off. This approach works well because elements can have multiple classes - for example, one applied manually in the HTML for default styling and another controlled dynamically via JavaScript using the `class.toggle()` method. Any properties defined in the second class will override those in the first.

Since we need to reference both the interactive element (the `<button>`) AND the element that will change (the `<p>`), they both need unique id attributes.

```html
<button id="color-toggle-btn">Click Me</button>

<p id="changing-text" class="blue-text">Hello, world.</p>
```

In CSS, define both the default style and the changes that should occur to the `<p>` element when the button is clicked.

```css
/* default */
.blue-text {
  color: #1111ff;
}

.red-text {
  color: #ff1111;
}
```

In JavaScript, we introduce two new concepts:

1. When defining a function, start by creating variables that reference _the element(s) that will change_ when the function is triggered. In this case, we will be changing the color of the text in the `<p>` element. Waiting to declare the variable until it is needed can help organize and scope your code appropriately.
2. Use the method `classList.toggle()` to add/remove the `.red-text` class.

```js
const colorToggleBtn = document.querySelector("#color-toggle-btn");

colorToggleBtn.addEventListener("click", colorToggle);

function colorToggle() {
  const changingText = document.querySelector("#changing-text");
  changingText.classList.toggle("red-text");
}
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qBgevNq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevNq">
  Class Toggle 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Active/Inactive States

One useful application of `classList.toggle()` is to think of elements as having "active" and "inactive" states. There is no new code to learn for this approach - it's just a way for you as the developer to mentally model the interaction.

Let's create a text drawer that opens and closes when a button is clicked. In CSS, define the default or "active" state for the element. A `transition` is applied so that the change will occur gradually rather than immediately, while the `overflow: hidden` property ensures that no text spills out when the drawer is closed.

```css
.open-drawer {
  margin: 0;
  padding: 1rem;
  background-color: #ccccff;
  max-height: 4rem;
  transition: 0.2s;
  overflow: hidden;
}
```

To close the drawer, set its `max-height` and vertical `padding` to 0.

```css
.closed-drawer {
  padding: 0 1rem;
  max-height: 0;
}
```

**Why are we using max-height instead of height?**
Typically, you wouldn't need to specify a height value for a `<p>` element, as the browser handles it automatically. However, for a transition to occur, the element _must have a specific value to transition from/to_ (`auto` will not work). We use `max-height` instead of `height` because it allows for an approximation - `4rem` is sufficient to display all the text without creating extra empty space.

The rest of the HTML and JavaScript code is essentially the same as the previous example.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WNPVmxL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNPVmxL">
  Class Toggle 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
