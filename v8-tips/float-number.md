# Float Number are expensive

V8 uses tagging to represent values efficiently when types can change.

V8 infers from the values that you use what number type you are dealing with. Once V8 has made this inference, it uses tagging to represent values efficiently, because these types can change dynamically.

However, there is sometimes a cost to changing these type tags, so it's best to use number types consistently, and in general it is most optimal to use **31-bit signed integers** where appropriate.

```js
var i = 42  // this is a 31-bit signed integer (whole).
var j = 4.2 // this is a double-precision floating point number (float).
```

If you actually don't need the extra of information, avoid it.
