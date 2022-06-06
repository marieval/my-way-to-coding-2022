# My Way To Coding (2022)

This is a log of my way (back) to coding in 2022.

## Intro
In 2017, during my maternity leave, I came across web development and I decided to learn how to build webpages from scratch. When I later came to JavaScript, I was excited even more. I love to think about what needs to be done, plan how to do it, how to divide it into smaller logical chunks, how these influence each other. 

I wanted to see also the bigger picture and understand how all the things work together, so I learned also basics of other connected technologies on the backend. 

I learned mostly from online courses (Udemy, FreeCodeCamp, Codecademy and others), in-site courses (mostly by Czechitas) and attended frontend-meetups. 

During my way I learned about:
- HTML5, CSS3, Sass
- JavaScript
- React
- JQuery, Bootstrap, Tachyons
- Git & GitHub
- CommandLine
- Node.js, Express.js
 
And also basics of:
- Gulp, Webpack
- SQL (PostgreSQL, MySQL)
- Java

In 2019 (at the end of my maternity leave) I planned not to go back to my previous work at the university, but I intended to change my career and go to the world of coding. However, I got an offer to another work-challenge, so I went for it and (for the time being) left the idea of IT. 
However, I still felt attracted to coding and 3 years later, in 2022, I got back to it with the plan to revise and expand my knowledge of this topics. 

