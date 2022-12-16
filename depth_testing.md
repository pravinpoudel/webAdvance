Depth testing is done after the fragment shader

```javascript
gl_FragCoord from vertex shader mean screen space coordiantes on the viewport defined by glViewport
x and y components of gl_FradCord represents fragment's screen space cordinates with (0, 0) mean the bottom-left corner.
This gl_FragCoord also contains a z-component which is the depth of the fragment. This z value is value compared to the depth buffer's content
```

Note: Most GPU now support early depth testing !!!

---------------------------------------------------------

### Fragment shaders are usually quite expensive so wherever we can avoid running them we should

#### Wikipedia:





