### react components

Components in React are reusable pieces of code.

- a component can be stateless or stateful
- a stateful component has a series of lifecycle events
- a stateful component act as a function that takes props and returns a react element

```javascript
import React,{Component} from 'react';
import ReactDOM from 'react-dom';

// this is a steless component
const TestComponent = props => (<div>Hello {props.name}</div>;)
// this is a stateful component (the state has not been defined ... yet)
class App extends Component{
  render(){
    return <div>
      <TestComponent name="Davide" />
    </div>
  }
}

ReactDOM.render(<App />, document.getElementById('root'));
```
