---
id: 4kr8qnqvd9azf1jf4gz7hfn
title: React Component
desc: ''
updated: 1722624677867
created: 1722624336602
---

#interview-question

Building blocks of React application. Independent, reusable pieces.

### Functional Components

Functions that take props as argument and return React elements.

```js
function Greeting(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
Functional components can hold state via React Hooks.

### Class Components

ES6 Classes that extend from `React.Component` and must have a `render` method.

```js
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

Class components can hold state.

### Higher-Order Components

React HOCs are like [[paradigm.func.components.higher-order]]s. They take in a component, modify or add state or behavior to it, and return a new component.

