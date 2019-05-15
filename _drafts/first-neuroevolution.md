---
layout: post
title: "My first Neural Network with Neuroevolution"
tag: [neural networks, p5.js]
---

This project represents my first solo-flight in the world of machine learning. And a bumpy flight it was.

The project can be broken up into some parts:
* Build a virtual environment for the AI to lean in - essentially: _build a simple game_.
* Give the AI agency over a player in the game.

Taking inspiration from so many flash games of the 2000's, I created a simple defense-game environment - an invader attempts to cross the screen and the player tries to gun them down.

<!-- Image of the most basic game environment -->
*Amazing*.


* shoots straight up
* add reward for how early ufo destroyed - trains slowly
* add reward for near misses to encourage faster training - now misses on purpose



`gun.score += 1000`
`gun.score += 5 * map(planes[j].x,0,width,200,0) + 120;`
`gun.score += map(gun.projs[i].minDistance,0,120,120,0, true);`
