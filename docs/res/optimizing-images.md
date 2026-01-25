# Optimizing Images

## Image Resolution and Compression

Although internet speeds have greatly increased over the years, it is still important to reduce image file sizes using appropriate resolution and compression settings.

For resolution, consider how much of the browser window your images will cover (in pixels), then _double that value_ when cropping or downloading image files to accommodate HiDPI displays.

For example, if you're targeting a maximum layout width of `1400px`:

- An image spanning the entire body should have a width around `2800px`.
- An image spanning half the body (e.g., in a 2-column layout) should have a width around `1400px`.
- An image spanning one-third the body (e.g., in a 3-column layout) should have a width around `933px`.
- When using [Lorem Picsum](https://picsum.photos), specify the required resolution in the URL.
- When downloading images from [Unsplash](https://unsplash.com), another stock photo site, or using your own images, resize them with [Squoosh](https://squoosh.app) or your preferred photo editing tool if needed before adding them to your project.

You are not expected to perfectly match every image to its layout proportions, but keep in mind that even a fullscreen image rarely needs to exceed the resolution of a 4K display. Part of the graded requirements for projects is that:

"All images must be in `jpeg` or `webp` format with a resolution no larger than `3840` pixels in width or `2160` pixels in height. Logos, icons, or other vector drawings may be in `svg` format. Use [Squoosh](https://squoosh.app/) or another image editor to resize or compress images before adding them to your project (set quality level around 80%)."

## Fluid Images

It is highly recommended to start sizing all `<img>` elements using _only_ `max-width: 100%`. This ensures they responsively fill their closest parent container, regardless of the original resolution of the image file. It also allows responsive layout containers like **Flexbox** and **Grid** to manage image sizing effectively when multiple images appear in the same row.

If needed, wrap an `<img>` in a `<div>` or `<figure>` element (with a `<figcaption>` if a caption is needed) to keep images and captions paired, even when the browser window resizes. Note that `<figure>` has default margins, which you may want to adjust or remove for better spacing.

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="KKEpJzp" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKEpJzp">
  Fluid Images (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
