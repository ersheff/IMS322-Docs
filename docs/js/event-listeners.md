---
title: Event Listeners
---

An _event_ is a signal that something has happened in the browser. There are several triggers for [events](https://developer.mozilla.org/en-US/docs/Web/Events), some that occur automatically (e.g. the [load](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event) event fires when the page has finished loading), and others that occur in response to an interaction from the user (e.g. the [click](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event) event fires when the user clicks on a page element). In this class, we will primarily be focussed on the latter category.

In order to make something happen in response to an event, we need to attach an [event listener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) to the interactive element in JavaScript.

## Adding an Event Listener

As with many coding scenarios, there are multiple ways to approach browser-based interaction development. For consistency and simplicity, the recommended procedure for this class is as follows:

1. Declare a variable to reference the interactive element.
2. Write a function that defines what should happen when the interaction occurs.
3. Add an event listener that calls the function.

### Step 1: Declare a variable to reference the interactive element

In addition to the [basic data types](basic-data-types) that we have already covered (number, string, boolean), a variable can also be assigned to an _HTML element_.

```js
let myButton = document.querySelector("#my-button");
```

Notice that the argument of this method begins with `#`, which is the CSS selector for ids - this implies that the element we are trying to reference should have a matching _id_ attribute.

```html
<button id="my-button">Click Me</button>
```

Also notice that the naming convention for the id in HTML (and where it is used in `querySelector`) is _kebab-case_, while the variable name in JavaScript is _camelCase_. I recommend using the same words for both the id and the variable name, but styled appropriately (kebab-case or camelCase, based on location in code).

### Step 2: Write a function that defines what should happen when the interaction occurs

In this simple example, we will log the message "Button was clicked!"" to the console.

```js
function wasClicked() {
  console.log("Button was clicked!");
}
```

### Step 3: Add an event listener that calls the function

The _event listener_ should be added to the element that fires the desired event - in this case, _the element that the user interacts with_, which is a button. As previously mentioned, there are many different kinds of events that can be listened for - we will specifically be listening for the _click_ event.

```js
myButton.addEventListener("click", wasClicked);
```

Notice that this statement begins with the variable name that we created in step 1. The `addEventListener()` method is given 2 arguments: the event type to listen for (`"click"`), followed by the name of the function we created in step 2 (`wasClicked`).

Click the button in the example below. Remember, you'll need to open the console in order to see the results.

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qBvWqaG" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBvWqaG">
  Event Listener (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
