---
title: Modals
---

A modal is a pop-up that appears on top of the current page, taking priority and preventing interaction with underlying content in the `<body>` until it is either submitted or closed.

## The `<dialog>` element

Designing and implementing modals is straightforward with the `<dialog>` element. It includes attributes, properties, and methods that make it easy to use and customize as a modal, especially for collecting user-submitted information.

The `<dialog>` element can be styled like any other HTML element using properties like `border`, `background-color`, `box-shadow`, and more. Modals can be displayed and dismissed using the `showModal()` and `close()` methods, respectively.

When a `<form>` is put in a modal and given the attribute `method="dialog"`, the modal will close automatically upon form submission and fire a "submit" event.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="vYPByZL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPByZL">
  Modals (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
