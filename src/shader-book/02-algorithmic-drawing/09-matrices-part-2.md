
# Matrices Part 2

## Scale

Objects can also be scaled with matrices.

This function can be used:

```
mat2 scale(vec2 _scale){
    return mat2(_scale.x,0.0,
                0.0,_scale.y);
}
```

Again, this function pivots at (0,0), so by default it scales from (0,0).
If we want to scale from the center, we need to move center to (0,0), scale and move back.
