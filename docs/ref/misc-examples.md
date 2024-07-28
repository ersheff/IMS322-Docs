---
title: Miscellaneous Examples
---

This page includes a collection of basic examples for unique scenarios that fall outside of the regular course content. They will not be covered during class but can be adopted and modified for assignments as needed.

## Wireframe Outlines

This example is intended to help clarify the relationship between a wireframe and the resulting HTML structure. Notice that there are boxes drawn around every part of the wireframe that corresponds with a discrete element in the HTML. For example, in order to achieve the desired alignment of the contents inside the question button (space between) and address the indicator from JavaScript for the open/close transition (the + sign), they are each different elements inside the `<button>`.

<p class="codepen" data-height="420" data-default-tab="html,result" data-slug-hash="BabzGpb" data-editable="true" data-user="ersheff" style="height: 420px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BabzGpb">
  Wireframe Outlines (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

wireframe example

Although color-coded boxes are important for clarity, it is perfectly appropriate to use the same color for sibling elements (those that occur at the same hierarchical level in the HTML, like the 2 elements inside the button).

wireframe example outlines

## Click to Reveal

Uses `position: absolute` to place one element on top of another, then changes the top element's opacity to make it appear as though the bottom element is being revealed. _Be very careful_ when using `position: absolute`. It should only be implemented when absolutely necessary. Layout positioning may become unpredictable when modifying the position property. For additional information, reference [this MDN Web Docs article](https://developer.mozilla.org/en-US/docs/Web/CSS/position).

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="BabBQWW" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BabBQWW">
  Click to Reveal (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Plus-Minus Indicator

Uses `position: absolute` to draw a separate vertical line on top of a horizontal line (both created using `<div>` elements) in order to independently change only the vertical line and create a smooth transition from **+** to **-**.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="zYbBqVK" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYbBqVK">
  Plus-Minus Indicator (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Working with Background Images

<p class="codepen" data-height="720" data-default-tab="js,result" data-slug-hash="eYozXNe" data-editable="true" data-user="ersheff" style="height: 720px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/eYozXNe">
  Background Images (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Date Formatting

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MWRGqXr" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/MWRGqXr">
  Date Formatting (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Flex-wrap Sizing
When wrapping items in a flexbox, one of the challenges is to create items with flexible yet consistent widths, especially when there are fewer items on the bottom row. The approach used in this example (adapted from the GameStop site) uses media queries to set the `width` of items to progressively smaller `%` based on window width.

There are a couple of accommodations that need to be made when calculating widths this way in a flexbox:

- The flexbox `gap` property cannot be used reliably when attempting to divide the row evenly with `%,` so we've simulated the gap by putting the items in `div` containers and adding `padding` to the container.
- Since this also means that the `padding` doubles up between items, side padding is added to the flexbox row to compensate.
<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="dyLazXy" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/dyLazXy">
  Flex-wrap Sizing (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
