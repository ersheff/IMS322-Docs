# Objects

When working with HTML elements in JavaScript, you are often using or changing the object's _properties_ and _methods_.

```js
// example properties
textDisplay.innerText = "Hello!";
headshotImage.src = "images/headshot.jpeg";

// example methods
audioFile.play();
compass.style.setProperty("font-size", "2rem");
```

Remember that _properties_ are charactertistcs about the object (often corresponding to HTML attrbutes), while _methods_ are actions that the object can perform.

You can also define your own objects to organize and provide context for data about something. For example, if you were describing Miami University, you might want to include information about the type of institution, when it was established, and where it is located. The _object_ data type stores these as _key/value_ pairs.

```js
// format is key: value

const miamiOh = {
  type: "Public", // type is key, "Public" is value
  established: 1809, // established is key, 1809 is value
  location: "Oxford, OH", // location is key, "Oxford, OH" is value
};
```

The key provides context for the values. You can reference the individual values of an object using _dot notation_.

```js
miamiOh.type; // returns "Public"
miamiOh.established; // returns 1809
```

You have already been using dot notation to interface with objects in JavaScript.

```js
// the getElementById() method of the document object
document.getElementById("text-input");

// the innerText property of the textInput object
textInput.innerText;
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="vYPByeL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPByeL">
  Objects (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
