# 🔥Crack-React-Interview-Questions

## 1)What is React.js?
- React.js is an open-source JavaScript library created by Facebook for building modern, interactive user interfaces, primarily for single-page applications (SPAs). It allows developers to build web applications that can update and render efficiently based on data changes, without requiring a page reload.

```bash
function Welcome() {
  return <h1>Hello, React!</h1>;
}

```
- Here, we are creating a simple React component that renders a "Hello, React!" message. This component is reusable and can be plugged into any part of a larger application

## 2) What are the main features of React.js?
- Component-based architecture: UI is divided into small, reusable pieces called components. Each component can have its own logic and state.
- Virtual DOM: React creates a virtual representation of the DOM and updates only the parts that have changed, making the update process faster.
- Declarative: React allows you to describe what the UI should look like at any point in time, and it automatically updates when the data changes.
- Unidirectional data flow: Data flows from parent components to child components, making the application easier to debug and reason about.

## 3) What are the advantages of using React.js?
- Reusable components: Write once, reuse anywhere. This reduces redundancy and increases maintainability.
- Fast performance: With the Virtual DOM, React can efficiently update and render components only when necessary.
- SEO-friendly: React can be rendered on the server side (with libraries like Next.js), making applications more SEO-friendly compared to traditional client-side rendering.
- Strong ecosystem: React has a large community and a rich ecosystem of tools, libraries, and resources, making it easier to build, test, and maintain React applications.
## 4)What is JSX in React?
- JSX (JavaScript XML) is a syntax extension for JavaScript that looks similar to HTML. It allows you to write HTML elements directly within JavaScript code. JSX makes the code more readable and expressive.

```bash
const element = <h1>Hello, World!</h1>;

```
- JSX allows you to write this HTML-like syntax directly in JavaScript files. The above JSX code is compiled into a React.createElement() call that creates a React element.


## 5)  How does JSX differ from HTML?
- JSX uses JavaScript expressions: You can insert JavaScript expressions inside JSX using curly braces {}.
- JSX has slight syntax differences: For example, you use className instead of class, and all tags must be closed (even self-closing tags like <img />).
- JSX is compiled: JSX isn't understood by the browser directly; it gets transformed into JavaScript functions by Babel before it is executed.

```bash
const name = "React";
const element = <h1>Hello, {name}!</h1>; // "Hello, React!"

```

## 6)What is the Virtual DOM in React?
- The Virtual DOM is an in-memory representation of the real DOM elements. React uses the Virtual DOM to track changes in the UI and efficiently update the real DOM without redrawing the entire page. This reduces the number of expensive operations on the real DOM, improving performance.


## 7) How does the Virtual DOM work?
- When the state or props of a React component change, React creates a new Virtual DOM tree. It then compares this new tree with the previous one (a process called "diffing"). Only the parts of the DOM that have changed are updated in the real DOM, making the update process efficient.
## 8)What is the difference between the Virtual DOM and the Real DOM?
- Virtual DOM: Exists in memory and is a lightweight copy of the real DOM. It allows React to make updates without directly interacting with the real DOM, which is a slow process.
- Real DOM: Represents the actual DOM structure on the webpage. Any update to the real DOM requires re-rendering of the page, which is slower.
## 9)What are components in React?
- Components are the building blocks of a React application. Each component represents a part of the UI. Components can be either simple (like a button) or complex (like a form). A component can accept inputs (called props) and maintain its own state.
```bash
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
- In this example, Welcome is a functional component that receives a name prop and renders a greeting message.

## 10)What are the different types of components in React?
- Functional Components: These are basic components that are JavaScript functions and do not have their own state or lifecycle methods. They receive props as an argument and return JSX.
- Class Components: These components are ES6 classes that extend React.Component. They can have their own state and lifecycle methods.
- Example of a class component:
```bash
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

 ```

## 11) What is the purpose of render() in React?
- In class components, the render() method is required. It returns the JSX that defines how the UI should look. Every time a component’s state or props change, the render() method is called to update the UI.

```bash
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

```
## 12) What is the significance of the key prop in React?
- key is used in lists of components to uniquely identify each item. This helps React efficiently update and reorder elements in the list when the data changes.
```bash
const items = ['Apple', 'Banana', 'Cherry'];
const itemList = items.map((item, index) => <li key={index}>{item}</li>);

```

## 13) Why are keys important in lists?
- Keys help React identify which elements have changed, been added, or been removed. Without keys, React would re-render the entire list, leading to poor performance. Keys provide stability to the list and help avoid unnecessary DOM operations.
## 14)What is a functional component in React?
- A functional component is a JavaScript function that takes props as an argument and returns a React element (JSX). Functional components are simple and stateless by nature, but with React hooks, they can now manage state and lifecycle events.

```bash
function Greeting(props) {
  return <h1>Hello, {props.name}</h1>;
}

```

## 15) What is a class component in React?
- A class component is a more traditional way to define a React component using ES6 classes. Class components can hold state and have access to lifecycle methods, making them more feature-rich than functional components (before React Hooks were introduced).

```bash
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

