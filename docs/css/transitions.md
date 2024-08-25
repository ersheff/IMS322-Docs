# Transitions

Setting a transition time (in seconds) allows changes between two states to occur gradually. The example below demonstrates a transition time using the `:hover` pseudo-class to initiate a change between states.

Keep in mind that [not all CSS properties](https://vallek.github.io/animatable-css/#anim) are fully animatable with transitions. For example, the last button in the example below attempts to transition using `visibility: hidden`, but the button appears and disappears inconsistently without a fade animation.

<p class="codepen" data-height="400" data-default-tab="css,result" data-slug-hash="qBgevZq" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevZq">
  CSS Transitions (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
