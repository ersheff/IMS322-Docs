# Nesting - XXX

Excerpted from MDN Web Docs ["Using CSS nesting"](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Using_CSS_nesting):

> \[CSS Nesting\] allows you to write your stylesheets so that they are easier to read, more modular, and more maintainable. As you are not constantly repeating selectors, the file size can also be reduced.

> You can use CSS nesting to create child selectors of a parent, which in turn can be used to target child elements of specific parents.

While nesting may not be appropriate for all situations, a notable benefit is that the structure more closely resembles the corresponding HTML - meaning that children inside parent elements can be styled with child selectors inside parent selectors.

```css
parent {
  /* parent styles */

  child {
    /* child of parent styles */
  }
}
```

<iframe height="600" style="height: 600px; width: 100%;" scrolling="no" title="CSS Nesting (IMS322 Docs)" src="https://codepen.io/ersheff/embed/PoVMLGa?default-tab=html%2Cresult" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLGa">
  CSS Nesting (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>
