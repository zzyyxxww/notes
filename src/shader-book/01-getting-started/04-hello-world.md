
# Hello world

GPU architecture can compile and replace shaders *on the fly*.

## Characteristics of shaders

* There's a single `main` function.
* A final pixel color is assigned to the reserved global variable `gl_FragColor`
* GLSL has built in **variables**, **functions** and **types**
* gl_FragColor is a vector for the RED, GREEN, BLUE and ALPHA channels
* Values are normalized (they go from 0 to 1) which is easier for computations
* C macros can be used, like in the code it sets the level of precision
* In shaders, floats are vital, so the level of precision is also crucial
* Precision can be set with the statement `precision <prec> float;` where `<prec>` can be `lowp`, `mediump` or `highp`
* GLSL specs don't guarantee that vars will be automatically casted. Because of that, we need to make all numbers floats by putting a dot after each number
