# My Way (Back) To Coding (2022)

This is a log of my way (back) to coding in 2022.

## Intro
In 2017 (during my maternity leave) I came across web development and enjoyed learning how to build webpages from scratch. It was like magic! :-) When I later came to JavaScript, I was excited even more. I love to think about what needs to be done, plan how to do it, how to divide it into smaller logical chunks, how these influence each other. 

I wanted to see the bigger picture and understand how all the things work together, so I learned also basics of other connected technologies on the backend. 

I learned mostly from various online courses (Udemy, FreeCodeCamp, Codecademy and others), and later (when the family-situation allowed it) also in-site courses (mostly by Czechitas) and attended frontend-meetups. 

During my way I learned:
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

In 2019 (at the end of my maternity leave) I was so excited about this area, that I planned not to go back to my previous work at the university, but I decided to change my career and go to the world of coding. However, when I was handing my notice to my boss, she was interested in my motivations and plans for the future, and finally I got an offer to another work-challenge. It was really hard to find the final decision, but I went for it and (for the time being) left the idea of IT. At this position, I learned a lot, had many challenges, discovered new areas and it has been a great experience. 
But 3 years later, in 2022, I still feel attracted to coding. So I got back to it and started again to revise and expand my knowledge of these topics. 

## April 2022 
I revised the basics of HTML and CSS, and also the theory of JavaScript. 
I decided to create my own project: [LOGIC-game](https://github.com/marieval/logic-game). (It´s a favorite board game of my son, so I decided to create an electronic version of this game.)

**LOGIC-game:**
- I started by simple HTML & CSS, created the wireframe of the JS-logic needed for the game and started the JS-logic and step-wise improved it.
- I was excited when I realized that after stumbling across some bugs I remember a lot of stuff and am able to find the bugs and solve the problems quite quickly. Even when I don´t remember the details, I often know what to look for as I already heard about the problem earlier.

## May 2022
My [LOGIC-game](https://github.com/marieval/logic-game) is working great, but I still have ideas how to improve it, so it´s not finished.
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

## June 2022
I revised some stuff from the course [The Complete Web Developer in 2022: Zero to Mastery](https://www.udemy.com/course/the-complete-web-developer-zero-to-mastery/): 
- DOM manipulation
- CommandLine
- Fundamentals of React

I wanted to join a simple open-source project to practice my knowledge. I searched for some projects but these required more experience than I have. So for this moment I left this idea.

## July 2022
I came accross the term ***"headless solution"*** and searched more about what that means: *Headless* means software application or program without frontend (it´s connected to another FE-application or interface through API).
   
**Headless x Coupled x Decoupled CMS:**
- *Coupled CMS:* contains two tightly connected parts (frontend & backend). Example of coupled CMS: WordPress
- *Headless CMS:* without frontend part. They distribute their content to other systems (websites, mobile apps, social networks, mailers,...). The content can be used on different systems and platforms. 
- *Decoupled CMS:* contains FE-part, but the architecture strictly separates FE and BE (so that eventually only the FE part can be completely changed / switched to other technology).
   
**Types of headless CMS:**
- *API-based headless CMS:* The content is stored in databases and are served through API (usually REST or GraphQL). Examples: Contentful, DatoCMS, Strapi.
- *Git-based headless CMS:* They don´t store content in databases, instead they use Git. Examples: Netlify CMS, Jekyll Admin, Forestry.

**Advantages of headless systems:** Centralised storage of data (can be then distributed to different places and systems). Change of frontend is much easier. Higher security (it´s easier to properly secure the API than whole website). Scalability (lower need for performance). Higher flexibility (various technologies and solutions can be chosen for processing of the data).

## August 2022
**Big O:**
- [Big O cheatsheet](https://www.bigocheatsheet.com/)
- O(1) --> constant time / (No loops)
- O(log N) --> logarithmic / (usually searching algorithms have log n if they are sorted (binary search))
- O(n) --> linear time / (for loops, while loops through n items)
- O(n log(n)) --> Log linear / (usually sorting operations)
- O(n^2) --> quadratic time / (every element in a collection needs to be compared to every other element. Two nested loops)
- O(2^n) --> exponential / (recursive algorithms that solves a problem of size N)
- O(n!) -> factorial / (you are adding a loop for every element)
- Iterating through half a collection is still O(n)
- Two separate collections: O(a*b)

**Good code:** 
- Readable
- Speed / Time complexity (operations, comparisons, looping, outside function calls)
- Memory / Space complexity (variables, data structures, function calls, allocations)

**Create-react-app & NPM vs. NPX:**
- NPX downloads and immediately executes the command (runs the package - it´s latest version) and deletes it => it helps not to clutter my workspace!
- by using `npx create-react-app` we use the CRA to start our project and then it´s deleted. (Earlier we had to use `npm create-react-app` and install CRA locally or globally)

**React:**
- with *setState* we should use callback function, so that the code is more clear and readable (the second callback runs after the state is completely updated => expected result):  
```
this.setState(
      () => { return: { name: "Maru"}},
      () => { console.log(this.state)}
   );
```
- *Flow in React:* Constructor runs -> initializes the state -> render the initial component UI -> componentDidMount + update state -> re-render the UI with the updated state.
- *Re-rendering of a component:* 1) when setState is called, 2) when props have changed; (3) forceUpdate() - this shouldn´t be used).
- *Class-components* have lifecycle methods (componentDidMount, componentDidUpdate, componentWillUnmount) and methods like `setState()`. In class-components only render() is re-run.
- *Functional-components* don´t have lifecycle methods, they have hooks (e.g. `useState()`). In functional-components the whole function/component is re-run (when props or state change).   
**Routing in React:**
- *React-Router:* v6 is not backwards compatible with v5! 
-  *BrowserRouter* component: import it to index.js, wrap with this component our whole app.
-  *Routes, Route:* import it in App.js, wrap all the routes with <Routes> component. Specify individual routes inside: `<Route path="/" element={<Homepage />}>`. (When there is `index` as a parameter of a route, it´s rendered as a default route/component.)
- *Outlet:* compontent `<Outlet />` (from react-router-dom) helps us with nesting the routes - it tells where the other portions of code are supposed to be positioned.
- *Fragment:* component `<Fragment />` (imported from react) can serve as wrapping component instead of a div - it renders to nothing (so there are no unnecessary divs in the end)
- *Link:* from react-router-dom, `<link classname="nav-link" to="/shop">SHOP</Link>`. 
- *Using svg in react:* we import ReactComponent (`import { ReactComponent as MyLogo } from "../../assets/myLogo.svg;` and then we can us it as a component `<MyLogo className="logo" />`

**GitHub & Markdown:**
- I like using markdown (I use it even for notes-taking (in Obsidian)) and I just came across some new things there: `~~Strike through~~` is this: ~~Strike through~~, subscript `H<sub>2</sub>0` makes this: H<sub>2</sub>0, superscript `X<sup>2</sup>` makes this: X<sup>2</sup>.

**Arrays:**
- search: O(n) / lookup: O(1) / push: O(1) / insert: O(n) / delete: O(n). (Lookup: finding the keys. Search: look for keys when we don´t know the keys)
- difference between static and dynamic arrays (according to language - e.g. C++ has static arrays - the size of the array must be allocated ahead; / arrays in JavaScript, Python, arraylists in Java: are dynamic - the memory is not allocated ahead, but it is done dynamically). With dynamic arrays: according to the situtation, append/push can be O(n)!!!
- *Pros of arrays:* fast lookup, fast push/pop, ordered in memory. *Cons of arrays:* slow insert, slow delete

**Hash-tables:**
- in various languages: objects in JS, dictionaries in Python, maps in Java, hashes in Ruby
- search: O(1) / insert: O(1) / lookup: O(1) / delete: O(1). // Lookup can be O(n), when hash collisions happen!  (Lookup: finding the keys. Search: look for keys when we don´t know the keys)
- in JS are also *maps* (`const a = new Map();`): keys in maps can be any data-type and it maintains the insert-order (-> difference from objects)
- *Pros of hash tables:* fast lookups (without collisions -> possible solution of collision: linked list), fast inserts, flexible keys. *Cons of hash tables:* unordered, slow key iteration.
- With using hash tables we can improve time complexity (but tradeoff: increased space complexity)

**Linked lists:**
- each node contains a value + pointer to the next node. The last element (tail) points to null.
- doubly linked lists: each node contains a value + pointer to the next node + pointer to the previous node
- nodes of linked lists are scattered in memory => traversing is slower than in arrays (is ordered in memory, on the same place)
- not pre-built in JS. 
- prepend: O(1) / append: O(1) / lookup: O(n) / insert: O(n) / delete: O(n)
- *Singly linked lists:* take less memory, are quicker for insertion and deletion. BUT can´t be traversed from the end.
- *Doubly linked lists:* take more memory, can be traversed both from the beginning and the end.
- *Pros of linked lists:* fast insertion, fast deletion, are ordered, have flexible size. *Cons of linked lists:* Slow lookup, take up more memory.

## September 2022
**Stacks & Queues:**
- linear datastructures, can be traversed sequentially, accessed can be only first or last element.
- *Pros of stacks&queues:* fast operations, fast peek, ordered. *Cons of stacks&queues:* slow lookup.

**Stacks:** 
- lookup: O(n) / pop: O(1) / push: O(1) / peek: O(1) (peek = view the last item)
- first in - last out (LIFO)
- important in language-specific engines, in browser history, undo-actions,...
- can be implemented using arrays (are quicker in lookup, cached in memory in one place) or linked-lists (more space (hold pointers), have more dynamic memory, can increase the size) -> decide about choosing according to operations performed

**Queues:** 
- first in - first out (FIFO)
- lookup: O(n) / enqueue: O(1) / dequeue: O(1) / peek: O(1)  (Dequeue = to take first item away)
- can be implemented using linked-lists (NOT using arrays as these are unefficient when removing elements from the beginning)

**Trees:**
- Binary tree: each node has 0/1/2 nodes, each node can have only 1 parent node. *Perfect BT:* all nodes have just 2 children. *Full BT:* all nodes have 0 or 2 children. 
- Perfect BT: in next level 2-times more nodes than in previous level. Amount of nodes in last level = sum of all other levels + 1. / `Number of nodes = 2^number-of-levels - 1`.
- *Binary search-tree:* lookup O(log n) / insert O(log n) / delete O(log n). / Left child: lower; right child: higher. In unbalanced-search-trees: lookup, insert and delete can get to O(n)! ([Visualisation of BST](https://visualgo.net/en/bst?slide=1)).
- *Pros of BST:* better than O(n), ordered, flexible size. *Cons of BST:* There are no O(1) operations.
- *AVL tree & Red/black tree:* trees that automatically rebalance
- *Binary heap:* child nodes are always smaller (in max-heap). Not so well organised as trees. Used in data-storage, in priority queues, sorting algorithms. / lookup: O(n) / insert: O(log n) / delete: O(log n). Heaps add a value to the tree from left to right and then it bubbles up. Binary heaps are memory-efficient. *Pros:* better than O(n), nodes have priority, flexible size, fast insert. *Cons:* slow lookup.
- *Tries:* similar to trees, for strings (used in autocompletion,...). Memory and speed efficient. O(lengt-of-the-word)

**Graphs:**       
- Node = vertex. / Edge = link between nodes.     
- *Types of graphs:* directed x undirected / weighted x unweighted (have weight of the links) / cyclic x acyclic.     
- *Ways to describe graphs:* Edge list, Adjacency list, Adjacency matrix.     
- *Pros of graphs:* show relationships. *Cons of graphs:* scaling is hard.

**Recursion:**
- It´s a function that refers to itself inside of the function.
- Good for tasks that have repeated subtasks to do.
- Every recursive function needs to have *a base case* (= a stop).
- Recursive functions: O(2^n)! Anything we do with a recursion can be done iteratively (with a loop).
- *Pros of recursion:* readability, DRY. *Cons:* large stack
- *Tail call optimization:* methods in various languages that make recursion less memory-demanding.
- *When to use recursion:* traversing or searching through trees and graphs: Every time we are using a tree or converting something into a tree, consider recursion! 

**Sorting:**
- In every language sort methods work differently. In JS `array.sort()` converts the numbers in the array into strings! (The complexity is dependent on implementation -> differs in different browsers.)
- [Sorting algorithms animations](https://www.toptal.com/developers/sorting-algorithms)
- Elementary sorts: bubble sort, insertion sort, selection sort.
- *Bubble sort:* Time complexity: O(n^2), Space complexity: O(1)
- 