```

## 16)What are props in React?
- Props (short for properties) are inputs passed from a parent component to a child component. Props are read-only and cannot be modified by the child component. They allow components to be dynamic and reusable.
```bash
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
## 17) How are props used in React?
- Props are passed to a component as attributes in JSX. The component receives them as an argument and can render dynamic content based on them.
```bash
<Welcome name="John" />
```
## 18)What is state in React?
- State is an internal object in a class component or a functional component (with hooks) that holds data that can change over time. Unlike props, state is mutable and is typically used for data that changes in response to user actions or other events.
```bash
class Counter extends React.Component {
  state = { count: 0 };

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>{this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}
```
## 19)How is state different from props in React?
- Props: Passed from parent to child and cannot be changed by the child component (read-only).
- State: Managed within the component and can be updated using setState().

## 20)How do you update the state in a React component?
- You can update the state using the setState() method. This method merges the new state with the existing state and triggers a re-render of the component.

```bash
this.setState({ count: this.state.count + 1 });
 ```


## 21) What is the use of setState() in React?
- setState() is used to update the component’s state. When setState() is called, React schedules a re-render of the component with the new state. This ensures the UI is in sync with the state.
```bash
this.setState({ name: 'John' });

```
## 22) What is the lifecycle of a React component?
- The lifecycle of a React component can be divided into three phases:

- Mounting: When the component is first created and inserted into the DOM.
- Updating: When the component's state or props change, and it needs to re-render.
- Unmounting: When the component is removed from the DOM.

## 23)What are React lifecycle methods?
- Lifecycle methods are special methods that are called at different stages of a component’s lifecycle. They allow developers to hook into these stages and execute custom logic.

### Common lifecycle methods:

- componentDidMount(): Called after the component is inserted into the DOM.
- componentDidUpdate(): Called after the component is re-rendered due to state or prop changes.
- componentWillUnmount(): Called before the component is removed from the DOM.
## 24)What is the use of componentDidMount()?
- componentDidMount() is invoked immediately after a component is mounted (inserted into the DOM). It’s commonly used for making network requests or initializing third-party libraries.
```bash
componentDidMount() {
  fetch('/api/data')
    .then(response => response.json())
    .then(data => this.setState({ data }));
}
```

## 25) What is the use of componentWillUnmount()?
- componentWillUnmount() is invoked immediately before a component is unmounted and destroyed. It's used for cleanup tasks like clearing timers or unsubscribing from event listeners.
```bash
componentWillUnmount() {
  clearInterval(this.timer);
}


```

## 26)What is the use of componentDidUpdate()?
- componentDidUpdate() is called after a component has re-rendered due to changes in props or state. This is useful for responding to updates, such as making additional network requests when certain conditions are met.
## 27) What is the use of shouldComponentUpdate()?
- shouldComponentUpdate() allows you to control whether a component should re-render or not when state or props change. It’s often used to optimize performance by preventing unnecessary re-renders.
```bash
shouldComponentUpdate(nextProps, nextState) {
  return nextProps.value !== this.props.value; // only re-render if the value changes
}

```
## 28)What is the difference between componentWillMount() and componentDidMount()?
- componentWillMount() is called before the component is rendered (but it’s deprecated).
- componentDidMount() is called after the component has been rendered and inserted into the DOM, making it a safer place for code that relies on the DOM being available.
## 29)What is the use of constructor() in a React class component?
- The constructor() method is used to initialize the state and bind methods to the component instance in a class component. It's the first method called when a component is instantiated.
```bash
constructor(props) {
  super(props); // Must call super() before accessing 'this'
  this.state = { count: 0 };
}
```
## 30)What is the purpose of super() in React?
- super() is required in a constructor when extending a class. It calls the constructor of the parent class (React.Component), giving the child component access to this and props.
```bash
constructor(props) {
  super(props); // Calls the parent class's constructor
  this.state = { count: 0 };
}
```

## 31) What are React Hooks?
- React Hooks are functions that allow you to "hook into" React features, such as state and lifecycle methods, in functional components. Hooks were introduced in React 16.8 to make functional components more powerful, eliminating the need to write class components in many cases.

- For example, the useState hook enables you to add local state to a functional component, while useEffect allows you to perform side effects like fetching data or subscribing to events.
#### Example 
```bash
import { useState, useEffect } from 'react';

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    const timer = setInterval(() => {
      setCount(prevCount => prevCount + 1);
    }, 1000);

    // Cleanup the timer when component unmounts
    return () => clearInterval(timer);
  }, []);

  return <h1>Timer: {count}</h1>;
}
```
## 32) What is the useState hook in React?
- useState is a hook that lets you add state to functional components. It returns two values: the current state and a function to update that state.

