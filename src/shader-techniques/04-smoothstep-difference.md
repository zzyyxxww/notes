
# Smoothstep difference

By substracting one smoothstep to another you can achieve a off/on/off sequence.

The way it works is that at first both `smoothstep`s result in 0, so 0-0 is 0.

Then, one of the smoothsteps start becoming a 1, but the second is still 0.

Later and from then on, the second smoothstep also becomes 1, so their substraction becomes 0.
