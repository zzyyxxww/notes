
# Debugging

In shaders, there isn't too many resources for debugging, other than
assigning strong colors to variables and trying to make sense of them.

Coding GLSL is similar to putting ships inside bottles.
It's hard, beautiful and gratifying.

## Exercises

* Can you tell where the coordinate (0.0, 0.0) is?

(I can see that the origin is at the lower left corner of the screen)

* What about (1.0, 0.0), (0.0, 1.0), (0.5, 0.5) and (1.0, 1.0)?

In order, the lower right corner, the upper left corner, the middle of the screen, and the upper right corner of the screen.

* Can you figure out how to use `u_mouse` knowing that the values are in pixels and NOT normalized values? Can you use it to move colors around?

`u_mouse` can be divide by `u_resolution` to get it normalized.
