### mobx - core concepts

2. create a view that responds to changes in the state

```javascript
import {observer} from 'mobx-react'
import appState from "./state.js"

@observer
class TimerView extends React.Component {
    render() {
        return <button onClick={() => this.props.appState.resetTimer()}>
                Seconds passed: {this.props.appState.timer}
            </button>
    }
}

ReactDOM.render(<TimerView appState={appState} />, document.body)
```


