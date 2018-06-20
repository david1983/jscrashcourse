# react and JSX

JavaScript XML is a syntax extension to JavaScript. It produces react elements and it is very similar to HTML

```javascript
import React from 'react';
import ReactDOM from 'react-dom';

const TestComponent = props => (<div>Hello {props.name}</div>;)

const App = props => (
  <div>
    <TestComponent name="Davide" />
  </div>
);

ReactDOM.render(<App />, document.getElementById('root'));
```
