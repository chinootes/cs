![react lifecycle stages](lang.js.react.components.lifecycle.png)

1. **Mounting**: When an instance of a [[lang.js.react.components]] is created and inserted into the DOM
2. **Updating**: When component is re-rendered due to changes to props or state
3. **Unmounting**: When component is being removed from DOM
4. **Error Handling**: 

## Lifecycle methods

React offers several methods which are automatically called in different stages of lifecycle of a component.

### Mounting

- `constructor(props)`: 
    - Called: before component is mounted
    - Used for: initializing state, binding event handlers
- `static getDerivedStateFromProps(props, state)`: 
    - Called: right before rendering, both on the initial mount and on subsequent updates.
    - Used for: updating state based on props -> returned object is used to update state - `null` to update nothing. 
- `render()`: **Required**. Returns JSX to render.
- `componentDidMount()`: 
    - Called immediately after component is mounted.
    - Used for: making network requests, setting up subscriptions, interacting with DOM

### Updating

- `static getDerivedStateFromProps(props, state)`: 
    - Called: again before rendering.
- `shouldComponentUpdate(nextProps, nextState)`: Determines whether component should re-render
    - Called: before render
    - Used for: #optimization.performance - returning false skips update (true by default)
- `render()`: Re-renders the component
- `getSnapshotBeforeUpdate(prevProps, prevState)`: 
    - Called: right before DOM is updated. 
    - Used for: passing something to `componentDidUpdate()` - you can return it from this method.
- `componentDidUpdate(prevProps, prevState, snapshot)`: 
    - Called: immediately after component updates 
    - Used for: working with DOM or sending network requests after updates.


### Unmounting

`componentWillUnmount()`:
    - Called: right before component is unmounted/destroyed
    - Used for: cleanup(e.g. cleaning timers, cancelling network requests, removing event listeners)

### Error Handling

- `static getDerivedStateFromError(error)`
    - Used for: updating state based on the error so that error is not propagated to next render -> returned object is used to update state - `null` to update nothing.
- `componentDidCatch(error)`: 
    - Called: when error has been thrown by descendant component
    - Used for: logging error info