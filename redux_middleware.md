# Redux

- Redux is an open-source, JavaScript library used to manage the application state
- Redux is state managment tool
- Redux use to manage and update application state, using events called "actions".

- Action : It is an object that contains the payload of information.
- Action Creators : It is a function that creates and returns an action object.

  const addTodo = text => {
    return {
      type: 'todos/todoAdded',
      payload: text
    }
  }

# Reducer:

  A reducer is a function that receives the current state and an action object and return
  the new state: (state, action) => newState

  Reducers update store based on the value of the action

# Hooks
  React Redux provides a pair of custom React hooks that allow your React components to interact with the Redux store.

  useSelector => reads a value from the store state and subscribes to updates

  useDispatch => returns the store's dispatch method to let you dispatch actions.

* Note:
    The useDispatch and useSelector hooks are alternatives to mapDispatchToProps and mapStateToProps, respectively.

# flux JavaScript

  It is a JavaScript Architecture or pattern for UI which runs on a unidirectional data flow and has a centralized dispatcher

  It is useful when your project has dynamic data and you need to keep the data updated in an effective manner.

  * Redux                                          Flux
    Redux includes a single Store per app.         Flux includes multiple Stores per app 
    

# redux-saga vs redux-thunk
  
- Both Redux Thunk and Redux Saga take care of dealing with side effects.
- In most of the scenarios, Thunk uses Promises to deal with them, whereas Saga uses Generators.

- Thunk is simple to use and Promises are familiar to many developers,
- Sagas/Generators are more powerful but you will need to learn them.

# Webpack

  Webpack is a popular module bundling system built on top of Node. js. 
  It can handle not only combination and minification of JavaScript and CSS files, 
  but also other assets such as image files (spriting) through the use of plugins.

##  Middleware:
  Middleware helps you with logging, error reporting, making asynchronous requests, routing and a whole lot more

# Redux-thunk:

  Redux-Thunk is a middleware that allows our action creators to return a function instead of an action object.

  The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met.

  The inner function receives the store methods dispatch() and getState() as parameters.

  can contain both synchronous and asynchronous logic.

  Dispatching thunk functions
  const thunkFunction = (dispatch, getState) => {
  // logic here that can dispatch actions or read state
  }

  store.dispatch(thunkFunction)


# redux-saga

  redux-saga is a library that aims to make side effects (asynchronous things like data fetching and impure things like accessing the browser cache) in React/Redux applications easier and better

# Generator function(*)
  
  A generator is a special type of function which does not return a single value, instead, it returns an iterator object with a sequence of values.

  * yield => The yield keyword is used to pause and resume a generator function.

  # Effect Creators
    Redux actions which serve as instructions for Saga middleware

    select => returns the full state of the application
    put    => dispatch an action into the store (non-blocking)
    call   => run a method, Promise or other Saga (blocking)

  # Effect combinators
    all  =>  run multiple Effects in parallel and wait for all of them to complete. similar to Promise.all

  # Helpers:
    takeEvery => takes every matching action and run the given saga (non-blocking)
  
  
    function* generator(i) {
    yield i;
    yield i + 10;
    }
    // init
    const gen = generator(10);

    // use
    console.log(gen.next()); // {value: 10, done: false}
    console.log(gen.next()); // {value: 20, done: false}
    console.log(gen.next()); // {value: undefined, done: true}


  ## imp linkes:
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*
  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield