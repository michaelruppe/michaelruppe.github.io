---
title: Drift Car
layout: post
date: 2019-05-17
thumbnail: demo/screenshot.png
tagline: A car class in javascript with simple skidding physics
meta-title: Drift Car
meta-description: A car class in javascript with simple skidding physics
meta-image: demo/screenshot.png
tags: [physics, car, drifting, friction, p5.js, javascript]
code-source: https://github.com/michaelruppe/drift-car/tree/master/
permalink: /MiscProjects/drift-car/
---
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.7.3/p5.js"></script>
<script src="sketch.js"></script>
<script src="car.js"></script>

**Control the car with arrow-keys**

<div id="sketch-holder"></div>


Seems like a lot of ML projects centre around self-driving cars in top-down game environments. This is a car class that attempts to capture some realistic steering behaviour. Give it a go! The car turns red when it loses traction, indicating some skidding/drifting. The car turns white when it regains traction and steers "normally." Obviously it's still not a very realistic model (the car can spin in place!) but I think it's useful for a bit of fun.

### Using the class (p5.js)
Copy `car.js` into your p5 project directory and create a car in your script:
```javascript
car = new Car(); // Initialises car in the middle of the canvas.
// OR
car = new Car(x, y, angle); // Initialises car with desired location, angle
```
you need to call the following once every loop through `draw()` .
```javascript
car.update(); // simulates the car
car.show();   // renders the car
```

If you want to change how the car is controlled (eg. by some neural network) you will have to modify the `update()` function in `car.js`