- You can think of state as data that can change over time. useState helps you handle such data changes in a React component.
#### Example 
```bash
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Current count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increase Count</button>
    </div>
  );
}
```
- Here, count is the state variable, and setCount is the function used to update it.
## 33)What is the useEffect hook in React?
- useEffect is a hook that lets you perform side effects in function components, such as fetching data, directly manipulating the DOM, or setting up subscriptions. It is similar to lifecycle methods in class components, such as componentDidMount, componentDidUpdate, and componentWillUnmount.
#### Example
```bash
import { useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(result => setData(result));

    // Optional cleanup function
    return () => {
      console.log('Cleanup when component unmounts');
    };
  }, []); // Empty array ensures this runs only once after the initial render

  return <div>{data ? JSON.stringify(data) : 'Loading...'}</div>;
}
```
- Here, useEffect fetches data after the component renders, and the empty dependency array ensures the effect runs only once.
## 34) What is the useContext hook in React?
- useContext is a hook that allows you to consume values from a React Context without the need for prop drilling (passing data through multiple layers of components).
#### Example
```bash
const ThemeContext = React.createContext('light');

function ThemedButton() {
  const theme = useContext(ThemeContext);

  return <button className={theme}>Button with {theme} theme</button>;
}

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <ThemedButton />
    </ThemeContext.Provider>
  );
}
```
- In this example, ThemedButton can access the theme directly from ThemeContext without needing to pass it as a prop from the parent.
## 35) What is the useReducer hook in React?
- useReducer is a hook that is used to handle more complex state logic in React components. It’s similar to useState but allows for more control by using reducers (functions that determine changes to state based on actions).
#### Example
```bash
import { useReducer } from 'react';

function reducer(state, action) {
  switch (action.type) {
    case 'increment':
      return { count: state.count + 1 };
    case 'decrement':
      return { count: state.count - 1 };
    default:
      throw new Error();
  }
}

function Counter() {
  const [state, dispatch] = useReducer(reducer, { count: 0 });

  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={() => dispatch({ type: 'increment' })}>Increment</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button>
    </div>
  );
}
```
- useReducer is a good alternative to useState when the state logic becomes complex, such as when multiple values depend on each other.

## 36)What is the useRef hook in React?
- useRef returns a mutable object whose .current property persists across re-renders. It’s commonly used to access DOM elements or store values that don’t need to trigger a re-render when updated.
#### Example
```bash
import { useRef } from 'react';

function TextInputWithFocusButton() {
  const inputEl = useRef(null);

  const onButtonClick = () => {
    inputEl.current.focus();
  };

  return (
    <div>
      <input ref={inputEl} type="text" />
      <button onClick={onButtonClick}>Focus the input</button>
    </div>
  );
}
```
- Here, useRef is used to access the input DOM element and trigger the focus on button click without causing a re-render.


## 37)  What is the useCallback hook in React?
- useCallback is a hook that returns a memoized version of a callback function, which means it will only recreate the function if its dependencies change. This is useful for optimizing performance, particularly in scenarios involving expensive operations or when passing functions as props.
#### Example
```bash
import { useState, useCallback } from 'react';

function Button({ onClick }) {
  console.log('Button rendered');
  return <button onClick={onClick}>Click me</button>;
}

function App() {
  const [count, setCount] = useState(0);

  const handleClick = useCallback(() => {
    setCount(count + 1);
  }, [count]);

  return (
    <div>
      <p>Count: {count}</p>
      <Button onClick={handleClick} />
    </div>
  );
}
```
- useCallback prevents the handleClick function from being recreated on every render unless count changes, thus avoiding unnecessary re-renders of the Button component.
## 38)What is the useMemo hook in React?
- useMemo is a hook that memoizes the result of a computation. It recomputes the memoized value only when one of its dependencies changes, which helps optimize performance by preventing expensive calculations on every render.
#### Example
```bash
import { useMemo, useState } from 'react';

function App() {
  const [count, setCount] = useState(0);

  const expensiveCalculation = (num) => {
    console.log('Expensive calculation');
    return num * 2;
  };

  const result = useMemo(() => expensiveCalculation(count), [count]);

  return (
    <div>
      <p>Result: {result}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}

```
- Here, useMemo memoizes the result of expensiveCalculation, preventing it from running on every render unless count changes.
## 39)What are custom hooks in React?
- Custom hooks are functions that encapsulate reusable logic built using React’s built-in hooks like useState, useEffect, and others. Custom hooks let you reuse logic across multiple components.
#### Example
```bash
function useLocalStorage(key, initialValue) {
  const [value, setValue] = useState(() => {
    const savedValue = localStorage.getItem(key);
    return savedValue !== null ? JSON.parse(savedValue) : initialValue;
  });

  useEffect(() => {
    localStorage.setItem(key, JSON.stringify(value));
  }, [key, value]);

  return [value, setValue];
}

function App() {
  const [name, setName] = useLocalStorage('name', '');

  return (
    <div>
      <input value={name} onChange={(e) => setName(e.target.value)} />
    </div>
  );
}
```
- In this example, the useLocalStorage custom hook allows any component to easily manage state that syncs with localStorage.
## 40)How do you create custom hooks in React?
- Custom hooks are created by writing a function that uses other hooks (such as useState, useEffect, etc.) and begins with the prefix use.
#### Example
```bash
function useDocumentTitle(title) {
  useEffect(() => {
    document.title = title;
  }, [title]);
}

function App() {
  useDocumentTitle('My App Title');
  return <div>Check the document title!</div>;
}
```
- This custom hook useDocumentTitle allows you to change the document title from any component without duplicating logic.

