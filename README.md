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
- *Functions:* 1) can be assigned to a variable; 2) can be passed as an argument to another function; 3) can be returned from another function; NOTE: Never initialise a function inside a loop! (Instead make a function and inside it make a loop).
- *Higher-order functions:* functions returning another function.
- *Closures:* JS-engine ensures that a function has access to all the variables outside of the function within the closure (it puts the variable to a closure, if it´s referenced by a child-function) - Lexical scoping. Benefits: 1) Memory efficient (fn runs only once and then has variables stored in closure). 2) Encapsulation (hiding informations, it´s not visible for the outside / can not be changed from outside).
- *Prototypal inheritance:* an object gets access to methods and properties of another object (its prototype). / Don´t use obj.__proto__ (because of performance). Instead use `let socrates = Object.create(human);` / To find out what is inherited and what is "own": `obj.hasOwnProperty();` and `obj.isPrototypeOf();` / (In Java, C#, ... is *classical inheritance*). 

- *Object Oriented Programming:* paradigm, how to organise code. / In Java, C#, Ruby, Python. 
- *Factory functions:* create objects (return new objects).
- *Object.create():* to create prototype chain. (True prototype-inheritance.)
- *Constructor functions:* (they don´t return anything) / `function Elf (name, weapon) {this.name = name, this.weapon = weapon};` / To use constructor function we need to use the `new`-keyword: `const peter = new Elf ("Peter", stones")`. / We can add new properties: `Elf.prototype.attack = function () {return ..... }` 

