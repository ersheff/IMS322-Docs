# Elements

In the introduction, we've already seen some of the most common element types used in HTML: headings and paragraphs.

There are dozens of other types of elements that all have unique purposes. You will probably never use many of them, and you certainly do not need to attempt to memorize them all. There are freely available online reference pages, such as [this one from MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements), that you can visit and search any time.

That being said, it can be helpful to identify a smaller collection of important elements to focus on at this stage.

## The Only Tags You Need to Know (for now)

You should be familiar with all of the tags listed below, which have been excerpted from Kevin Powell's ["The Only Tags You Need to Know (for now)."](../assets/the-only-tags-that-you-need-to-know-for-now.pdf)

### Metadata Tags

- `<html>` - creates the "root" of the document
- `<head>` - contains extra information for the browser that doesn't appear on the page
- `<title>` - title of the page, which will appear in the browser tab and in search results
- `<link>` - used to link to a separate CSS file
- `<body>` - container for the content that will be visible on the page

**Metadata** tags operate "behind the scenes" to tell the browser about the page's content and some of the required assets, like CSS, JavaScript, and font files. It may be helpful to remember that these tags _should not_ contain any content that will be visible on the page, such as headings, paragraphs, or images.

When working in CodePen, you will never actually see these metadata tags. CodePen's simplified editor interface keeps them in the background.

For VS Code, they have been created for you in the project templates. When starting an HTML document from scratch in VS Code, these tags are all created using an autocomplete command (typing `!`, then pressing the tab key).

In class projects, you will usually only need to modify metadata tags when importing fonts or icon packs via `<link>` or `<script>` tags.

### Content Tags

- `<h1>`...`<h6>` - headings and subheadings
- `<p>` - paragraph
- `<a>` - link
- `<ol>` - ordered list (numbered)
- `<ul>` - unordered list (bullet points)
- `<li>` - list item (used inside `<ol>` and `<ul>`)
- `<span>` - generic inline element
- `<img>` - image
- `<figcaption>` - figure caption (used inside `<figure>`)

**Content** tags are the ones that you fill with text and image content---plain and simple! The different types of content tags simply define the role of the content and, in some cases, provide default styling (e.g., larger bold text for headings, bullet points for lists, etc.).

### Layout Tags

- `<header>` - header of the page
- `<main>` - main content of the page
- `<footer>` - footer of the page
- `<nav>` - used for major navigational elements (e.g., links to other pages on the same site)
- `<article>` - a standalone piece of content
- `<section>` - a section of content
- `<div>` - generic block element
- `<figure>` - used to pair an `<img>` with a `<figcaption>`

**Layout** tags are used to group related content together and describe the overall structure of a document. They usually wrap one or more content elements (and sometimes other layout elements). These tags _do not_ control how things look on the page (that is handled by CSS). Rather, they describe what the different parts of the page _are_.

You can think of layout tags as defining "containers" to be filled with content elements.

**Note**: `<figure>` and `<figcaption>` do not appear in Kevin Powell's document, but they are included here because they are especially useful for pairing images with captions.
