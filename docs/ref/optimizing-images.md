# Optimizing Images

## Image Resolution and Compression

Although internet speeds have greatly increased over the years, it is still important to reduce image file sizes using appropriate resolution and compression settings.

For resolution, consider how much of the browser window your images will cover (in pixels), then _double that value_ when cropping or downloading image files (to accommodate HiDPI displays). Assuming a maximum layout width of `1100px`:

- An image spanning the entire body should have a width around `2200px`.
- An image spanning half the body (e.g., in a 2-column layout) should have a width around `1100px`.
- An image spanning one-third the body (e.g., in a 3-column layout) should have a width around `734px`.
- When using [Lorem Picsum](https://picsum.photos), specify the required resolution in the URL.
- When downloading images from [Unsplash](https://unsplash.com), another stock photo site, or using your own images, resize them with [Squoosh](https://squoosh.app) or your preferred photo editing tool before adding them to your project.

You are not expected to perfectly match every image to its layout proportions, but keep in mind that even a fullscreen image rarely needs to exceed the resolution of a 4K display. Our GitHub autograder will check that no image files are larger than `3840px` in width, as anything larger is unnecessary.

There are several different types of image compression codecs suitable for web development. For simplicity, all images used in your projects should be in the WebP format.

- When using [Lorem Picsum](https://picsum.photos), simply add `.webp` to the end of the URL.
- For all other image sources, choose the WebP codec when compressing your files using [Squoosh](https://squoosh.app) or another application.

## Fluid Images

It is highly recommended to start sizing all `<img>` elements using _only_ `width: 100%` (the default in project templates). This ensures they responsively fill their closest parent container, regardless of the original resolution of the image file. It also allows responsive layout containers like **Flexbox** and **Grid** to manage image sizing effectively when multiple images appear in the same row.

If needed, wrap an `<img>` in a `<figure>` element with a `<figcaption>` to keep images and captions paired, even when the browser window resizes. Note that `<figure>` has a default margin, which you may want to adjust or remove for better spacing.

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="KKEpJzp" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKEpJzp">
  Fluid Images (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
