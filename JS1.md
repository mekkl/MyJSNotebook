```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```typescript
var s = "TypeScript syntax highlighting";
alert(s);
```

```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

## Explain and Reflect:

### Explain differences between Java and JavaScript. You should include both topics related to the fact that Java is a compiled language and JavaScript a scripted language, and general differences in language features.

#### Both Can Run in a Browser
JavaScript runs on most modern browsers, and most websites take advantage of this to enhance the user’s experience. Java applets can also run in a browser, but they have been declining in popularity for various reasons, including compatibility and security. It is reasonable to expect a website visitor to have JavaScript enabled and it is common for a website visitor to have Java applets disabled, especially with the proliferation of mobile browsers.

#### Both Can Run on a Server
Java has long been a major workhorse of the web with application servers like WebSphere, JBoss, and Apache Tomcat running a large portion of the web applications seen by users on both public sites and behind corporate firewalls. While JavaScript has dabbled in the server-side realm for a while, the recent popularity of Node.js is causing more JavaScript-powered application servers to pop up all over the place.

#### Compiled vs. Interpreted
Java code is typically written in an Integrated Development Environment (IDE) and compiled into bytecode. This bytecode is not readable by humans and any Java Virtual Machine (JVM) should be able to run it. JavaScript code is normally executed by a JavaScript engine in the same syntax in which it is written, although JavaScript files that are sent over the internet are often compressed into a barely readable format to reduce their size. Making changes in Java application environments can require several steps using specialized software to compile and deploy the changes, while making changes to JavaScript can sometimes be done with just a simple text editor.

#### Both Are Influenced by the Programming Community
Java uses the Java Community Process to accept input on what to include in the language in the form of Java Specification Requests. Oracle, the current owner of Java, uses these to determine the official implementation of the language. JavaScript, on the other hand, is a derivative of ECMAScript which is defined by the European Computer Manufacturers Association (ECMA), a non-profit standards organization. Without open processes like these, programming languages have a tendency to become obsolete and more proprietary, thus creating vendor lock-in to an inferior product.

#### Write-once, Run-anywhere vs. Branching Madness
Java is specifically designed to enable developers to write their code once and deploy it to any operating system without making changes. In general, this does work as designed, although sometimes there are hiccups depending on the JVM and the code used. Although JavaScript has a standard through ECMAScript, it is much more susceptible to the differences in execution environments (normally in the form of different browsers). While it is very frustrating for developers to write JavaScript code for different environments, one silver lining is that the program itself can query the environment to decide what branch of code to run for that specific environment.

#### Two-Stage vs. Runtime-only Debugging
Java is compiled before it can be run, so if there are any structural problems with code they become apparent very quickly. Once it is running, IDEs often enable the developer to attach to the JVM to debug in real-time. JavaScript is not compiled in the same way, so all bugs are found at runtime. As such, the debugging capabilities of JavaScript are highly dependent on the execution environment and this can vary quite a bit.

#### Both Have Libraries and Frameworks
Libraries and frameworks help programmers by providing access to general and purpose-specific code that can be reused over and over again for different products. When used properly, libraries and frameworks can cut development time – sometimes by a very significant factor. Both Java and JavaScript are mature enough to have a wide range of library and framework options available to assist developers in a variety of scenarios.

#### Static vs Dynamic Type Checking. 
Java uses static type checking, where the type of a variable is checked at compile-time. The programmer must specify the type (integer, double, string, etc.) of any variable they create. JavaScript, like most scripting languages, uses dynamic typing, where type safety is verified at runtime. It is not required for a programmer to specify the type of any variable they create. There are many pros and cons for these two paradigms, but the primary advantage of static type checking is that type errors are caught early in development, and because the compiler knows exactly what data types are being used, code typically executes faster or uses less memory. The primary advantage of dynamic type checking is programmer productivity—you are free to assign types at your leisure.

#### Concurrency. 
The ability to handle the execution of several instruction sequences at the same time is handled very differently between Java and JavaScript. Java makes use of multiple threads to perform tasks in parallel. JavaScript, particularly as it exists as Node.js in server-side applications, handles concurrency on one main thread of execution via a queue system called the event loop, and a forking system called Node Clustering. For most use-cases, both methods work just fine, but Java is generally faster because thread to thread memory sharing much faster than interprocess communication (IPC).

