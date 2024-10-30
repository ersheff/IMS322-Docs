---
title: Forms
---

The `<form>` element is used to collect user data with one or more inputs and either process the values directly in JavaScript or submit the data to a server. Grouping multiple inputs in a `<form>` is beneficial because it enables access to all values in a single dataset using a single "submit" event (often triggered with an `<input type="submit">`).

Adding the `name` attribute to inputs is crucial when working with forms, as it allows access to individual values as properties of the form.

In the examples below, you'll notice that while values are correctly logged to the console upon form submission, the page reloads with a 404 error. This happens because the form's default action is to send data to a server, and the error occurs because we have not set up a server to receive the data. _This is expected behavior_ and will not be an issue once we move to placing forms within modals in later readings and examples.

<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="abeGoQp" data-pen-title="Form Submission (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abeGoQp">
  Form Submission (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Input Validation

Validating inputs ensures that the data entered by the user matches the expected format. There are many ways to apporach input validation with varying levels of complexity, but the most direct and simlple implementation is to use the input `type` attribute that best fits the requirements, along with the `required` attribute to prevent empty values.

You can read more about the various `type` attributes for inputs [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#input_types).

<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="WNVJNbe" data-pen-title="Form Submission (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNVJNbe">
  Form Submission (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
