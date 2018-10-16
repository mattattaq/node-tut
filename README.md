# Node Beginner tutorial

## Intro
1. What is node?
* A wrapper around VM like V8 with built-in modules providing rich features through easy-to-use asynchronous APIs
* VM: Virtual Machine
* API: Application Programming Interface
* An API isn’t the same as the remote server — rather it is the part of the server that receives requests and sends responses.

2. Why Node?
* Built-in modules (fs, http, crypto, zip, ...)
* Asynchronouse API (no threads)
* C++ addons
* Debugger and other utilities
* NPM
* Module dependency manager (referred to as CommonJS)
* One language through the whole stack

3. Some Analogies about Node
1. Node is like a baking recipe where the installs are the ingredients / tools
```
// THe making of a cupcake
// First steps:

$ npm install cake-mix
$ npm install cupcake-pan
```
[from FreeCodeCamp](https://medium.freecodecamp.org/hard-coding-concepts-explained-with-simple-real-life-analogies-280635e98e37)

2. Callbacks are like ordering coffee from Starbucks. You initiate the exchange and wait until the drink is ready to get the payload (latte). This is an example of Asynchronous Programming.

## Getting started with Node
1. REPL
* Read-Eval-Print-Loop
* In terminal or environment that reads your code, evaluates it, prints, and then waits for your response. Similar to sql environment in terminal.
* `.help` lists commands in REPL environment
* can run files via `node [filepath]`
2. Timers: setTimeout || setInterval
* setTimeout sets a timer in thousands of a second which delays execution of code
* ```setTimeout(func, delay, arg1, arg2, arg3, ...)```
* setInterval sets an interval for a repeating function or action (can be infinite)
* clearTimeout is used to stop a function with a setTimeout()
* clearInterval stops a function that has a setInterval() method
```js
//print "Hello world" every seconds for 5 seconds
//then print "Done and exit"
// set iterator
let counter = 0;
// make a function that sets an interval that fires off every second
// and increases counter
const intervalId = setInterval(()=>{
    console.log('Hello World');
    counter += 1;

    if(counter === 5) {
        console.log('Done');
        clearInterval(intervalId);
    }
}, 1000);
```
* setTimeout(func, delay, arg1, arg2, etc... );
```js
//example
const rocks = who => {
    console.log(who + ' rocks');
}

setTimeout(rocks, 2 * 1000, 'Pluralsight');
```

* setInterval - The setInterval() method calls a function or evaluates an expression at specified intervals (in milliseconds).

The setInterval() method will continue calling the function until clearInterval() is called, or the window is closed.

The ID value returned by setInterval() is used as the parameter for the clearInterval() method.

* Counter challenge
```js
//print 'Hello World' once every second five times then print 'Done' in the console
let counter = 0;
const intervalId = setInterval(()=>{
    console.log('Hello World');
    counter += 1;

    if(counter === 5) {
        console.log('Done');
        clearInterval(intervalId);
    }
}, 1000);
```
## Modern JavaScript
* is `{{{}}}` valid js? `Yes`
* {} = block scopes
```js
{{{ var a=42;}}} console.log(a);
///yeilds 42
```
* const = constant reference to a variable
* let = variable that can't be accessed outside of block scope


## NPM: Node Package Manager

## Modules and Concurrency

## Working with Web Servers

## Working with Operating Systems

## Links
* [Node API Docs v9](https://nodejs.org/docs/latest-v9.x/api/)
