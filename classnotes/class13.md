# 201 Day 13
[Back to Table of Contents](../reading|notes.md)<br/>

#### Today's Reading:<br/>

**Article**: 
- [Local Storage](http://diveinto.html5doctor.com/storage.html)

## Local Storage

### What is HTML5 Storage?

- Storing key/value pairs locally.
- Used for cookies
- Access through `localStorage` object on the global `window` object.
- Always check if the user browser supports it.

```javascript
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```
##### Data stored in the localStorage will be returned as a string.

- getItem
- setItem
- clear
- removeItem

### Storage Event Object

| Property | Type |
|--|--|
| key | string |
| oldValue | any |
| newValue | any |
| url | string |

