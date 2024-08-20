# Optimizing Images

## Image Resolution and Compression

Although internet speeds are much faster than they used to be, it is still important to reduce image file sizes if possible with suitable resolution and compression settings.

For resolution, you should consider how much of the browser window your images will cover (in pixels), and then _double that value_ when cropping or downloading image files. Assuming a maximum `1100px` layout width:

- An image that will span the entire body should have a width around `2200px`.
- An image that will span half the body (e.g. in a 2-column layout) should have a width around `1100px`.
- An image that will span 1/3 the body (e.g. in a 3-column layout) should have a width around `734px`.
- When using images from [Lorem Picsum](https://picsum.photos), specify the desired resolution in the url.
- When using images downloaded from [Unsplash](https://unsplash.com), another stock photo site, or your own original image files, resize them using [Squoosh](https://squoosh.app) or your preferred photo editing application before incorporating them into your project.

There are several different types of image compression codecs suitable for web development. For simplicity, all images used in your projects should be in the WebP format.

- When using images from [Lorem Picsum](https://picsum.photos), simply add `.webp` to the end of the url.
- When using images downloaded from [Unsplash](https://unsplash.com), another stock photo site, or your own original image files, choose WebP when compressing your files using [Squoosh](https://squoosh.app) or your preferred photo editing application before incorporating them into your project.

## Image Containers

It is highly recommended to style all `<img>` elements with `width: 100%` and wrap them in a parent container like `<div>` or, if captions are needed, `<figure>`. This will often make it easier to attain the desired size, position, and aspect ratio with responsive layouts and is generally all that is needed when putting multiple images in a flexbox or grid layout. If other size conditions are required, like `min-width` or `max-width`, these should be applied to the parent container.

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="KKEpJzp" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKEpJzp">
  Image Containers (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
