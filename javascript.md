**Typescript**

- TypeScript is a programming language developed by Microsoft
- It is a typed superset of JavaScript, and includes its own compiler.
- Being a typed language, TypeScript can catch errors and bugs at build time,

**JavaScript:**

- JavaScript is a lightweight, interpreted, or just-in-time(run time compilation) compiled programming language with first-class functions.

- JS single threaded language.


**ES5 VS ES6**

- Performance improve
- requires to import
- Exports to export
- Introduced Components
- Added Arrow function
- LET and const
- Object manupulation
  - Spread
  - Rest operator
- Symbol data type
- Promise
- Callback

**Destructuring**

- Destructuring is a JavaScript expression that allows us to extract data from arrays, objects,
  and maps and set them into new, distinct variables.

  Ex. [a, b] = array;

**Spread vs Rest operator and Destructuring**

- Destructuring: It is used create varibles from array items or object properties.
- Spread: Spread unpack iterables such as arrays, objects, and function calls.
- Rest: Rest will create an array from an indefinite number of values

**var , let and const**

- Var : global and functinal scope
- Let : global and functinal and block scope

# Hosting

- var are hoisted to the top and can be initialized at any time.
- let and const are hoisted to the top of the block, but not "initialized".

- The variable(Let and const) is in a "temporal dead zone" from the start of the block until it is declared

  Let : RefferenceError if use before it is declared
  Const : Syntax Error if use before it is declared (so the code will simply not run)

# Temporal Dead Zone:

  It is the period of time during which the let and const declarations cannot be accessed

  A temporal dead zone (TDZ) is the area of a block where a variable is inaccessible until the moment the computer completely initializes it with a value.

  it is the phase between the starting of the execution of block in which the let or const variable is declared till that variable is being initialized is called Temporal Dead Zone for the variable.

**strict mode**
  - JavaScript in strict mode does not allow variables to be used if they are not declared.
  - usage => "use strict";

**Shallow copy vs Deep copy**

  Primitive Data types                Non Primitive Data Types
  - Numbers                           - array 
  - Boolean                           - object      
  - String                            - function
  - null
  - undefined

* Primitive types are immutable and always create Deep Copy.
  
  - In deep copy, When original variable (originalVariable) copied into or assign to copy
    variable (copyVariable) then, only copyvariable is changed not originalvariable

* Non primitive type create Shallow Copy

  - To convert shalow copy to deep copy there has methods,
    1. JSON.stringify (based on code)
    2. Object.assign (partial options)
    3. Spread operator with minimal changes

Deep Copy: A deep copy of an object is a copy whose properties do not share the same references
Shalow Copy: A shallow copy of an object is a copy whose properties share the same references

**String and Array methods:**

- String:

  Extracting a part of a string:

  slice(start, end) => extracts a part of a string and returns the extracted part in a new string.
  substring(start, end)
  substr(start, length)

  length
  replace()
  toLowerCase() and toUpperCase()
  concat()
  trim()
  padStart() and padEnd()

  charAt(position) || charCodeAt(position) || Property access [ ]
  split()

- Array methods:

  toString() -  converts an array to a string of (comma separated) array values
  join()      - joins all array elements into a string (returns an array as a string)
  pop()       - removes the last element from an array:
  push()      - adds a new element to an array (at the end)
  shift()     - removes the first array element and "shifts" all other elements to a lower index.
  unshift()   - unshift() method adds a new element to an array (at the beginning),
  concat()    - The concat() method concatenates (joins) two or more arrays.
  slice()     - slices out a piece of an array.
  splice()    - adds new items to an array

* slice   =>    returns a piece of the array but it doesn't affect the original array. 
* splice  =>    changes the original array by removing, replacing, or adding values and returns the affected values.

## Optional Chaining (?.)

  The optional chaining operator (?.) accesses an object's property or calls a function. 
  If the object is undefined or null, it returns undefined instead of throwing an error.

# First class function
  First-class functions means when functions in that language are treated like any other variable.

  const handler = () => console.log("This is a click handler function");

# Callback Function
  A function passed into another function as an argument.

# Higer Order Function
  A function which takes another function as an argument or returns a function is known as a higher order function.

# First Order Function
  A function that doesn’t accept another function as an argument and doesn’t return a function as its return value.

const firstOrder = () => console.log("I am a first order function!");

# map vs forEach vs reduce vs filter
  
 map                                    forEach
- map return a new array                 - Not return an array(or return undefined)
- can attach filter,reduce,sort          - forEach is not chainable

# Closure 
  The closure is a combination of functions, where the outer functional scope can be accessible 
  to the inner function.

  function makeFunc() {
    var name = 'Amit';
    function displayName() {
      console.log(name);
    }
    return displayName;
  }

  const myFunc = makeFunc();
  myFunc();

**Debouncing and Throttling**

- Debouncing and throttling are techniques in javascript to optimise the application and browser performance.

* Debouncing:

  - Debouncing is used to ensure that time-consuming tasks do not fire so many times,
    that it affects the performance of the web page.

  - limits the execution of a function call
  - and waits for a certain amount of time before running it again.

