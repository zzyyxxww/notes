
# step

```
float step(float edge, float x)  
vec2 step(vec2 edge, vec2 x)  
vec3 step(vec3 edge, vec3 x)  
vec4 step(vec4 edge, vec4 x)

vec2 step(float edge, vec2 x)  
vec3 step(float edge, vec3 x)  
vec4 step(float edge, vec4 x)
```

If x < edge returns 0
Else returns 1

For element i of the return value, 0.0 is returned if x[i] < edge[i], and 1.0 is returned otherwise.

