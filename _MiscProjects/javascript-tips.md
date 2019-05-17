---
title: p5.js and javascript tips
layout: post
date: 2019-05-17
thumbnail: demo/screenshot.png
tagline: Useful tips for p5.js workflow
meta-title: p5.js and javascript tips
meta-description: Useful tips for p5.js workflow
meta-image:
tags: [tutorial, tips, p5.js, javascript]
---

# Basics

### Quickstart: Include p5.js - base and libraries

`<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/p5.js"></script>`

Use the Content Distribution Network version instead of including local files. This stops you having a thousand instances of p5.js and its libraries on your computer.

For a library, eg. `p5.dom.js`:

`<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/addons/p5.dom.min.js"></script>`

Note: at the time of writing, 0.7.3 was the most recent version. Update these numbers as necessary. All old versions are served as well, so you don't need to worry about your script breaking when a new version is released.


# Interactivity

### Prevent arrow keys and spacebar from scrolling the page
This is useful to stop the page moving around when you're trying to interact with your game.

Add the following to your main .js file:
```javascript
// Prevent arrow-keys and spacebar from scrolling the page.
window.addEventListener("keydown", (key) => {
    // space and arrow keys
    if([32, 37, 38, 39, 40].indexOf(key.keyCode) > -1) {
        key.preventDefault();
    }
}, false);
```