## April 2022 
I revised the basics of HTML and CSS, and also the theory of JavaScript. 
I decided to create my own project: [LOGIC-game](https://github.com/marieval/logic-game). (It´s a favorite board game of my son, so I decided to create an electronic version of this game.)

**LOGIC-game:**
- I started by simple HTML & CSS, created the wireframe of the JS-logic needed for the game and started the JS-logic and step-wise improved it.
- I was excited when I realized that after stumbling across some bugs I remember a lot of stuff and am able to find the bugs and solve the problems quite quickly.

## May 2022
My [LOGIC-game](https://github.com/marieval/logic-game) is working great, but I still have ideas how to improve it, so it´s not finished yet.
- I improved *logic* of the game, added *modal* at the end of the game.
- I added the action after clicking *New Game* button (At first I tried to avoid reload and instead to re-set all the conditions to the initial state, but there was always some issue, so in the end I solved it simply by reloading of the page.)

I also revised *AJAX and Promises*

I go through the course [JavaScript: The Advanced Concepts](https://www.udemy.com/course/advanced-javascript-concepts/) to remind myself of the JS-topics: 
- I went through the chapters about *JS-engine, Call stack, Memory heap*, *"single-threaded"*, *Garbage collection* (is automatic in JS)
- *Hoisting:* it´s first going through the code and allocating memory for the variables and functions (if *var / function* are the first words on the line!). *var*: partially hoisted (is hoisted as undefined), *function* is fully hoisted.
- *Lexical environment, lexical scope:* in JS our lexical scope (= where it is defined in code) determines our available variables
- *Function scope / block scope:* in JS is function scope (*var*: we get to it from the global-scope, even in an if-statement. When we use *const / let*: it´s block-scoped
- *this-keyword:* has dynamic scope (it´s  important where it was CALLED). BUT if we use *arrow function*: it´s lexically bound! (Earlier it was solved also by *var self = this;* inside of the object).
- *apply(), call():* we use them to "borrow" a method from another object.
- *bind():* when we need to have some function called later already with some context (specific *this*).
- *Passing by reference / by value:* primitive types are passed by value, non-primitive types (objects) by reference.
- *Dynamic / static typing:* in statically-typed languages (Java, C#,...) we must define of what type is the variable. In JS (dynamically typed) the typing is done during the runtime.
- *Weakly typed languages:* JS, C, C++, PHP (have type coercion). x *Strongly typed languages:* Python, Ruby, C#, Java.
- *Functions:* special type of objects - "callable objects". When we invoke them, the *execution context* is created (with *this* and *arguments*), it looks for *variables-environment* (what variables are available), and it creates *scope-chain* (what variables are available in parent environment).
- *Arrow functions:* lexical scope (where it was written)   X   *Regular functions:* dynamic scope (where it was called)
- *`This` in functions inside of methods:* Functions defined inside of methods: `this` is not assigned to object itself, but to the window object!!!
- *Functions:* 1) can be assigned to a variable; 2) can be passed as an argument to another function; 3) can be returned from another function; NOTE: Never initialise a function inside a loop! (Instead make a function and inside it make a loop).
- *Higher-order functions:* functions returning another function.
- *Closures:* JS-engine ensures that a function has access to all the variables outside of the function within the closure (it puts the variable to a closure, if it´s referenced by a child-function) - Lexical scoping. Benefits: 1) Memory efficient (fn runs only once and then has variables stored in closure). 2) Encapsulation (hiding informations, it´s not visible for the outside / can not be changed from outside).
- *Prototypal inheritance:* an object gets access to methods and properties of another object (its prototype). / Don´t use obj.__proto__ (because of performance). Instead use `let socrates = Object.create(human);` / To find out what is inherited and what is "own": `obj.hasOwnProperty();` and `obj.isPrototypeOf();` / (In Java, C#, ... is *classical inheritance*).    
   
- ***Object Oriented Programming:*** paradigm, how to organise code. / In Java, C#, Ruby, Python. 
- *Factory functions:* create objects (return new objects).
- *Object.create():* to create prototype chain. (True prototype-inheritance.)
- *Constructor functions:* (they don´t return anything) / `function Elf (name, weapon) {this.name = name, this.weapon = weapon};` / To use constructor function we use the `new`-keyword: `const peter = new Elf ("Peter", stones")`. / We can add new properties: `Elf.prototype.attack = function () {return ..... }` 
- *Prototype:* only functions have access to their prototype!
- *Classes in JS:* are only syntactic sugar (based on prototypes, not true classes as in Java, C#, ...). / All state and properties are inside of the class. / Functions (=properties, what they can do) are not inside of the constructor-function (because constructor-function is run everytime the class is instantiated, but we want to have just link to one definition of the property for all the instantiations => memory-efficient).
- *Inheritance:* one class is based on another: `class Elf extends Character {constructor(name, weapon, type) {super(name, weapon); this.type = type}}`
- *4 pillars of OOP:* Encapsulation (objects) // Abstraction (hide the complexity from user) // Inheritance (inherit from other classes) // Polymorphism (ability to use method on different objects and have different outputs based on the parameters)
   
- ***Functional Programming:*** separation of concerns - functions & data are separated.
- *1 pillar of FP:* pure functions (Have no side effects. + There is the same output given same input.)
- *Immutability of objects:* all objects created in FP are immutable! (There is no shared state!)
- *"Perfect" function:*: Performs only 1 task. / Has return statement. / Is pure. / Has no shared state. / Has immutable state. / Composable. / Predictable.
- *Idempotence:* given the same input, it gives same output. (When calling x-times, it still has the same result.)  
- *Higher order function:* takes a function as an argument / return a function
- *Closure:* we can use it to create private variables
- *Currying:* change a function taking multiple parameters to multiple functions taking 1 parameter at a time  
- *Partial application:* call a function with one parameter and the others accept at the second call (null: we don´t care about this-argument)
```
const multiply = (a,b,c) => a*b*c;
const partialMultiplyBy5 = multiply.bind(null, 5);
partialMultiplyBy5(4,10); 
```

- *Memoization:* special type of caching: if the parameter is not changed, it remembers the result of a function and doesn´t need to calculate it again.
- *Compose, pipe:* we can combine functions into 1 function (compose: left to right / pipe: right to left).
- *Arity:* number of arguments a function takes (it´s good to have 1-2 arguments in a function).   

***OOP x FP:***
- FP: many operations on fixed data     x    OOP: few operations on common data
- FP: stateless (immutable state)     x     OOP: stateful (we are modifying state)
- FP: with pure functions (without side-effects)     x     OOP: with side effects (methods manipulate the internal state)
- FP: more declarative (what we want to be doing)     x     OOP: more imperative (how we want it to be done)
- FP: can be run on many processors (they don´t influence each other, they can work independently), it´s good in parallelic (distributed) systems

**Asynchronous JS:** 
- *Job queue:* with promises we have also *job queue* = microtask-queue (earlier: only callbeck queue - task queue). Job queue has higher priority than callback queue. Because job-queue is implemented by the browser, there are differencies between individual browsers.
- *Promise.race():* returns just the first-resolved promise.
- *Promise.paralell():* the promises are done in paralell.
- *Promise.sequence():* after one promise is resolved, the other is done.
- *Promise.all():* resolves only if both/all the promises resolve (are fulfilled) ->don´t forget to `catch`!
- *Promise.allSettled():* resolves even when one of the promises is rejected.

**Modules:**
- *Module pattern:* (earlier: just global scope + function scope (+block scope with const/let)), used IIFE. Available are only the things which we return. Disadvantage: order of scripts matters!
- *CommonJS:*  `module.export = {....};` and `var module = require("modul1");` / Is synchronous. Using *browserify* -> bundle.js (combines all thescripts to one js-file)
- *ES6 modules:* `import module1 from "Module1";` and`export function jump() {....};`. It´s necessary to define in HTML `<script type = "module"}....</script>` and it must be run from the server (e.g. live-server)!!!

**Error handling:**
- error is a feature, not a mistake. It stops the program and throws an error. By catching an error: the program doesn´t stop. An error has name, message, stack (where it happened). If the error is not handled, it goes down the call-stack down to the browser (there it´s the runtime catch `onerror()` / In node.js it´s `process.on("uncoughtException")`). 
- Several types of errors: SyntaxError, ReferenceError, ... 
- Node.js handles error differently - it´s another runtime
- *Try-catch-(finally):* works only with syncrhonous code! 
- *Async Error Handling:* with promises we need `.catch(err => {console.log(err)}`. / Inside `async function` can be used also try-catch.
- Error object can be extended: it´s useful e.g. at Node-server when we don´t want others to see the details of the error. 
- Try to handle your errors! Protect it from unexpected behavior! 

**NPM:**
- Node-package-manager
- packages installed globally or locally (only for the individual project or globally on the computer)
- dependencies vs. dev-dependencies
