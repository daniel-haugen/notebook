# 301 Day 1
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>


## React State and Lifecycle

- State is similar to props, but it is private and fully controlled by the component.

- Use setState() to render a component

- State updates may be asynchronous

## Conditional Rendering

```javascript
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}

function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}

ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,
  document.getElementById('root')
);
```


