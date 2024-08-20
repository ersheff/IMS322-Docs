# Flexbox

Flexbox is used to create responsive layouts. It is typically considered ideal for 1-dimensional rows or columns, though more complex layouts can be achieved by nesting flexboxes inside of each other.

From CSS Tricks' ["A Complete Guide to Flexbox"](https://css-tricks.com/snippets/css/a-guide-to-flexbox/):

> The main idea behind the flex layout is to give the container the ability to alter its items’ width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). A flex container expands items to fill available free space or shrinks them to prevent overflow.

<figure markdown="span">
  ![Flexbox Container](../assets/01-container.svg){ width="400px" }
  <figcaption>Flexbox Container (image source: CSS Tricks)</figcaption>
</figure>

<figure markdown="span">
  ![Flexbox Items](../assets/02-items.svg){ width="400px" }
  <figcaption>Flexbox Items (image source: CSS Tricks)</figcaption>
</figure>

The CSS Tricks article ["A Complete Guide to Flexbox"](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) is an excellent reference for all things flexbox. To get started, this selection of seven properties (demonstrated in the example below) can be used to accomplish most layout goals:

**Container properties:**

- `display` - Set this property value to `flex` to create a flexbox container.
- `flex-direction` - Options are `row` (the default) or `column`.
- `flex-wrap` - By default, flexbox will try to fit everything in one row. Set the value of this property to `wrap` to wrap flex items to multiple rows as needed (only works if items have a fixed or minimum size).
- `justify-content` - Defines the alignment along the main axis.
- `align-items` - Defines the alignment along the cross axis.
- `gap` - Controls the space between flex items.

**Item properties:**

- `flex` - Determines how much space an item will inhabit proportionally. For example, a flex item with `flex: 2` will take up twice as much space as a flex item with `flex: 1`.

_When testing responsiveness with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen** and using your browser's [Device Mode](https://developer.chrome.com/docs/devtools/device-mode) (Chromium-based) or [Responsive Design Mode](https://firefox-source-docs.mozilla.org/devtools-user/responsive_design_mode/) (Firefox)._

<p class="codepen" data-height="600" data-default-tab="css,result" data-slug-hash="VwRLgEg" data-editable="true" data-user="ersheff" style="height: 600px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/VwRLgEg">
  Flexbox (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
