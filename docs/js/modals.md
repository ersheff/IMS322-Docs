---
title: Modals
---

A modal is a pop-up that appears on top of the current page and takes priority, meaning that it prevents interaction with the underlying content until it is submitted or closed.

## The `<dialog>` element

Designing and implementing modals recently became much easier with changes to the standard `<dialog>` element. It now includes default properties and methods that make it fairly easy to use and customize, especially for gathering user-submitted information.

The `<dialog>` element can be styled like any other element, including `border`, `background-color`, `box-shadow`, and more. The `::backdrop` pseudo-element selects the backdrop displayed behind a modal while it is open. Modals can be displayed and dismissed using the `showModal()` and `close()` methods, respectively.

Typically, `<form>` elements have a default behavior when submitted that requires additional server infrastructure to receive and process data - this is why you may have seen an error when clicking "Submit" in previous reading examples. However, when put in a modal with the attribute `method="dialog"`, the default `<form>` behavior is blocked, values from inputs in the form can be referenced locally with JavaScript, and the modal will close automatically upon submission.

<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="vYPByZL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPByZL">
  Modals (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
