### stateful components

```javascript

class App extends Component{
  constructor(){
    this.state = {
      name: "Davide"
    }
  }
  // lifecycle methods
  componentWillReceiveProps(nextProps){} //called when the props have changed and when this is not an initial rendering 
  shouldComponentUpdate(nextProps, nextState){} // allows to define if a component should update, triggered before componentWillUpdate()
  componentWillUpdate(nextProps, nextState){} // before render() on updates
  componentDidUpdate(prevPros, nextState){} // after render() on updates
  componentWillMount(){} // before render() on mount
  componentDidMount(){} // after render() on mount
  componentWillUnmount(){} // before unmount
  componentDidCatch(){} //called when there is an error during rendering, in a lifecycle method, or in the constructor of any child component.

  render(){
    return <div>
      <input type="text" onChange={e => this.setState({name: e.target.value})}/>
      <TestComponent name={this.state.name} />
    </div>
  }
}

```