#### Class Based vs Prototype Based. 
Java follows class based inheritance—a top down, hierarchical, class-based relationship whereby properties are defined in a class and inherited by an instance of that class (one of its members). In JavaScript, inheritance is prototypal—all objects can inherit directly from other objects. Hierarchy is accomplished in JavaScript by assigning an object as a prototype with a constructor function.

### Explain the two strategies for improving JavaScript: ES6 (es2015) + ES7, versus Typescript. What does it require to use these technologies: In our backend with Node and in (many different) Browsers

#### Babel is a JavaScript compiler
Babel is a toolchain that is mainly used to convert ECMAScript 2015+ (ES6+) code into a backwards compatible version of JavaScript in current and older browsers or environments. Here are the main things Babel can do for you:
- Transform syntax
- Polyfill features that are missing in your target environment (through @babel/polyfill)
- Source code transformations (codemods)
- And more! (check out these videos for inspiration)

#### TypeScript
TypeScript er et programmeringssprog der er en udvidelse af JavaScript, som giver mulighed for at angive typer i koden og definere klasser, interfaces og moduler som det kendes fra sprog som fx C# og java. Det består bl.a. af en compiler der genererer javascript som resultat.

### Explain generally about node.js, when it “makes sense” and npm, and how it “fits” into the node echo system.


#### Node.js
Node.js is a JavaScript run-time environment. Sounds great, but what does that mean? How does that work?

The Node run-time environment includes everything you need to execute a program written in JavaScript.