* Throttling:

  - Throttling is a technique used to limit the execution of an event handler function,
    even when this event triggers continuously due to user actions.

  - The common use cases are browser resizing, window scrolling etc.

**True values:**
=> '', '0', {} , [] All these will give true value

**False values:**
=> false, undefined, null , 0, NaN

**Null vs Undefined**

- Null is a value that was defined but empty or null,
- whereas undefined is a value that was declared but no value assigned.
- Undefined is a type where null is an object.

## Nullish
  A nullish value is the value which is either null or undefined. Nullish values are always falsy.

**undefined vs Not defined**

- undefined => indicates that a variable has been declared but not given a value
- not defined => indicates that a variable does not exist.


* what is script async and defer? *https://javascript.info/script-async-defer*

  # defer:

    - Scripts with defer never block the page.
    - Scripts with defer always execute when the DOM is ready (but before DOMContentLoaded event).
    
    ex => <script defer src="https://javascript.info/article/script-async-defer/long.js?speed=1"></script>
    
  # async

    - The browser doesn’t block on async scripts (like defer).
    - DOMContentLoaded and async scripts don’t wait for each other:

    ex => <script async src="https://javascript.info/article/script-async-defer/long.js"></script>

  - The async/defer attribute is only for external scripts
  - the async/defer attribute is ignored if the <script> tag has no src attribute.


**preventDefault() vs stopPropagation()**

  - preventDefault()  => prevents the default browser behavior for a given element.
  - stopPropagation() => stops an event from bubbling or propagating up the DOM tree.


**Event Bubbling and Capturing:**

  Bubbling and Capturing are the two phases of propagation.
  * Event Bubbling :

  - Bottom to Top (Event Bubbling)
  - Document <= HTML <= Body <= Div <= Button
        
    <<<===========================

  * Event Capturing:
  - Capturing travels from the root to the target.  
  - Top to Bottom(Event Capturing)

  - Document => HTML => Body => Div => Button
        
    ==============================>>>



## The event loop:

  Event loop is responsible for executing the code, collecting and processing events, and executing queued sub-tasks.

  The Event Loop processes Tasks and Microtasks. It places them into the Call Stack for execution one at a time. It also controls when rerendering occurs.

# call stack:

  The call stack is responsible for keeping track of all the operations in line to be executed. Whenever a function is finished, it is popped from the stack.

  The Call Stack tracks function calls. 
  It is a LIFO stack of frames. 
  Each frame represents a function call.

# Event Queue:
  Event handle the promise functinality

**Typed arrays**
 - typed arrays are like objects that provide a mechanism for reading and writing raw binary data in memory buffers.

# the purpose of void 0:
  Void(0) is used to prevent the page from refreshing. This will be helpful to eliminate the unwanted side-effect, because it will return the undefined primitive value.

  <a href="JavaScript:void(0);" onclick="alert('Well done!')">
    Click Me!
  </a>

**Prototypal inheritance**  (https://javascript.info/prototype-inheritance)

- Objects have a special hidden property [[Prototype]], that is either null or references another object. 
  That object is called “a prototype”:

- When we read a property from object, and it’s missing, JavaScript automatically takes it from the prototype.
  In programming, this is called “prototypal inheritance”.

## What is interceptor in Javascript?
  Interceptors are code blocks that you can use to preprocess or post-process HTTP calls, helping with global error handling, authentication, logging, and more.

**Currying**

- Currying transforms a function with multiple arguments into a sequence/series of functions 
  each taking a single argument.

  # Why it’s useful ?
    - Currying helps to avoid passing the same variable again and again.
    - It helps to create a higher order function

  Example:

    function sum(a, b, c) {                     function sum(a) {
    return a + b + c;             ==>               return (b) => {
    }                                                   return (c) => {   
    sum(1,2,3); // 6                                      return a + b + c
                                                        }
                                                    }
                                                }
                                                console.log(sum(1)(2)(3)) // 6



# Tree shaking
  Tree shaking is a form of dead code elimination. It means that unused modules will not be included in the bundle during the build process.


# IIFE (Immediately Invoked Function Expression)
  * It is an  Self-Executing Anonymous Function 
  * runs as soon as defined.


  (function () {
    // …
  })();

  The primary reason to use an IIFE is to obtain data privacy because any variables declared within the IIFE cannot be accessed by the outside world. i.e, If you try to access variables with IIFE then it throws an error.


```
  let num;
  for (var i = 0; i<5; i++) {
  num = i;
  setTimeout(function(){
    console.log(num);
    },1000);
  }
```

**Callback hell**

	function callback_fun_1 () {
			function callback_fun_2 (){
				function callback_fun_3 (){
					function callback_fun_4 (){
						function callback_fun_5 (){
							function callback_fun_6 (){
								console.log("This is a callback hell function")
						}
					}
				}
			}
		}
	}


# Babel:
  Babel is a JavaScript transpiler that converts edge JavaScript(ES6) into plain old ES5 JavaScript that can run in any browser even in the old ones.