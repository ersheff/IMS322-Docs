---
title: More DOM Manipulation
---

If you recall from a previous reading, the DOM (Document Object Model) is "the data representation of the objects that comprise the structure and content of a document on the web."

You can think of the structure of the DOM in terms of _parents_ and _children_ using a diagram like this:

<img src="../images/dom.webp">

There are 3 child elements in the `<body>` of the diagram - an `<h1>`, `<p>`, and `<img>` - each which also have their own attributes and inner text. The corresponding HTML would look something like this:

```html
<body>
  <h1>My Site</h1>
  <p>Blah blah blah blah blah blah</p>
  <img src="pic.webp" />
</body>
```

Take a look at the following example - how would you describe the structure in terms of parents and children? You can probably make some guesses just by looking at the results, but you should open the inspector and/or look at the HTML to confirm.

<p class="codepen" data-height="500" data-default-tab="html,result" data-slug-hash="XWGrjOq" data-editable="true" data-user="ersheff" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/XWGrjOq">
  Parent-Child (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
Each `<img>` has a `<figcaption>` sibling, both of which are children of a `<figure>` element, which are themselves children of the `<div>` flex row. Or, looking at it from the other direction, the `<div>` flex row is the parent element containing 3 `<figure>` children, which each contain one `<img>` child element and one `<figcaption>` child element. 
## Creating Elements and Appending Children
If you were given a large collection of images in a folder to display in a responsive gallery site, you might manually create flexboxes for rows, `<figure>` or `<div>` elements for image containers, and `<img>` elements in your HTML. But what if you were running a website for a cafe that featured different specials and events each week? Might it be easer to automatically generate the HTML with some information about the images in the folder?

Let's start with a single photo. If you were to create an object that describes a single photo from [Lorem Picsum](https://picsum.photos), it might look like this:

```js
const photo = {
  url: "https://picsum.photos/id/292/800/600.webp",
  alt: "onion and peppercorns",
  caption: "Onion and Peppercorns."
};
```

You can use JavaScript to create each required element using the `createElement()` method and set the required attributes:

```js
const figureElement = document.createElement("figure");
const imageElement = document.createElement("img");
const captionElement = document.createElement("figcaption");

// sets src attribute to "https://picsum.photos/id/292/800/600.webp"
imageElement.src = photo.url;
// sets alt text attribute to "onion and peppercorns"
imageElement.alt = photo.alt;
// sets inner text of <figcaption> to "Onion and Peppercorns."
captionElement.innerText = photo.caption;
```

Then, you can use the `appendChild()` method to append the `<img>` and `<figcaption>` elements to the `<figure>` element and the `<figure>` element to the `<body>` (see example below).

<p class="codepen" data-height="500" data-default-tab="js,result" data-slug-hash="mdobOPe" data-editable="true" data-user="ersheff" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdobOPe">
  Creating and Appending Elements (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Creating and Appending Elements in a For Of Loop
In the example below, an array containing objects is used to generate elements for a flexbox-based row of photos. Each object contains information about the photo source (url), alt text, and caption text.
<p class="codepen" data-height="680" data-default-tab="js,result" data-slug-hash="PoLpZQV" data-editable="true" data-user="ersheff" style="height: 680px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoLpZQV">
  Generating a Photo Row with a For Of Loop (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
