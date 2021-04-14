# 301 Day 1
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:
- [Intro to React](https://reactjs.org/tutorial/tutorial.html)
- [Hello World](https://reactjs.org/docs/hello-world.html)
- [Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
- [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
- [Components and Props](https://reactjs.org/docs/components-and-props.html)

## Intro to React

- React is a declarative, efficient and flexible Javascript Library for building user interfaces.
- React has a multiple types of components
  - React.Component

>We use components to tell React what we want to see on the screen. When our data changes, React will efficiently update and re-render our components. [^[source](https://reactjs.org/tutorial/tutorial.html)]

### Render
The `render()` method returns a React element.

```javascript
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}
```

### JSX
- JSX is a special syntax used in React.js files which is transformed at build time. 
- You can put any Javascript expressions within braces inside JSX. 
- Each React element is a JS object that you can store in a variable.

Built-in DOM Components - div, li, h2
Custom React Components - `<componentName />`

### State

##### To remember things, React components use state

State Example with the Tic Tac Toe Game
1. Add a constructor to the class to initialize the state.
2. Always call `super()` when defining the constructor of a subclass. All React components that have a constructor should start with a `super(props)` call.

```javascript
class Square extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: null,
    };
  }
```

3. Next you change the `render` mehtod to display the state's value after being clicked. This tells React ot re-render the square whenever the component is clicked.

```javascript 
render() {
    return (
      <button
        className="square"
        onClick={() => this.setState({value: 'X'})}
      >
        {this.state.value}
      </button>
    );
  }
```

### Function Components
>In React, function components are a simpler way to write components that only contain a `render` method and **don't have their own state.**

- `this.props` becomes just `props`
- `onClick={()=> this.props.onClick()}` becomes `onClick={props.onClick}`

```javascript
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}
```

## Rendering

To render a React element into a root DOM node, pass both to ReactDOM.render():
```javascript
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```

In the following code example, we're re-rendering a component every second.

```javascript 
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```
