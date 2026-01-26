# Properties and Units

## Common Styling Properties

As with HTML tags and attributes, there are dozens of valid CSS style properties, all of which can be found [here on MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties). The collection of properties listed below should be sufficient for most of your styling and layout needs.

### Basic Text and Container Appearance

- [background-color](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/background-color)
- [border](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border)
- [border-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/border-radius)
- [color](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/color)
- [font-family](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-family)
- [font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-size)
- [font-weight](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/font-weight)

### Basic Layout, Sizing, and Spacing

- [height](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/height)
- [line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/line-height)
- [margin](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/margin)
- [padding](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/padding)
- [text-align](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/text-align)
- [width](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/width)

### Responsive Design

- [display](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/display) (primarily used for **Flexbox** or **Grid**)
- [max-height](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/max-height)
- [max-width](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/max-width)
- [min-height](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/min-height)
- [min-width](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/min-width)

### Effects

- [opacity](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/opacity)
- [transform](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/transform) (e.g., scale, rotate, translate)

## Units

There are multiple valid ways to specify **units** for any style property that deals with size or space, such as **width**, **height**, **font-size**, **border-radius**, etc. Again, the list below is just a selection of recommended units to apply to your designs.

### Absolute Units

- `px` - Absolute pixel units.

### Relative Units

- `%` - Relative to the parent element's corresponding property (e.g., **width**, **height**, etc.).
- `ch` - Relative to the width of a "0" text character at the element's current font size.
- `em` - Relative to the element's current font size (roughly the height of the text).
- `rem` - Relative to the root document's font size (`1rem` is usually equivalent to `16px`).
