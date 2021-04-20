# 301 Day 6
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [Intro to Node.js](https://reactjs.org/docs/thinking-in-react.html)
- [6 Reasons for Pair Programming]()
- [Geocoding API Docs]()
- [Axios Docs]()
- [MDN Async and Await]()

## Intro to Node.js

- use a node version manager

### NodePackageManager
You can either install node packages locally or globally.

1. Locally - `npm init -y` will create a `package.json` dependency file and `npm install [package] --save` will install a package locally and add to the dependency list.
2. Globally - `npm install -g [package]`

Example HTTP server starter code:
```javascript
const http = require('http');

http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello, World!');
}).listen(3000);

console.log('Server running on http://localhost:3000');
  ```

1. Create node's http module
2. createServer method to create a server object, which is passed an arrow function.
3. the arrow function is invoked for every new connection made to the server.
4. the function contains `request` and `response` arguments. 
5. Finally, tell the server to listen to incoming requests on port 3000.  