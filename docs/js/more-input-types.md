---
title: More Input Types
---

Buttons are the simplest form of control or input type. They present only one choice: to click or not to click, with no other information or decision-making required.

There are many other HTML input types and input-like elements that vary in complexity and intended application. Whenever possible, the type of input presented to the user should be the best fit for the information being collected.

This page provides an overview of a few other commonly used input types. A full reference for all valid input types can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input).

In each the examples below, `change`, or `input` event listeners are used to gather values.

## List Controls

List controls allow users to select from a small set of text strings, each representing a command, object, or attribute. The dropdown menu in the example below is created using `<select>` tags instead of `<input>` tags. Each item in the dropdown menu is created by adding `<option>` elements as children.

Some important things to note about `<select>` dropdown menus:

- The `value` attribute is what will be gathered in your JavaScript. This does not need to match the displayed text.
- It is recommended to put instructions in the first `<option>` with an empty `value`, as this will be the first thing the user sees by default. This will also prompt the user to make a selection.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="dyrbOzP" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/dyrbOzP">
  List Controls (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Entry Controls

Entry controls enable users to supply their own value. The most basic entry control is the `<input>` element with type attribute `text` (the default). However, there are other entry control types that may be better suited to certain data types. For example, the `email` type provides a simple way to check for valid email address formatting, while the `number` type includes increment and decrement buttons, as well as minimum and maximum attributes.

The `placeholder` attribute of entry controls is also very useful. Placeholder text can provide sample values or hints when the `<label>` alone is not sufficient.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="yLwBVoE" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/yLwBVoE">
  Entry Controls (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
