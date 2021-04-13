# 301 Prework
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
- [JS Arrow Function Intro](https://wesbos.com/arrow-functions)

## Arrow Functions


```javascript

// Updating to Arrow Functions

function sum (a,b) {
  return a + b
}

let sumArrow = (a,b) => a + b

function isPositive(number) {
  return number >= 0
}

let isPositiveArrow = number => number >= 0

function randomNumber() {
  return Math.random
}

let randomArrow = () => Math.random 

document.addEventListener('click', function() {
  console.log('Click')
})

document.addEventListener('click', () => console.log('Click'))



// Arrow Functions change the meaning of the This keyword


```


## this Keyword


