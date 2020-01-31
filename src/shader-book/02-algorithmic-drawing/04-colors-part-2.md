
# Colors Part 2

The `mix()` functions lets you mix two values in percentages.

(The book then asks for ways to draw some things.
I'm shy of even trying those because I will feel that I'm doing something ugly)

## HSB

Hue, Saturation and Brightness (or Value) is a more intuitive organization of colors. 

Two functions to translate between hsb and rgb are provided.

Then, a bunch of geometric functions are provided (namely, length(), distance(), dot(), cross, normalize(), faceforward(), reflect() and refract(). Also GLSL has special vector relational functions such as: lessThan(), lessThanEqual(), greaterThan(), greaterThanEqual(), equal() and notEqual())

Then the author shows some drawings from Josef Albers' book Interaction of Color, and recreate them as shaders (these have their own solution, so they could be used).

## Argument qualifiers

Basically, depending on the qualifier what the effect it has on the argument:

* `in` makes it read-only
* `out` makes it write-only
* `inout` is read-write (similar to passing by reference)
