---
title: Objects
---

We recently learned that [arrays](arrays) are useful for storing sequences of related data, such as GPS coordinates, enrollment figures, names of the months in a year, etc.

```js
const miamiCoordinates = [39.511047326918174, -84.72907894440365];

const miamiEnrollment = [21627, 20613, 20784, 20384, 20036];

const months = ["January", "February", "March", "April", "May"]; // etc
```

The type of data and the relationship that those items have to each other suggest that an array is a suitable way to organize and store those items. They fall into a series and can be easily referenced using only the index number (e.g. `months[0]` for the first month of the year, `months[1]` for the second month of the year, etc).

You may want to store multiple pieces of data about a subject that don't necessarily belong in a sequence. For example, general information about Miami University looks kind of strange in an array.

```js
const miamiOh = ["Public", 1809, "Oxford, OH", "Division I"];
```

While you can likely guess what each item in that array means, it isn't the most obvious or meaningful way to store that specific information. Also, it can become confusing to refer to non-sequential data by index number.

```js
miamiOh[2]; // returns "Oxford, OH" - but what does that mean?
```

For cases like this, the _object_ data type is a better fit. Objects store data as _key/value_ pairs.

```js
// format is key: value

const miamiOh = {
  type: "Public", // type is key, "Public" is value
  established: 1809, // established is key, 1809 is value
  location: "Oxford, OH", // location is key, "Oxford, OH" is value
  ncaa: "Division I" // ncaa is key, "Division I" is value
};
```

The key provides context for the values in a way that the generic index numbers of an array do not. You can reference the individual values of an object using _dot notation_.

```js
miamiOh.type; // returns "Public"
miamiOh.established; // returns 1809
```

You have already been interfacing with objects in the JavaScript code that you've been developing. Essentially, any time you have written something using dot notation, that is a reference to a property (characteristic) or method (action it can perform) of an object.

```js
// the querySelector() method of the document object
document.querySelector("text-input");

// the innerText property of the textInput object
textInput.innerText;
```

<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="vYPByeL" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPByeL">
  Objects (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
