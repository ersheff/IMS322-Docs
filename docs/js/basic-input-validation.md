---
title: Basic Input Validation
---

When using entry controls, it is a good idea to validate the input in some way to ensure that it adheres to the desired format or range. Basic validation can be implemented using `<input>` element attributes.

## HTML Form Validation

When put inside a `<form>` element, many inputs will automatically validate data upon submission based on their type. For example, an input with type `email` will prompt for a valid email address if one is not provided.

_FYI, the examples on this page will display an error after clicking "Submit" once all fields are completed correctly. This is intentional - the additional steps required to gather all data at once from a `<form>` will be described in subsequent readings._

In this first example:

- All 3 inputs are given the `required` attribute.
- The input with type `email` will not accept data unless it is in the user@domain.com format.
- The input with type `number` will not accept letters.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="bGzXObb" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/bGzXObb">
  Quick Validation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
Further customization can be attained by using the `pattern` attribute to specify the exact format required. However, it must be written as a [regular expression](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) (regex), which can be very challenging. A couple of simple examples are shown below, but beyond that you will likely need to search for additional regex patterns online or use AI tools to help design your own.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="RwvXEbq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwvXEbq">
  Regex Validation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
