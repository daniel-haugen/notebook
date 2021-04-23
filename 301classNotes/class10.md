# 301 Day 8
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [Javascript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
- [JS Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
- [JS Error reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

## JS Call Stack

>At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

Stack overflow occurs when a recursive function is called witihout an exit point. The stack is single-threaded operating with LIFO principles. 

## Throwing Errors
standard try / catch method for catching errors:
```javascript
(function testing(){
  function add(a, b) {
    try {
      var result = a + b
      return result.split('')
    } catch (error) {
      console.error('add went wrong ->', error)
      return [] // default value
    }
  }
  var stringResult = add("1", "2")
  var numberResult = add(1, 2)
})()
```
