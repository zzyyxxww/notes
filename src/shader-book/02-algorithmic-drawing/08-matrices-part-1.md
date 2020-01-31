
# Matrices Part 1

## Translation

The trick to move some shapes is to move the coordinate system itself.
We do that my adding a vector to the st variable.

Try to recreate some motion and move the cross in the same way.

## Rotation

To rotate objects we also need to move the entire space system using a **matrix**.

Vectors can be multiplied by matrices following a precise set of rules to modify
the values of the vector in a particular way.

GLSL has 2, 3 and 4 dimensional matrices.  
Also supports matrix multiplication and an interesting matrix function (`matrixCompMult`).

Matrices can produce specific behaviours. For example, a matrix can translate a vector.

We can also use a matrix to rotate the coordinate system.

Rotation depends on a pivot. To rotate the system in $.5, .5$ we need to move the coordinates
to $0, 0$, rotate and move back.

This is a function to rotate
```
mat2 rotate2d(float _angle){
    return mat2(cos(_angle),-sin(_angle),
                sin(_angle),cos(_angle));
}
```

