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
1. --- others ---
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
