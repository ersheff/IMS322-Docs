# Event Listeners

An _event_ is a signal that something has happened in the browser. There are several triggers for [events](https://developer.mozilla.org/en-US/docs/Web/Events), some that occur automatically (e.g., the [load](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event) event fires when the page has finished loading), and others that occur in response to user interactions (e.g., the [click](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event) event fires when the user clicks on a page element).

To respond to an event, you can attach an [event listener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) to the relevant HTML element in JavaScript.

## Adding an Event Listener

The recommended procedure for this class is as follows:

1. Declare a variable in JavaScript to reference the interactive HTML element.
2. Write a function that defines what should happen when the interaction occurs.
3. Add an event listener that calls the function in response to the intended event.

### Step 1: Declare a variable in JavaScript to reference the interactive HTML element.

When an HTML element is assigned to a variable using `document.querySelector()`, it is treated as an [_object_ data type](https://ersheff.github.io/IMS322-Docs/js/data-types/#object). More specifically, it is a class of object called _HTMLElement_.

```html
<button id="my-button">Click Me</button>
```

```js
const myButton = document.querySelector("#my-button");
```

Note that the naming convention for the `id` attribute in HTML (and how i's used in `querySelector`) is _kebab-case_, while the variable name in JavaScript is _camelCase_. Although they are the same words, they represent different things in different contexts. This is also a valid way to assign an HTML element to a variable:

```js
const button1 = document.querySelector("#my-button");
```

However, using the same words for both the `id` and the variable name (styled appropriately in kebab-case or camelCase), simplifies the process, as it reduces the number of names you need to create and remember.

### Step 2: Write a function that defines what should happen when the interaction occurs

```js
function wasClicked() {
  console.log("Button was clicked!");
}
```

### Step 3: Add an event listener that calls the function

The _event listener_ should be added to _the element that fires the desired event_ - in this case, the button that the user interacts with.

```js
myButton.addEventListener("click", wasClicked);
```

Notice that the statement begins with the variable name that we created in step 1. The `addEventListener()` method takes 2 arguments: the event type to listen for (`"click"`) and the name of the function we created in step 2 (`wasClicked`).

_When using the console with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and then clicking the **Console** button in the CodePen editor._

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qBvWqaG" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBvWqaG">
  Event Listener (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
