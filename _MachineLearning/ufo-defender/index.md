---
title: UFO Defender
layout: page
thumbnail: screenshot.png
tagline: Defending Earth with neuroevolution
sort-key: 100
meta-title: UFO Defender - Neuroevolution
meta-description: Defending Earth with neuroevolution
meta-image: screenshot.png
tags: [neural, networks, p5.js, javascript]
code-source: https://github.com/michaelruppe/ml-experiments/tree/master/ufo-defender
---

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/p5.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/addons/p5.dom.min.js"></script>
<script src="sketch.js"></script>
<script src="gun.js"></script>
<script src="projectile.js"></script>
<script src="plane.js"></script>
<script src="ga.js"></script>
<script src="libraries/nn.js"></script>
<script src="libraries/matrix.js"></script>

Here's my spin on the machine-learning right-of-passage: Building a flappy bird clone.

**Apologies**: The script renders poorly (the controls are offscreen!) using jekyll templating. This problem does not occur on the [original project page](https://michaelruppe.github.io/ml-experiments/ufo-defender/index.html).

<div>
  <div id="sketch-holder"></div>
</div>
<div id="gen-holder"></div>
<div id="score-holder"></div>

## What's going on here?

A population of guns is trialled one-by-one. Each gun is controlled by a (randomly initialised) neural network.
If a gun lets some UFOs through, it fails and the next one takes its place. Once all the guns have been trialled,
a new generation is created. Higher scoring guns are more likely to pass their neural network on to the next generation.
Small mutations occur between generations.
Performance is measured by how many UFOs are destroyed and how quickly. Near misses are also rewarded to encourage faster
training during early generations.

- train mode: perform neuro-evolution on the guns
- best so far: display the best-performing gun that has been trained yet.
- pretrained model: deploy a very well-performing neural network that has already been trained.
- manual: take control of the gun yourself!
