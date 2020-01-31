
```
float r = length(pos)*4.0;
float a = atan(pos.y,pos.x);
// function
color = vec3( 1.-smoothstep(f,f+0.02,r) );
```

* helix: `float f = cos(a*3.)`;
* flower1: `float f = abs(cos(a*3.))*1.`;
* flower2: `float f = abs(cos(a*2.5))*.5+.3;`
* crystal: `float f = abs(cos(a*12.)*sin(a*3.))*.8+.1;`
* explosive mine: `float f = smoothstep(-.5,1., cos(a*10.))*0.2+0.5;`
