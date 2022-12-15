There are three kind of way you can read array buffer,
### 1. typed array

with typedArray like Int8Array(), you can read with index at certain position muliple of 1 byte where as with Float32Arraay() you can only read with position multiple of 4 bytes and
can only read 4 bytes. This is view which is not flexible and reason is that it read based on the index.

### 2. Dataview

Dataview is intended for scenario where you need a flexible array buffer and need to read variable widths and from positions in the buffer.

Example int32 index only point to memory location divisble y 4 whereas Dataview can read from anywhere.

```javascript
let buffer = reader.result // you got the buffer
let view = new Int8Buffer(buffer) // change array buffer into view that we can access by index
console.log(view[0])

//with dataview

console.log(new DataView(buffer).getInt8(0))
```

### 3. Shared Buffer:

https://www.youtube.com/watch?v=AVVdon6X9AA&ab_channel=codedamn

this is to share data or variable between multiple worker by post message 
