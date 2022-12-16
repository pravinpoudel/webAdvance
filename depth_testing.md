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


![image](https://user-images.githubusercontent.com/11494733/207999943-32df5819-5688-4c6e-beaf-10baf2b87669.png)


![image](https://user-images.githubusercontent.com/11494733/208000087-6b2cf00b-62e8-41b0-8d8a-ab0e03b0c55e.png)

for frame buffer, 

render attachment is frame buffer where we use context to configure width and height of the frame buffer

1. get context
2. configure swap chain in the context
3. from that context, get the current view
4. pass it to color attachment in render pass descriptor which need color attachment and depth attachment
5. in that command/pass encoder, also give the viewport size

