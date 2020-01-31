
# Shapes Part 2

## Distance field

Apparently, distance fields cause perception of depth.

Since sqrt is computationally expensive, you can use this

```
float circle(in vec2 _st, in float _radius){
    vec2 dist = _st-vec2(0.5);
	return 1.-smoothstep(_radius-(_radius*0.),
                         _radius+(_radius*0.08),
                         dot(dist,dist)*4.0);
}
```


## Useful properties of a Distance Field

Distance fields can be used to draw almost everything.

The use of min, max and pow can be used to shape distance fields.
