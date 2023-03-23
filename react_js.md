**React js**
  
  React JS is a free and open-source front-end JavaScript library for building user interfaces  based on UI components, especially for single-page applications

**Features of React**

  - JSX
  - Components (Reuse Components)
  - Virtual DOM 
  - One way Data Binding
  - High performance
  - Easy To Debug
  - Supports server-side rendering

**Advatage of react js:**

  - Increases the application's performance with Virtual DOM.
  - It renders both on client and server side (SSR).
  - Easy to write unit and integration tests with tools such as Jest.

## Limitation of React JS
  
  - React is just a view library, not a full framework.
  - 

**Virtual DOM**
  
  The Virtual DOM (VDOM) is an in-memory representation of Real DOM.
  The representation of a UI is kept in memory and synced with the "real" DOM

# Note: Always start component names with a capital letter.

  - React treats components starting with lowercase letters as DOM tags. 
    For example, <div /> represents an HTML div tag, 
  
  - but <Welcome /> represents a component and requires Welcome to be in scope

**Optimizing Performance:**

  - Use the Production Build
  - Single-File Builds
  - Avoid Reconciliation
  - Avoid Unnecessary Re-renders
  - Memorize Callbacks

**JSX**

  JSX stands for JavaScript XML. It is simply a syntax extension of JavaScript
  It allows us to directly write HTML in React (within JavaScript code)

  JSX makes it easier to write or add HTML in React
  JSX can easily convert HTML tags to react elements
  It is faster than regular JavaScript


**Can web browsers read JSX directly?**

  Web browsers cannot read JSX directly. This is because they are built to only read regular JS objects and JSX is not a regular JavaScript object
  
  For a web browser to read a JSX file, the file needs to be transformed into a regular JavaScript object. For this, we use Babel

# PropTypes:

  PropTypes is React's internal mechanism for adding type checking to components.

  TypeScript and flow JS extension also available for type checking
  The set of predefined prop types:

  PropTypes.number
  PropTypes.string
  PropTypes.array
  PropTypes.object
  PropTypes.func
  PropTypes.node
  PropTypes.element
  PropTypes.bool
  PropTypes.symbol
  PropTypes.any

  import PropTypes from 'prop-types';

  class Greeting extends React.Component {
    render() {
      return (
        <h1>Hello, {this.props.name}</h1>
      );
    }
  }

  Greeting.propTypes = {
    name: PropTypes.string
  };

**What is Components?**

  Components are independent and reusable bits of code.

  Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

  Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

# Types:
  - Class Components
  - Functinal Components
  - Pure Components
  - Higher Oreder Components

**Pure function**

  A Pure Function is a function (a block of code) that always returns the same result if the same arguments are passed.

  it renders the same output for the same state and props

  A Pure function is a function that does not modify any external variable.

  functional components that performs shouldComponentUpdate() automatically.
  Re-renders only if state or props is different from previous state or props.

  You can say that pure functions have no side effects.
  Pure functions must not rely on variables outside their scope
  Examples of pure functions are strlen(), pow(), sqrt(), array.length etc

**Higer Oreder Components**

  A higher-order component (HOC) is an advanced technique in React for reusing component logic.
  a higher-order component is a function that takes a component and returns a new component.

  * const EnhancedComponent = higherOrderComponent(WrappedComponent);

**Functional Components:**

  Functional components are functions that takes in props and return JSX.

  They do not natively have state or lifecycle methods, but this functionality can be added by implementing React Hooks

**State and Props**

  State : The state is a built-in React object that is used to contain data or information about the component.
  
  The state is a local data storage that is local to the component only and cannot be passed to other components

  Props : Props provide a way to pass data from one component to another component
  Props are read-only

  Props are short for Properties. It is a React built-in object that stores the value of attributes of a tag and
  works similarly to HTML attributes

**Lifecycle of Components React JS**

It has 3 main phases

  1. Mounting
  2. Updating
  3. Unmounting

  1. Mounting

    - constructor()
    - getDerivedStateFromProps()
    - render() 								      //render required other are optional
    - componentDidMount()

  2. Updating

    - getDerivedStateFromProps()
    - shouldComponentUpdate()				// default value is true
    - render()
    - getSnapshotBeforeUpdate()
    - componentDidUpdate()

  3. Unmounting

    - componentWillUnmount()

**Refs**

  - Refs provide a way to access DOM nodes or React elements created in the render method.
  - Refs are created using React.createRef() and attached to React elements via the ref
    attribute

## Forwarding refs:

  Ref forwarding is an opt-in feature that lets some components take a ref they receive, and pass it further down (in other words, “forward” it) to a child.

**Controlled and uncontrolled components**

* Controlled component: 
  - form data is handled by a React component. 
  - A controlled input accepts its current value as a prop, 
    as well as a callback to change that value.

* Uncontrolled component:
  -	form data is handled by the DOM itself.

**Context API**

  Context provides a way to pass data through the component tree without having to
  pass props down manually at every level.

  Context is designed to share data that can be considered “global” for a tree of
  React components.

  const MyContext = React.createContext(defaultValue);

**Reconciliation**

  When a component’s props or state change, React decides whether an actual DOM update
  is necessary by comparing the newly returned element with the previously rendered one.
  
  When they are not equal, React will update the DOM. This process is called
  “reconciliation”

**fragments**

  Fragment in React is used for a component to return multiple elements.
  Fragments let you group a list of children without adding extra nodes to the DOM

  render() {
    return (
      <React.Fragment>
        <ChildA />
        <ChildB />
        <ChildC />
      </React.Fragment>
    )
  }

