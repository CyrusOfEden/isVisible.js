isVisible.js
============

A quick JavaScript tool to check if an element is visible within the viewport.


Getting Started
---------------

Include `isvisible.js` in your page:
```html
<script src="/path/to/isvisible.js"></script>
```

If you're using jQuery, including `jquery.isvisible.js` after jQuery:
```html
<script src="/path/to/jquery.js"></script>
<script src="/path/to/jquery.isvisible.js"></script>
```


Checking An Element's Visibility
--------------------------------

In plain JavaScript, just provide `isElementVisible` with a single node:
```javascript
var awesomeThing = document.querySelector(".awesome-thing");
isElementVisible(awesemeThing); // returns true or false
```

If you're using jQuery, it couldn't be easier:
```javascript
$(".awesome-thing").isVisible(); // returns true or false
```

Options
-------

You can provide a second argument to `isElementVisible` to specify limitations with the following syntax:
```javascript
var awesomeThing = document.querySelector(".awesome-thing");
isElementVisible(awesomeThing, { top: 20, right: 20 }); // returns true or false
```

The above will only return `true` if the top edge of `.awesome-thing` more than 20px below the top of the window, and its right edge is more than 20px to the left of the right of the window.

With jQuery, just provide the `object` to `$.fn.isVisible`:
```javascript
$(".awesome-thing").isVisible({ top: 20, right: 20 }); // returns true or false
```;

Available options are `top`, `right`, `bottom`, and `left`.
