---
layout: post
title: "Realistic car physics - drifting"
tag: [p5.js, physics, car, drifting]
---

I decided to try coding a vehicle that exhibits more realistic steering and traction, rather than the standard, slidey-spaceships I usually go for.

<!-- Include picture -->

so lets start from the slidey spaceship I mentioned:
<!-- An example of a slidey spaceship -->
This is a simple example where some friction acts on the vehicle in the opposite direciton to the velocity.

Working off the idea of separating sideways- from axial-friction requires us to not think of the vehicle velocity in terms of the world-reference-frame, but the vehicle reference frame.

<!-- diagram of velocity in vehicle frame -->

Now we can have separate friction for forward-backward (eg, drag and braking) and sideways.
But that's not quite enough.

Switch dynamic and static
