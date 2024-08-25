# Variables

CSS variables (aka custom properties) can help ensure consistent styling throughout your site. For example, you can apply a specific color in multiple places without needing to remember and type the exact HEX or RGB code each time. Additionally, if you want to test variations for different properties, you only need to change the value once where the CSS variable is declared at the top of the `style.css` file.

Thare are multiple ways to declare CSS variables, but the most common and general-purpose method is within the `:root` pseudo-element. These variables can then be referenced throughout the rest of the file by their variable name, which should always start with `--`.

<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="wvNVOKx" data-pen-title="CSS Variables (IMS322 Docs)" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvNVOKx">
  CSS Variables (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
