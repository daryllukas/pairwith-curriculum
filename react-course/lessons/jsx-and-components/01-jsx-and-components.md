---
marp: true
theme: gaia
_class: 
  - lead

---

![bg left:40% 80%](../../assets//dll-logo.png)

# **Learn React**

Introduction to JSX Syntax and React Components

With Daryl

---

# Basic Concepts
- We build user interfaces using  **Components**
- **React Updates**. When state (input) changes, the output (UI) also changes.
<!--
- React will react
- Handles updating the browser
-->
- **Virtual DOM**. We are generating HTML view in memory using JavaScript.
<!--
- Tree reconciliation
-->

---

# Components
We split the UI into independent and reusable pieces.

Isolate the pieces

---

![bg](../../assets/react-component-tree.png)

---

## Rendering components

In JSX, we represent HTML elements and React components like this:

```jsx
const htmlButton = <button>Submit</button>
const reactButton = <SubmitButton onSubmit={handleSubmit} />
```

**Always start component names with a capital letter.**
React treats lowercase letters as DOM tags

https://reactjs.org/docs/jsx-in-depth.html#user-defined-components-must-be-capitalized

---
**Try it out**

```jsx
// ./index.js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
function App() {
  return (
    <div>
      <Welcome name="Daryl" />
    </div>
  );
}
const root = ReactDOM.createRoot(document.getElementById('root'));
const element = <App />;
root.render(element);
```
<!-- 
Discuss Hierarchy

Props
- Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
- Readonly
- Pure function doesn't modify its own input
- All React components must act like pure functions with respect to their props.
-->

---
## Components are reusable

```jsx
// ./index.js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
function App() {
  return (
    <div>
      <Welcome name="Daryl" />
      <Welcome name="Matimba" />
      <Welcome name="Mukaba" />
    </div>
  );
}
```

<!-- 
Demo: Tree reconciliation and reactive updates
-->

---

# Let's Code

**Excercise**
- Component Hierarchy
<!-- Break down a given UI into individual compontents -->

**Assignments**
- Build A Static UI
<!-- Build A Static UI using individual compontents identified in the excercise -->
---

## Functions vs Classes

Function Components

```jsx
function Button(props) {
  return <button onClick={props.onSubmit}>Submit</button>;
}
```

Class Components

```jsx
class Button extends React.Component {
  render() {
    return <button onClick={this.props.onSubmit}>Submit</button>
  }
}
```

---

# Let's code

**Excercise**
- Convert from function to class component

**Assignment**
- Convert from class to function component
