# 201 Day 10
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>
**Javascript & Jquery by John Duckett** - *Chapter 10 - Error Handling*

## Debugging Javascript

### Error Objects
- SyntaxError
- ReferenceError
- TypeError
- RangeError
- EvalError
- URIError
- Error
- NaN

You can create breakpoints in your code by adding a `debugger` on the line you want to stop at.

### Exceptions

```javascript
try {
  //try to execute this code.
} catch (exception) {
  //if there is an exception, run this code.
} finally {
  //run this code.
}
```

To throw your own errorL `throw new Error('message');`