![](https://cdn-images-1.medium.com/max/1600/1*sYPllpcAZLHmpuQSRPuO0Q.png)

Node.js came into existence when the original developers of JavaScript extended it from something you could only run in the browser to something you could run on your machine as a standalone application.

Now you can do much more with JavaScript than just making websites interactive.

JavaScript now has the capability to do things that other scripting languages like Python can do.

Both your browser JavaScript and Node.js run on the V8 JavaScript runtime engine. This engine takes your JavaScript code and converts it into a faster machine code. Machine code is low level code which the computer can run without needing to first interpret it.

    "Node.js uses an event-driven, non-blocking I/O model that makes it lightweight and efficient."

Using a non-blocking request, you can initiate a data request for user2 without waiting for the response the request for user1. You can initiate both requests in parallel.

This non-blocking I/O eliminates the need for multi-threading, since the server can handle multiple requests at the same time.

#### npm
npm is a package manager for Node.js with hundreds of thousands of packages. Although it does create some of your directory structure/organization, this is not the main purpose.

The main goal, as you touched upon, is automated dependency and package management. This means that you can specify all of your project's dependencies inside your package.json file, then any time you (or anyone else) needs to get started with your project they can just run npm install and immediately have all of the dependencies installed. On top of this, it is also possible to specify what versions your project depends upon to prevent updates from breaking your project.

It is definitely possible to manually download your libraries, copy them into the correct directories, and use them that way. However, as your project (and list of dependencies) grows, this will quickly become time-consuming and messy. It also makes collaborating and sharing your project that much more difficult.

Hopefully this makes it more clear what the purpose of npm is. As a Javascript developer (both client-side and server-side), npm is an indispensable tool in my workflow.

### Explain about the Event Loop in Node.js

### Explain (some) of the purposes with the tools Babel and WebPack, using examples from the exercises



### Explain the purpose of “use strict” and Linters, exemplified with ESLint 



## Explain using sufficient code examples the following features in JavaScript. 

### Variable/function-Hoisting
One of the trickier aspects of JavaScript for new JavaScript developers is the fact that variables and functions are "hoisted." Rather than being available after their declaration, they might actually be available beforehand. How does that work? Let's take a look at variable hoisting first.

```javascript
// ReferenceError: noSuchVariable is not defined
console.log(noSuchVariable);
```

This is more or less what one would expect. An error is thrown when you try to access the value of a variable that doesn't exist. But what about this case?

```javascript
// Outputs: undefined
console.log(declaredLater);

var declaredLater = "Now it's defined!";

// Outputs: "Now it's defined!"
console.log(declaredLater);
```

What is going on here? It turns out that JavaScript treats variables which will be declared later on in a function differently than variables that are not declared at all. Basically, the JavaScript interpreter "looks ahead" to find all the variable declarations and "hoists" them to the top of the function. Which means that the example above is equivalent to this:

```javascript
var declaredLater;

// Outputs: undefined
console.log(declaredLater);

declaredLater = "Now it's defined!";

// Outputs: "Now it's defined!"
console.log(declaredLater);
```

One case where this is particularly likely to bite new JavaScript developers is when reusing variable names between an inner and outer scope. For example:

```javascript
var name = "Baggins";

(function () {
    // Outputs: "Original name was undefined"
    console.log("Original name was " + name);

    var name = "Underhill";

    // Outputs: "New name is Underhill"
    console.log("New name is " + name);
})();
```

In cases like this, the developer probably expected __name__ to retain its value from the outer scope until the point that __name__ was declared in the inner scope. But due to hoisting, __name__ is __undefined__ instead.

Because of this behavior JavaScript linters and style guides often recommend putting all variable declarations at the top of the function so that you won't be caught by surprise.

So that covers variable hoisting, but what about function hoisting? Despite both being called "hoisting," the behavior is actually quite different. Unlike variables, a function declaration doesn't just hoist the function's name. It also hoists the actual function definition.

```javascript
// Outputs: "Yes!"
isItHoisted();

function isItHoisted() {
    console.log("Yes!");
}
```

However, __function definition hoisting only occurs for function declarations__, not function expressions. For example:

```javascript
// Outputs: "Definition hoisted!"
definitionHoisted();

// TypeError: undefined is not a function
definitionNotHoisted();

function definitionHoisted() {
    console.log("Definition hoisted!");
}

var definitionNotHoisted = function () {
    console.log("Definition not hoisted!");
};
```

However, __function definition hoisting only occurs for function declarations__, not function expressions. For example:

### this in JavaScript and how it differs from what we know from Java/.net.

In most cases, the value of __this__ is determined by how a function is called. It can't be set by assignment during execution, and it may be different each time the function is called. ES5 introduced the bind method to set the value of a function's this regardless of how it's called, and ES2015 introduced arrow functions which don't provide their own __this__ binding (it retains the this value of the enclosing lexical context).

### Function Closures and the JavaScript Module Pattern

#### Function Closures
JavaScript variables can belong to the __local__ or __global__ scope. Global variables can be made local (private) with closures.

A function can access all variables defined inside the function, like this:

```javascript
function myFunction() {
    var a = 4;
    return a * a;
}
```

But a function can also access variables defined outside the function, like this:

```javascript
var a = 4;
function myFunction() {
    return a * a;
}
```

A local variable can only be used inside the function where it is defined. It is hidden from other functions and other scripting code.

```javascript

function myFunction() {
    var a = 4;
}

// ReferenceError: a is not defined
console.log(a)

```
#### JavaScript Module Pattern
JavaScript doesn’t have privacy, but creating new scope emulates this when we wrap all our function logic inside them. The idea then is to return only the parts we need, leaving the other code out of the global scope.

After creating new scope, we need to namespace our code so that we can access any methods we return. Let’s create a namespace for our anonymous Module.

I distinguish between private variables/methods? The _ character! You’ve probably seen this dotted around the web, and now you know why we do it:

```javascript
var Module = (function () {

  var _privateMethod = function () {
    // private stuff
  };

  var publicMethod = function () {
    _privateMethod();
  };
  
  return {
    publicMethod: publicMethod
  };

})();
```

### Immediately-Invoked Function Expressions (IIFE)



Now, whether you define a function like function foo(){} or var foo = function(){}, what you end up with is an identifier for a function, that you can invoke by putting parens (parentheses, ()) after it, like foo().

a function statement always starts with the function keyword. Whenever JavaScript sees function keyword as the first word in a valid statement, it expects that a function definition is going to take place. So to stop this from happening, we are prefixing “!” in-front of the function keyword on line 1. This basically enforces JavaScript to treat whatever that’s coming after “!” as an expression.

The most widely accepted way to tell the parser to expect a function expression is just to wrap it in parens, because in JavaScript, parens can’t contain statements. At this point, when the parser encounters the function keyword, it knows to parse it as a function expression and not a function declaration.

```javascript
// Variation 1
(function() {
    alert("I am an IIFE!");
}());

// Variation 2
(function() {
    alert("I am an IIFE, too!");
})();
```

Not only IIFEs can return values, but IIFEs can also take arguments while they are invoked. Let’s see a quick example.

```javascript

(function IIFE(msg, times) {
    for (var i = 1; i <= times; i++) {
        console.log(msg);
    }
}("Hello!", 5));
```

### JavaScripts Prototype

### User defined Callback Functions (writing your own functions that takes a callback)

### Explain the methods map, filter and reduce

### Provide examples of user defined reusable modules implemented in Node.js


## ES6-7 and TypeScript

### Provide examples and explain the es2015 features: let, arrow functions, this, rest parameters, de-structuring assignments, maps/sets etc.

### Explain and demonstrate how es2015 supports modules (import and export) similar to what is offered by NodeJS.

### Provide an example of ES6 inheritance and reflect over the differences between Inheritance in Java and in ES6.
### Provide examples with es6, running in a browser, using Babel and Webpack

### Provide an number of examples to demonstrate the benefits of using TypeScript, including, types, interfaces, classes and generics

## Callbacks, Promises and async/await

### Explain about promises in ES-6 including, the problems they solve, a quick explanation of the Promise API and:

#### Example(s) that demonstrate how to avoid the callback hell  (“Pyramid of Doom")

#### Example(s) that demonstrate how to execute asynchronous (promise-based) code in serial or parallel

#### Example(s) that demonstrate how to implement our own promise-solutions.

#### Example(s) that demonstrate error handling with promises

### Explain about JavaScripts async/await, how it relates to promises and reasons to use it compared to the plain promise API.

#### async
The async function declaration defines an asynchronous function, which returns an AsyncFunction object. An asynchronous function is a function which operates asynchronously via the event loop, using an implicit Promise to return its result. But the syntax and structure of your code using async functions is much more like using standard synchronous functions.

#### Promise
The await expression causes async function execution to pause until a Promise is resolved, that is fulfilled or rejected, and to resume execution of the async function after fulfillment. When resumed, the value of the await expression is that of the fulfilled Promise.

If the Promise is rejected, the await expression throws the rejected value.

If the value of the expression following the await operator is not a Promise, it's converted to a resolved Promise.

#### Why to use it
__Error handling__: Async/await makes it finally possible to handle both synchronous and asynchronous errors with the same construct, good old try/catch.

__Error stacks__: The error stack returned from a promise chain gives no clue of where the error happened. Even worse, it’s misleading; the only function name it contains is callAPromise which is totally innocent of this error (the file and line number are still useful though).

However, the error stack from async/await points to the function that contains the error

__Intermediate values__: You have probably found yourself in a situation where you call a promise1 and then use what it returns to call promise2, then use the results of both promises to call a promise3. Your code most likely looked like this

```javascript
const makeRequest = () => {
  return promise1()
    .then(value1 => {
      // do something
      return promise2(value1)
        .then(value2 => {
          // do something          
          return promise3(value1, value2)
        })
    })
}
```

This same logic becomes ridiculously simple and intuitive with async/await. It makes you wonder about all the things you could have done in the time that you spent struggling to make promises look less hideous.

```javascript
  const makeRequest = async () => {
  const value1 = await promise1()
  const value2 = await promise2(value1)
  return promise3(value1, value2)
}
```

__Debugging__, a killer advantage when using async/await is that it’s much easier to debug. Debugging promises has always been such a pain for 2 reasons

1. You can’t set breakpoints in arrow functions that return expressions (no body).
2. If you set a breakpoint inside a .then block and use debug shortcuts like step-over, the debugger will not move to the the following .then because it only “steps” through synchronous code.

With async/await you don’t need arrow functions as much, and you can step through await calls exactly as if they were normal synchronous calls.


#### Provide examples to demonstrate why this often is the preferred way of handling promises

#### Error handling with async/await

```javascript
const makeRequest = async () => {
  try {
    // this parse may fail
    const data = JSON.parse(await getJSON())
    console.log(data)
  } catch (err) {
    console.log(err)
  }
}
```

#### Serial or parallel execution with async/await.

```javascript
async function serial(count) {
    peopleList = [];
    for (let i = 1; i < count; i++) {
        peopleList.push(
        // Her vil 'await' blokke for videre kørsel af koden 
        await fetch("https://swapi.co/api/people/" + i)
            .then(res => { return res.json() }));
    }
    return peopleList
}

async function parallel(count) {
    peopleList = [];
    for (let i = 1; i < count; i++) {
        peopleList.push(
        fetch("https://swapi.co/api/people/" + i)
            .then(res => { return res.json() }));
    }
    peopleList = await Promise.all(peopleList);
    return peopleList
}

//Time each of the two strategies
```
