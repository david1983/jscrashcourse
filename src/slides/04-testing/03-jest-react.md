## Jest - React 

```javascript
import React from 'react'
import renderer from 'react-test-renderer'
import Dashboard from './Dashboard'
import { MemoryRouter, Route, Switch, Redirect } from 'react-router-dom'
import { Provider } from 'mobx-react'
import stores from '../../stores/Stores'

describe('Full', () => {
  it('should render the Dashboard component', () => {
    const component = renderer.create(
      <Provider {...stores}>
        <MemoryRouter>
          <Dashboard />
        </MemoryRouter>
      </Provider>
    )
    const tree = component.toJSON()
    const input = tree.children[3]
    input.props.onChange({ target: { value: 'testVal' } })

    expect(tree.props.className).toBe('animated fadeIn')
    expect(stores.Settings.observableTest).toBe('testVal')
  })
})

```