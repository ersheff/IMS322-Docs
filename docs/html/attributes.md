# Attributes

Some HTML elements benefit from additional information in the form of **attributes**. In some cases, like `<img>` and `<a>`, the attributes are required for the elements to function as expected---the image file to load (`src`) or URL to visit (`href`) when clicked, respectively.

Attributes are placed inside the opening tag of an element, like this:

```html
<a href="https://miamioh.edu">Link to Miami University's site</a>

<img src="https://picsum.photos/id/237" alt="cute black dog" />
```

Like elements themselves, there are dozens of valid attributes, as seen on [this MDN Web Docs reference page](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Attributes). However, you will likely only need to use the following attributes in your projects throughout the semester:

- `alt`: alternate text for an `<img>` element (important for accessibility and screen readers, and displayed if the image file does not load)
- `class`: used as a selector in CSS
- `href`: URL for `<a>` elements
- `id`: used to select an element in JavaScript
- `src`: path to the image file for an `<img>` element
