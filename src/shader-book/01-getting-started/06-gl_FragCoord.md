
# gl_FragCoord

GLSL gives us a default input `vec4 gl_FragCoord` which holds the screen coordinates
of the *pixel* or *screen fragment* of the current thread.

`gl_FragCoord` is not an uniform (it is different from thread to thread), but a **varying**.

It is possible to normalize `gl_FragCoord` by diving it with the resolution uniform.  
This lets us map to colors in an easier way.
