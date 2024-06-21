# `src` Folder

This **`src`** folder is where you will place practice and demo material for each class.

> :warning: **Do *NOT*** use this repository for any assignments that are worth marks. :warning:

If there is a sample in your instructor's workbook that you want to pull into your own workbook, the easiest way to do that is through a Node package called [**tiged**](https://github.com/tiged/tiged#readme). Here's an example of how to use it to [grab a subdirectory](https://github.com/tiged/tiged#specify-a-subdirectory) from your instructor's workbook:

> ***Note:** The following is based on using the `pnpm dlx` command. If you are using regular node/npm, you should use `npx` instead of `pnpm dlx`.*

```bash
$ pnpm dlx tiged --disable-cache --force DMIT-1234/Instructor-Workbook/src/008/demo-events ./src/008/demo-events
//\____________________________________/ \_______________________________________________/ \___________________/
//      |- Command to run               |- Instructor's source folder (on GitHub)        |- Your local destination folder
```

A more detailed explanation of the command would look like this:

```bash
$ pnpm dlx tiged --disable-cache --force DMIT-1234/Instructor-Workbook/src/008/demo-events ./src/008/demo-events
//\______/ \___/ \_____________/ \_____/ \_______/ \_________________/ \_________________/ \___________________/
// |    |          |          |       |             |                     |                     |- Destination folder
// |    |          |          |       |             |                     |- Instructor's sub-folder
// |    |          |          |       |             |- Name of Instructor's Repo
// |    |          |          |       |- GitHub Organization or User
// |    |          |          |- Force overwrite of existing files
// |    |          |- Disable caching of repo (so you grab the latest version)
// |    |- Command to run
// |- pnpm dlx is a Node package runner (alternative to npx)
```

----

## Starter Kits

- [MDN Curriculum - JavaScript](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/)
  - [6.1 Variables](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.1_variables)
  - [6.2 Math](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.2_math)
  - [6.3 Text](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.3_text)
  - [6.4 Arrays](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.4_arrays)
  - [6.5 Conditionals](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.5_conditionals)
  - [6.6 Loops](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.6_loops)
  - [6.7 Functions](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.7_functions)
  - [6.8 JavaScript object basics](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.8_javascript_object_basics)
  - [6.9 DOM scripting](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.9_dom_scripting)
  - [6.10 Events](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.10_events)
  - [6.11 Async JavaScript basics](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.11_async_javascript_basics)
  - [6.12 Network requests with fetch()](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.12_network_requests_with_fetch)
  - [6.13 Working with JSON](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.13_working_with_json)
  - [6.14 Libraries and frameworks](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.14_libraries_and_frameworks)
  - [6.15 Debugging JavaScript](https://developer.mozilla.org/en-US/curriculum/core/javascript-fundamentals/#6.15_debugging_javascript)


1. Course Intro
   - [**000**](./000/ReadMe.md)
1. CLIs, Version Control and Markdown (*Week 0*)
   - [**001 - Start Here**](./001-StartHere/ReadMe.md) - Markdown & git
   - [**002**](./002/ReadMe.md) - More Markdown
1. JavaScript Environments - *In each environment, declare variables and assign values.*
   - What is a REPL? *Read-Eval-Print Loop*
   - The browser Developer Tools' *Console* tab as a REPL

      ```js
      let answer = 42 // undefined
      answer // 42
      let message = "Hello World!" // undefined
      message // "Hello World!"
      message = answer // 42
      message // 42
      ```

   - Node REPL
     - `.help`
   - JavaScript as a Language: case-sensitive, loosly typed, "interpreted" vs. "compiled" (interpreted languages need an "environment" in which to run while compiled languages have their source code "compiled" into stand-alone executables or libraries)
1. HTML Review and Web Servers
   - Viewing HTML Files in the Browser
   - Why Web Servers?
   - Simple Node Projects
     - Bare-bones project with [Vite]() as a local server
     - Multi-page demo (for paths and the "web root")
   - An aside on file structure
   - An aside on Classless CSS (e.g.: picocss)
1. Variables, Values and Data Types
   - List & describe JavaScripts built-in data types
   - Explore `var`, `let` and `const`
   - `typeof` for primitive types
   - Literal values
   - Stranger Things *(a sneak peek)*:
     - What are Objects?
     - What are Arrays?
     - Functions as Objects
1. A Primer on Functions
   - What is a function?
     - *A set of instructions for manipulating information*
     - We *call* functions to "invoke" certain behaviours/actions/calculations
     - We can *declare* our own functions
   - Global functions (browser only): `alert()`, `prompt()`, `confirm()`
   - Method vs. Function
     - Global `console` object and `.log()`, `.error()`, `.info()` (browser and node)
     - **Dot notation**: The ever-humble, often-present **Property Accessor** - `.`
     - Members of `console`: in the node REPL, type `console.` and then hit <kbd>tab</kbd> twice.
1. A Gentle Introduction to Math and Operators
   - Numbers and arithmetic operators
   - Global `Math` object and utility functions/properties
     - In the node REPL, type `Math.` and hit <kbd>tab</kbd> twice
   - String concatenation with `+` operator
   - Template strings and `${placeholders}`
1. Object fundamentals
   - Object Literal Syntax
   - Members: Properties and Functions
     - **Dot notation**: The ever-humble, often-present **Property Accessor** - `.`
   - Objects are so much more... *(foreshadow Classes)*
1. DOM Elements as JavaScript Objects
   - Inspecting Elements in the Developer Tools (`$0`)
   - The Complexity of DOM objects
     - *Explore the properties of simple `<h1>`, `<p>`, and `<img>` elements*
   - Searching the `document` for elements
     - `.querySelector()`
     - `.querySelectorAll()`
     - `.getElementById()`
   - Text inside Elements
     - simple DOM elements, then complex DOM elements
     - Properties: get and set the value
       - `.innerText`
       - `.innerHTML`
       - `.textContent`
1. The Complexity Behind Primitives
   - Numbers: `.toString()`, `.toFixed()`
   - String methods:
     - `.toUpperCase()`
     - `.toLowerCase()`
     - `.startsWith()`
     - `.endsWith()`
     - `.includes()`
     - `.padEnd()`
     - `.padStart()`
     - `.repeat()`
     - `.replace()`
     - `.trim()`
     - `.trimLeft()` and `.trimStart()`
     - `.trimRight()` and `.trimEnd()`
     - `.substr()` and `.substring()`
     - `.search()`
     - `.repeat()`
     - `.split()`
1. DOM Styling in JavaScript
   - The `.classList` attribute
     - Add/Remove/Toggle
   - The `.style` attribute
     - Specific classnames
   - Exploring via the Browser's Console (Dev Tools)
   - Intellisense in VS Code by using `.` after query-selecting DOM
1. DOM Events and Listeners
   - Different kinds of events:
     - User-initiated events: mouse, keyboard
     - DOM-initiated events: page is loaded, page is navigating away, browser is losing focus or gaining focus (*yes, those annoying ads when you leave/re-enter a page*)
   - Adding Event Listeners
     - You can have multiple listeners for a single event
   - Event bubbling
   - Cancelling default behaviour
     - Stopping navigation of an `<a href>`
   - Functions as variables and "callbacks"
1. Function Callbacks
   - Expecting a function as a parameter
   - Passing a function as an argument
   - Recursion
1. HTML Forms and JavaScript
   - Client-Side Processing and `.preventDefault()`
   - Forms and Dialogs
1. Decisions: Alternate Paths of Logic
   - `if`/`else` statements as "flow-control"
     - "Truthy" and "Falsy" values
     - Simple conditional expressions
     - `&&`, `||` and `!`
   - `if` statements as "validation" (e.g.: *guard clauses* in functions)
     - `typeof` and `instanceof`
     - Other types of validations (in-range)
1. Loops: Repetition
   - Grammar of
     - `while() {}`
     - `do{}while()`
     - `for(init;compare;inc){}`
   - Algorithms:
     - Fibonacci
       - Display the sequence
       - Get a single value
     - Factorial
       - Get the value
     - IsPrime
       - internally it will loop with a counter
         - What's the most efficient way? (`Math.sqrt()` as the stopping point)
       - We can call IsPrime inside a loop to find all the prime numbers up to 500
     - Loop through numbers to find all the "perfect squares" (square root is a whole number) up to 1000
     - Find all the factors of a number
       - Accept a call-back function
         - Display to the console
         - Append to a DOM element's `.innerHTML`
     - IsPerfect - the number is the product and sum of all its factors
       - Do this **without** an array by having two callbacks to the `findFactors()` example above
     - **Loop within a loop**
       - Multiplication table as an HTML Table
       - *Prep for **In-Class-5***
1. JavaScript Arrays
   - Declare empty array - `[]` - and initialize array with values
   - `.length` and `.push()` and `.pop()`
   - Arrays of
     - strings
     - numbers
     - "mixed" types
   - `.join()`
   - Manually looping through the array
     - to aggregate (equivalent of `.reduce()`)
     - to search (equivalent of `.find()`)
   - Arrays and indexes; e.g.:
     - direct access
     - use in a traditional `for` loop
     - *for-in* vs. *for-of*
   - Arrays as arguments/parameters to functions
   - Returning Arrays from functions
1. Node Collections vs. Arrays
   - Similarities
     - Array Indexers
   - Differences
     - Lacks the *`Array`* methods
     - `.size` vs. `.length`
1. Fetch API
   - Promises and async/await
   - Fetch in your "domain"
   - Fetch outside your "domain"
     - Option Headers
1. DOM API
   - Creating Elements & Nodes
     - `document.createElement()`
     - `document.createTextNode()`
   - Shadow DOM vs. DOM Fragments vs. DOM
   - Moving Elements in the DOM
     - Drag'n'Drop
1. Timers
   - `setTimeout()` and `clearTimeout()`
   - `setInterval()` and `clearInterval()`
   - `setImmediate()` and `clearImmediate()`
1. Array API
   - Array functions:
   - `Array.from()`
1. --- others ---
1. Advanced Objects
   - Constructor function and `new`
   - Classes
   - Prototypes
   - Prototypical Inheritance
1. Advanced Functions
   - Returning functions from functions
   - Promises and Async functions
1. Destructuring Assignments
   - Destructuring Arrays

      ```js
      let name = "Stewart Andrew Dent"
      // When destructuring arrays, you can make your own
      // variable names for the resulting values.
      let [first, middle, last] = name.split(" ")
      // You can use the spread operator to grab a "chunk"
      // of values into their own array.
      let [...givenNames, surname] = name.split(" ")
      ```

   - Destructuring Object

      ```js
      let person = {
         fullName: "Stewart Archie Dent",
         suffix: "Jr."
         born: new Date("Feb 29, 2000")
      }
      // When destructuring objects, your variables names
      // must match the property names. If you use a name
      // that doesn't exit on the object, then you get an
      // undefined value.
      let { fullName, suffix, born, age } = person
      ```
1. Vanilla JavaScript Components
   - Have students read/implement/adapt the samples from the article ["The Vanilla JavaScript Component Pattern"](https://dev.to/megazear7/the-vanilla-javascript-component-pattern-37la)
   - 
1. Other Node Project Types
   - JavaScript Console Applications
   - Web Applications on Frameworks
1. TBD

----

1. Introduction to JavaScript (*Week 1*)
   - [**003**](./003/ReadMe.md) - JavaScript in the Browser
   - [**004**](./004/ReadMe.md) - JavaScript in your Web Page
   - [**005**](./005/ReadMe.md) - JavaScript Variables
1. Functions and Events (*Weeks 2 & 3*)
   - [**006**](./006/ReadMe.md) - Intro to Functions in JavaScript
   - [**007**](./007/ReadMe.md) - Creating JavaScript Functions
   - [**008**](./008/ReadMe.md) - Form Input and Handling Events
   - [**009**](./009/ReadMe.md) - Waiting for the DOM
   - [**010**](./010/ReadMe.md) - Debugging JavaScript
   - [**011**](./011/ReadMe.md) - Organizing Functions in JavaScript
1. Making Decisions (*Week 4*)
   - [**012**](./012/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. Loops and Arrays (*Weeks 5 & 6*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. JS Objects (*Weeks 7 & 8*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. Fetch Fundamentals (*Week 9*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. DOM API & Timers (*Week 10*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. NPM, Tools, ES Modules (*Weeks 11 & 12*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. Class, Object, Prototypes (*Weeks 13 & 14*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
1. Extra Topics (*Week 15*)
   - [**01**](./01/ReadMe.md)
   - [**01**](./01/ReadMe.md)
