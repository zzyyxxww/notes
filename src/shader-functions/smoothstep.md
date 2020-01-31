
# smoothstep

```
smoothstep(edge0, edge1, x) 
```

Smoothstep is like a ratio'd smoothed out clamp. 

This is one implementation
```
genType t;  /* Or genDType t; */
t = clamp((x - edge0) / (edge1 - edge0), 0.0, 1.0);
return t * t * (3.0 - 2.0 * t);
```

`smoothstep(.5, .52, .5) = 0`
`smoothstep(.5, .52, .51) = 0.5`
`smoothstep(.5, .52, .52) = 1`

Also, approaching the edges has polynomic behaviour, which is why it's called smooth.
