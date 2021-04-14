# 301 Day 1
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>
- [Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
- [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)
- [Declaring a Winner](https://reactjs.org/tutorial/tutorial.html)
- [How to Use the Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)


## Lifting State Up

1. Create BoilingVerdit component. 
```javascript
function BoilingVerdict(props) {
  if (props.celsius >= 100) {
    return <p>The water would boil.</p>;
  }
  return <p>The water would not boil.</p>;
}
```
2. Create a Calculator component that renders an `<input>` and keeps its value in `this.state.temperature`.

```javascript
class Calculator extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
    this.state = {temperature: ''};
  }

  handleChange(e) {
    this.setState({temperature: e.target.value});
  }

  render() {
    const temperature = this.state.temperature;
    return (
      <fieldset>
        <legend>Enter temperature in Celsius:</legend>
        <input
          value={temperature}
          onChange={this.handleChange} />
        <BoilingVerdict
          celsius={parseFloat(temperature)} />
      </fieldset>
    );
  }
}
```
3. Remove the local state from the TemperatureInput and move it into the Calculator


> Instead of trying to sync the state between different components, you should rely on the top-down data flow.


## Lists and Keys

Let’s assign a key to our list items inside numbers.map() and fix the missing key issue.
```javascript
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

- Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity
- The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys
- Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique. We can use the same keys when we produce two different arrays


## Spread Operator

##### Spread syntax spreads the array into seperate arguments and it's incredibly useful for:

- Copying an array
- Concatenating or combining arrays
- Using Math functions
- Using an array as arguments
- Adding an item to a list
- Adding to state in React
- Combining objects
- Converting NodeList to an array