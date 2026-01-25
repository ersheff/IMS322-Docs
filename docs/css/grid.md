# Grid

**Grid** is similar to [flexbox](../flexbox) in that it is used to create responsive layouts that adapt to fill the available space. However, while grid can be used for smaller components, it is primarily a two-dimensional layout system typically adopted for creating larger layouts.

The scope of properties and options in grid can be a little overwhelming. As with flexbox, CSS Tricks has an excellent article called ["CSS Grid Layout Guide"](https://css-tricks.com/snippets/css/complete-guide-grid/) that covers just about everything, but this selection of nine properties (demonstrated in the examples below) will suffice for most basic layout needs:

**Container properties:**

- `display` - Set this property value to `grid` to create a grid container.
- `grid-template-columns` - Defines the number and size of columns in your grid.
- `grid-template-rows` - Define the number and size of rows in your grid.
- `grid-auto-rows` - Specifies the size of any auto-generated grid rows.
- `gap` - Controls the space between grid rows and columns.
- `justify-content` - Similar to its use in flexbox, this property sets the alignment of items along the row axis. However, it only has an effect when grid items are sized with non-flexible units, such as `px`.
- `align-items` - Similar to its use in flexbox, this property sets the alignment of items along the column axis. However, it only has an effect when grid items within a row have varying heights.

**Item properties:**

- `justify-self` - Aligns a single grid item inside its cell along the row axis.
- `align-self` - Aligns a single grid item inside its cell along the column axis.

## Flexbox or Grid?

If you're not sure whether flexbox or grid is more suitable for your layout needs, consider the following:

- **Center a single element?** Use flexbox.
- **Arranging elements in a single row or column, like a row of photos or inputs?** Use flexbox.
- **Expecting the number of elements in your layout to change from time to time?** Use grid (or flexbox with wrapping).
- **Planning the overall layout of your page with a header, nav bar, sidebar, footer, and possibly more?** Use grid.
- **Creating an asymmetrical or multi-dimensional layout?** Use grid.

Ultimately, flexbox can be a bit easier to start with and conceptualize, but grid is more powerful and versatile once you get the basics down. You can always use both in your projects!

_When testing responsiveness with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen**, then use your browser's [Device Mode](https://developer.chrome.com/docs/devtools/device-mode) (Chromium-based) or [Responsive Design Mode](https://firefox-source-docs.mozilla.org/devtools-user/responsive_design_mode/) (Firefox)._

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

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
