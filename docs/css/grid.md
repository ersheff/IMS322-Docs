# Grid

Grid is similar to [flexbox](./flexbox) in that it is used to create responsive layouts that adapt to fill the available space. However, while it can certainly be used for smaller components, grid is a two-dimensional layout system that is typically adopted for creating larger layouts.

The scope of properties and options in grid can be a little overwhelming. As with flexbox, CSS has an excellent article called ["A Complete Guide to CSS Grid"](https://css-tricks.com/snippets/css/complete-guide-grid/#aa-introduction) that covers just about everything, but this selection of nine properties (demonstrated in the examples below) will be sufficient for most basic layout needs:

**Container properties:**

- `display` - Set this property value to `grid` to create a grid container.
- `grid-template-columns` - Use to define the quantity and size of columns in your grid.
- `grid-template-rows` - Use to define the quantity and size of rows in your grid.
- `grid-auto-rows` - Specifies the size of any auto-generated grid rows.
- `gap` - Controls the space between grid rows and columns.
- `justify-content` - Similar to its use in flexbox, this property sets the alignment of items along the row axis. However, it really only has an effect when grid items are sized with non-flexible units, like `px`.
- `align-items` - Similar to its use in flexbox, this property sets the alignment of items along the column axis. However, it really only has an effect when items within a row have varying heights.

**Item properties:**

- `justify-self` - Aligns a single grid item inside its cell along the row axis.
- `align-self` - Aligns a single grid item inside its cell along the column axis.

_When testing responsiveness with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and using your browser's [Device Mode](https://developer.chrome.com/docs/devtools/device-mode) (Chromium-based) or [Responsive Design Mode](https://firefox-source-docs.mozilla.org/devtools-user/responsive_design_mode/) (Firefox)._

<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="BagZVBE" data-pen-title="Grid 1 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BagZVBE">
  Grid 1 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br>
<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="PorjaGg" data-pen-title="Grid 2 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PorjaGg">
  Grid 2 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br>
<p class="codepen" data-height="300" data-default-tab="css,result" data-slug-hash="QWXgxNw" data-pen-title="Grid 3 (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/QWXgxNw">
  Grid 3 (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

If you're not sure whether flexbox or grid would be more suitable for your layout needs, consider the following advice:

- Do you just need to center something? Use flexbox.
- Do you just need elements in a single row or column, like a row of photos or inputs? Use flexbox.
- Is it possible that the number of elements in your layout will change from time to time? Use grid (or possible flexbox with wrap).
- Do you want to plan the full layout of your page with a header, nav bar, sidebar, footer, and possibly more? Use grid.
- Do you need an asymmetrical or multi-dimensional layout? Use grid.

Ultimately, flexbox can be a bit easier to start with and conceptualize, but grid is more powerful and versatile once you get the basics down. And you can always use both!

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
