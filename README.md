This is a fork of [tags-input](https://github.com/developit/tags-input)
=======================================================================

It adds a "remove" button to the left side of each tag.

Examples
========

It's easy to use! In addition to the example code, you'll also need to
include `tags-input.css` - I didn't bundle it because that's a bit gross.

**CommonJS:**

```js
var tagsInput = require('tags-input');

// create a new tag input:
var tags = document.createElement('input');
tags.setAttribute('type', 'tags');
tagsInput(tags);
document.body.appendChild(tags);

// enhance an existing input:
tagsInput(document.querySelector('input[type="tags"]'));

// or just enhance all tag inputs on the page:
[].forEach.call(document.querySelectorAll('input[type="tags"]'), tagsInput);
```

**HTML Example:**

```html
<link rel="stylesheet" href="tags-input.css">
<script src="tags-input.js"></script>

<form>
	<label>
		Add some
		<input name="hashtags" type="tags" pattern="^#" placeholder="#hashtags">
	</label>
</form>

<script>[].forEach.call(document.querySelectorAll('input[type="tags"]'), tagsInput);</script>
```
