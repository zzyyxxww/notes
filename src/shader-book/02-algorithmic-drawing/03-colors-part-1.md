
# Colors Part 1

`vec4` has an alias for xyzw called rgba.

Another feature of GLSL is that the properties can be combined in any order.
This is called **swizzle**.

```
vec3 yellow, magenta, green;

// Making Yellow
yellow.rg = vec2(1.0);  // Assigning 1. to red and green channels
yellow[2] = 0.0;        // Assigning 0. to blue channel

// Making Magenta
magenta = yellow.rbg;   // Assign the channels with green and blue swapped

// Making Green
green.rgb = yellow.bgb; // Assign the blue channel of Yellow (0) to red and blue channels
```

You might not be used to to pick colors with numbers, it can be very conterintuive.
Some software, like spectrum, generate templates that you can easily use in glsl code.
