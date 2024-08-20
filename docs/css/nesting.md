# Nesting

Excerpted from MDN Web Docs ["Using CSS nesting"](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Using_CSS_nesting):

> The CSS nesting module allows you to write your stylesheets so that they are easier to read, more modular, and more maintainable. As you are not constantly repeating selectors, the file size can also be reduced.

> You can use CSS nesting to create child selectors of a parent, which in turn can be used to target child elements of specific parents.

While nesting may not be appropriate for all situations, one notable benefit is that the structure more closely resembles the corresponding HTML in which child tags/selectors are wrapped in parent tags/selectors.

<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="PoVMLGa" data-pen-title="CSS Nesting 1 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLGa">
  CSS Nesting 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

It can also help alleviate the clumsiness of creating multiple classes, so long as the heirarchy of your document structure is not too complicated. In the example below, a class only needs to be named for the parent `<div>` since the color change will only apply to `<p>` elements that are children of the `dark-bg` class.

<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="BagZjBr" data-pen-title="CSS Nesting 2 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BagZjBr">
  CSS Nesting 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
