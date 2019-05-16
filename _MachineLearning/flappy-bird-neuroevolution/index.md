---
title: Fearless Flappers
layout: page
thumbnail: thumbnail.png
tagline: Neuroevolution of a flappy-bird
sort-key: 100
meta-title: Flappy Bird - Neuroevolution
meta-description: Neuroevolution of a flappy-bird
meta-image: screenshot.png
tags: [neural, networks, p5.js, javascript]
code-source: https://github.com/michaelruppe/ml-experiments/tree/master/flappy-bird-neuroevolution/toy
permalink: /MachineLearning/flappy-bird-neuroevolution
---

Here's my spin on the machine-learning right-of-passage: Building a flappy bird clone.

<div id="sketch-holder"></div>
<p>Time-Warp: <div id="slider-holder"></div></p>
<div id="gen-holder"></div>
<div id="score-holder"></div>

## What's going on here?

A population of birds tries to navigate the course. The more successful birds
are more likely to reproduce. Small mutations affect the behaviour of offspring.

Each bird is controlled by a neural-network which has some information about the virtual world -
like the bird's position and distance-to-wall, for example. The neural-net can only control the bird's flapping.
Importantly, the neural-nets have no idea about the physical meaning of the inputs - it has no concept of distance
or speed.

### A diagram of inputs and outputs for the neural network

![Schematic of inputs to the neural network](art/flappy-diagram.jpg)



<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/p5.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/addons/p5.dom.min.js"></script>
<script src="sketch.js"></script>
<script src="bird.js"></script>
<script src="pipe.js"></script>
<script src="ga.js"></script>
<script src="libraries/nn.js"></script>
<script src="libraries/matrix.js"></script>