# Error boundaries(React version 16)

  Error boundaries are React components that catch JavaScript errors anywhere in their
  child component tree, log those errors, and display a fallback UI instead of the
  component tree that crashed.

  It does not break the whole app component tree and only renders the fallback UI whenever
  an error occurred in a component.

  * Note :
    Before introduce Error boundaries whenever Error or JS Error occur, those errors broke
    react app or put react in broken state.

    To handle those errors, React 16 introduce NEW feature Error Boundaries.

    Error boundaries do not catch errors for:

    - Event handlers
    - Asynchronous code (e.g. setTimeout or requestAnimationFrame callbacks)
    - Server side rendering
    - Errors thrown in the error boundary itself (rather than its children)

    try or catch: is great but it only works for imperative code

# How are error boundaries handled in React v15?

  React v15 provided very basic support for error boundaries using unstable_handleError method.
  It has been renamed to componentDidCatch in React v16.

# React Router

  React Router is a powerful routing library built on top of React that helps you add new screens and flows to your application incredibly quickly,

  React Router is a fully-featured client and server-side routing library for React.
  React Router is the standard routing library for React

# Jest

  Jest is a JavaScript testing framework built on top of Jasmine and maintained by Meta.
  It was designed and built by Christoph Nakazawa with a focus on simplicity and support for large web applications.

  It works with projects using Babel, TypeScript, Node.js, React, Angular, Vue.js and Svelte

# What are the advantages of Jest over Jasmine?
  
  - Automatically finds tests to execute in your source code.
  - Automatically mocks dependencies when running your tests.
  - Allows you to test asynchronous code synchronously.
  - Runs your tests with a fake DOM implementation (via jsdom) so that your tests can be run on the command line. 
  
  - Runs tests in parallel processes so that they finish sooner.

# useCallback VS useMemo:
  Both are use for performance optimization
  
  # Memoize
    memoization or memoisation is an optimization technique used primarily to speed  up computer programs by storing the results of expensive function calls and returning the cached result when the same inputs occur again.

  * useCallback:
    - Returns a memoized callback
    - useCallback will return a memoized version of the callback that only changes
      if one of the dependencies has changed.

  * useMemo :
    - Returns a memoized value
    - useMemo will only recompute the memoized value when one of the dependencies has changed
    - This optimization helps to avoid expensive calculations on every render


# useReducer: 

  The useReducer Hook accepts two arguments
  - useReducer(<reducer>, <initialState>)
  - The useReducer Hook returns the current state and a dispatch method
  - The reducer function contains your custom state logic and the initialState can be a simple  value but generally will contain an object.


# Diffing Algoritham

  React implements a heuristic O(n) algorithm based on 2 assumptions:
	
- Two elements of different types will produce different trees.
- The developer can hint at which child elements may be stable across different 
  renders with a key prop.
 	
# Different root element
	If the root element is different , it completely tears down the old tree and begins from 
	the root of the new tree.

# Same root element:
	When comparing two React DOM elements of the same type, 
  React looks at the attributes of both, keeps the same underlying DOM node, 
  and only updates the changed attributes. For example:

# All the Elements are Of The Same Type:
	so that state is maintained across renders.
	
# Recursion on Child elements
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
</ul>

* Use of key: 
	To solve recursion child problem use KEY attribute

## can we pass hooks as a props?

  No, The benefit of passing the hook as a prop will be that you can conditionally pass another hook / skip the call. But in the case of hooks, It should not be called conditionally. So there is no point. of passing it as a prop, Just import it and use it.


## package-lock.json vs package.json

# package.json  
  - automatically generated and updated by npm, it can also be edited manually.
  - doesn’t specify exact version numbers for dependencies
  - only tracks top-level dependencies for the project
  
# package.json
  - sets the minimum version for each dependency,
  - Its track the entire tree of dependencies and the exact version of each dependency.

## what is minification?

  Minification, also known as minimization, is the process of removing all unnecessary characters from JavaScript source code without altering its functionality. 
  
  This includes the removal of whitespace, comments, and semicolons, along with the use of shorter variable names and functions.

  It's one of the main methods used to reduce load times and bandwidth usage on websites.

# Keys
  Keys help React identify which items have changed, are added, or are removed.

# Single-page application
  A SPA is a web application or website that interacts with the user by dynamically rewriting the current web page with new data from the web server.

  a page refresh never occurs

## Lazy loading:

   lazy loading means that a component or a part of code must get loaded when it is required

Middleware syntax 
------------------	*/
export function FirstMiddleWare(store) {
	return function(next) {
		return function(action) {

		}
	}
}

//ES6 
export let logger = store=>next=>action=> {
	console.log("Before Action " , action.type ,store.getState())
    var result =  next(action)
   	console.log("After Action store state is" , store.getState())
   	return result
}

  Code :

  const arr = [1,1,2,3,1,4]
  ans : Highest No: 1 and Occurance:3


## Recommended ordering of methods from mounting to render stage:

- static methods
- constructor()
- getChildContext()
- componentWillMount()
- componentDidMount()
- componentWillReceiveProps()
- shouldComponentUpdate()
- componentWillUpdate()
- componentDidUpdate()
- componentWillUnmount()

- click handlers or event handlers like onClickSubmit() or onChangeDescription()
- getter methods for render like getSelectReason() or getFooterContent()
- optional render methods like renderNavigation() or renderProfilePicture()
- render()