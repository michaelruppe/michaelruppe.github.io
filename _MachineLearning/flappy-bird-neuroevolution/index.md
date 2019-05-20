---
title: Fearless Flappers
layout: page
date:
thumbnail: thumbnail.png
tagline: Neuroevolution of a flappy-bird
meta-title: Flappy Bird - Neuroevolution
meta-description: Neuroevolution of a flappy-bird
meta-image: screenshot.png
tags: [neural, networks, p5.js, javascript]
code-source: https://github.com/michaelruppe/ml-experiments/tree/master/flappy-bird-neuroevolution/toy
permalink: /MachineLearning/flappy-bird-neuroevolution/
---

Here's my spin on a modern rite-of-passage for beginners in machine learning: Building a flappy bird clone.

<div id="sketch-holder"></div>
<p>Time-Warp: <div id="slider-holder"></div></p>
<div id="gen-holder"></div>
<div id="score-holder"></div>


## What's going on here?

A population of birds tries to navigate the course. The more successful birds
are more likely to reproduce. Small mutations affect the behaviour of offspring.

First, the game environment was created. This is:

 - The physics that affect the bird - gravity and flap mechanics
 - The obstacles
 - Collision logic

Next, the neural network is given control of the gun, and fed information from the game enviroment.
The neural network is dense (fully-connected) and has:
 - 5 Inputs: Bird height & vertical speed, distance to the pipes, length of top & bottom pipe.
 - A single hidden layer with 8 neurons.
 - 1 Output: Flap.

The population is trialled all at the same time, and performance is measured by how many pixels the bird makes it to the right.

If a bird hits a pipe it is killed off, with its performance logged.
Better performing birds are more likely to pass their genetics (neural net) to the next generation, with small mutations.

#### A diagram of inputs and outputs for the neural network

![Schematic of inputs to the neural network](art/flappy-diagram.jpg)


<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/p5.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/addons/p5.dom.min.js"></script>
<script src="sketch.js"></script>
<script src="bird.js"></script>
<script src="pipe.js"></script>
<script src="ga.js"></script>
<script src="libraries/nn.js"></script>
<script src="libraries/matrix.js"></script>
