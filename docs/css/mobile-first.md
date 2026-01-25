# Mobile-First Design

**Mobile-first design** is an approach that focuses on prioritizing small screen sizes, treating them as the "default" display target when designing layouts. When using **Flexbox** or **Grid** in combination with responsive styling properties and units, such as `max-width` and `%`, a well-designed mobile-first layout can often respond automatically to larger displays, expanding to fill available space in an organized and sensible way. Layouts can be progressively enhanced using **media queries** when the default behaviors of responsive methods are not sufficient.

## Responsive Design Mode

The best way to target small displays is to use the **Responsive Design Mode** (aka **Device Mode**) found in your browser's **Developer Tools**. This mode allows you to resize the browser window to specific resolutions or even models of mobile devices.

## Media Queries

**Media queries** allow you to responsively apply different styling depending on the size of the browser window or device screen. Common uses for media queries include adjusting the visibility, size, or layout direction (row vs. column) of elements to better fit different screen sizes, though any property can be modified as needed.

Since our main class projects treat any display width below `640px` as the "default" target for mobile-first design, a media query to address larger displays is included in all project templates.

```css
@media (min-width: 640px) {
  .flex-container {
    flex-direction: row;
  }
}
```

_When testing responsiveness with embedded CodePen examples, you should open the Pen in its own window by clicking **Edit On CodePen**, then use your browser's [Device Mode](https://developer.chrome.com/docs/devtools/device-mode) (Chromium-based) or [Responsive Design Mode](https://firefox-source-docs.mozilla.org/devtools-user/responsive_design_mode/) (Firefox)._

<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="bGZdPbe" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/bGZdPbe">
  Media Queries (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
