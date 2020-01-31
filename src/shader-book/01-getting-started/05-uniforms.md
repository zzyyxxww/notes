
# Uniforms

It is possible to send data from the CPU to each shader instructions in the GPU.
These are called **uniforms**, because they are the same across threads.

These are also **read-only**.

Uniforms that are introduced are:
* `uniform vec2 u_resolution;` the size of the canvas (width, height)
* `uniform vec2 u_mouse;` the position of the mouse (x, y)
* `uniform float u_time;` time since load

(The book then mentions the existence of several angle, trig and exponential functions)
