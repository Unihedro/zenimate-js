**zenimate-js** (zen animate javascript) is an animation toolkit for setting up animated elements, animated backgrounds on the site or behind content spans with object-oriented code. Except for animating elements, only Javascript is required and CSS knowledge is not mandatory.

It is currently in development.

#### Roadmap (How it will work)

Animating the `body` element with handled `element.style`, kind of like injected CSS:

```js
var variating = zenimate.variating; // An alternate way is to use 'with()'.

var preset = zenimate({
  // Give elements ever changing colors.
  color: variating("5s", "#ddd", "#fff"), // variating() == variating.byTime()
  // Change the background color with delayed transition when scrolling.
  background: variating.byMotion("vertical scroll repeat 20px transition .1s",
      "rgba(237, 67, 107, .5)", "rgba(59, 119, 176, .3)", "rgba(255, 222, 73, .8)")
  // Change the font size when clicked.
  font-size: variating.byMotion("onclick 1x transition .1s", ".8em", "1.2em");
});

preset.animateElement($("#content_box")); // jQuery usage, otherwise document.getElementById
```
