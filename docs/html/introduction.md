# HTML

**HTML** stands for "HyperText Markup Language." It is the standard language for describing and structuring the content of a web page.

Consider how a paper or article is structured. Let's use the Wikipedia entry for [HTML](https://en.wikipedia.org/wiki/HTML) as an example.

- The main **heading** of the page, _HTML_, appears in large bold text at the very top.
- **Subheadings**, like _History_, _Markup_, _Semantic HTML_, and _Delivery_, organize the page into logical sections. These subheadings are also larger than standard text, but not as large as the main heading.
- These sections also have their own subheadings that serve a similar purpose, organizing the content into even smaller logical subsections. For example, in _History_, there are subheadings for _Development_, _HTML version timeline_, and _HTML draft version timeline_.
- Under headings and subheadings, standard text is separated into **paragraphs**.
- There are occasional images, graphics, lists, quotes, and links throughout the article.

In HTML, these discrete units---headings, subheadings, paragraphs, links, etc.---are called **elements**. You define the type of element by surrounding its content with a pair of **tags**. For the text-based elements that we've covered so far, there are up to 6 levels of headings that use tags `<h1>` through `<h6>`, and paragraphs that use `<p>` tags (with no numbered levels).

```html
I am some text. However, since I don't have any tags, I don't have a role in an
HTML document.

<p>
  I am also some text, but now I'm a paragraph element because of the p tags.
</p>

<h1>I am the top-level heading and typically appear only once on a page.</h1>
<h2>I am a second-level subheading. You can use me as many times as needed.</h2>
<h3>I am a third-level subheading. Ditto.</h3>
```

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="XJKRvLB" data-pen-title="HTML Introduction (IMS322 Docs)" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
      <span>See the Pen <a href="https://codepen.io/ersheff/pen/XJKRvLB">
  HTML Introduction (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Although some elements, such as headings, have a default appearance that is different from standard text, HTML does _not_ otherwise describe a page's styling or layout. In fact, the very first web page, which can still be viewed [here](https://info.cern.ch/hypertext/WWW/TheProject.html), was created using only HTML tags.

<script async src="https://public.codepenassets.com/embed/index.js"></script>
