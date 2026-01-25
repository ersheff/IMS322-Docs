---
title: Manipulating Style Properties
---

In general, it is recommended to change styling with `classList.toggle()`, `classList.add()`, and/or `classList.remove()` whenever possible, especially when alternating between two states. However, if more direct or continuous control is required, `style.setProperty()` may be a better fit.

```js
style.setProperty("property-name", "value");
```

The `'property-name'` string can be any familiar CSS styling property, such as `'background-color'` or `'font-size'`. For the `'value'`, units usually need to be appended using string concatenation e.g. by adding `'px'` or `'rem'` to the end of a variable or number.

<p class="codepen" data-height="500" data-default-tab="html,result" data-slug-hash="qBgevRR" data-editable="true" data-user="ersheff" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevRR">
  Manipulating Style Properties (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
