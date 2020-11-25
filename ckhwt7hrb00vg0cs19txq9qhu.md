## ES6 and the road to react



The thing with JavaScript is that it takes a week to learn the basics but ages to understand it completely. Even though I have worked with JavaScript a lot, I still get stuck and feel uncomfortable sometimes. So this week I decided to dive deep into it. 

### 📔 I don't know Js yet
Tutorials are great but they don't provide a deeper understanding of the language. So I picked a book series called **"You don't know Js"** by Kyle Simpson. It focuses on the core mechanisms of the JavaScript language. After going through a few chapters I had to say that I don't know Js yet.


![screenshot (67).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1605794885239/gJ4hCTT1h.png)

Its first edition is free to read on [GitHub](https://github.com/getify/You-Dont-Know-JS/blob/1st-ed/README.md). And I would highly recommend for anyone who wants to deeply understand JavaScript.

### ⚛ ES6 and react
If you have spent enough time with JavaScript and want to jump straight to learning react, Wait. Have you learned about ES6? Because If you haven't, you might want to change your mind. Let's see why.

### 🤷‍♂️ What is ES6 and Why it's important?

ES6 is the 6th version of ECMAScript, (*a standardized name for JavaScript*) which was released in 2015 with new features and enhancements. And react uses some of its features like classes, modules, destructuring, etc. So if you don't want to scratch your head and wonder what's happening while learning react, Take some time and learn ES6. It will help you understand react better and easily.

I will give you a brief idea about some of its features.

### let and const
Earlier we used `var` for declaring variables which is function scoped, but ES6 introduced two new ways. i.e. `let` and `const` which are block-scoped. Anything inside { } is a block. for ex. for loop, if-else.
```js
// value can be changed.
let someVariable = 12; 

// read-only, value cannot be changed
const PI = 3.14;
```

### Template literals
Template literals are another way of creating strings. You can create multiline strings and can embed variables and expression using `${expression}` syntax.

```js
let age = 20;
console.log(`Hi, I am Rutik, I am ${age} years old.`)   
// Hi, I am Rutik, I am 20 years old.

```
### Arrow functions
Arrow functions are mainly syntactic sugar for defining function expressions. 
```js
// Regular function
function sum (a,b){
return a+b;
}

//Arrow Function
var sum = (a,b) => { return a+b; }
```
The primary use case of arrow functions is for functions that get applied over and over again to items in a list. For example, if you have an array of values that you want to transform using a map, an arrow function is ideal.
But we can't use arrow functions in every situation. There are certain limitations. [read more](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
> 
In arrow functions, the behavior of `this` is different. Arrow functions do not default `this` to the window scope, rather they execute in the scope they are created.


### Modules 
A module is nothing but a JavaScript code written in a separate file. Before ES6 we had to use libraries like CommonJS, requireJS, etc to work with modules. But now with ES6, JavaScript has its own built-in modules. The idea is to access a piece of code, only when needed.

#### Import and export
If we want something declared in a module to be available somewhere else, we export that module using an export statement. You can export any top-level function, class, var, let, or const.
```js
// utils.js
export const pi = 3.14;
export function add(x, y){
    return x + y;
}

```
All this exported code will be available where we import it.
```js
// app.js
import {pi, add} from utils;

```
We will use the same concept while dealing with components in react. 

### Class
ES6 introduced a new syntax for creating a class.

```js
class Person { 
  constructor(name, role) {
    this.name = name;
    this.role = role;
  }
  
   sayHi() {
    return ('Hi ! I am ' + this.name + ', I am a ' + this.role);
  }
}

let person1 = new Person("Rutik", "Frontend developer");

person1.sayHi(); 
// returns "Hi ! I am Rutik, I am a Frontend developer"
```

### Destructuring
 Destructuring, the name itself suggests breaking down a complex structure into small individual parts. We can break down an array or object into individual variables.

#### Array Destructuring

```js
let a, b;
[a, b] = [10, 20];
console.log(a); // 10
console.log(b); // 20
```

#### Object Destructuring
```js
const student = {
    firstname: 'Jhon',
    lastname: 'Doe'
};

// Object Destructuring
const { firstname, lastname } = student;

console.log(firstname, lastname); // Jhon Doe
```

You will use these concepts in useState hook or while sending props to a component in react.

And there are more such features like
- promises
- default function parameters
- rest operator
- spread operator
- and many more.

A good grasp of these concepts will help you in the early stages of learning react. Next, I started with react fundamentals and brushed up a few basic concepts like components, props, state, etc. I Will talk about it more in the next week. Till then goodbye.

--------------------------
I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade). Also, subscribe to my newsletter and stay up-to-date with my latest blog posts.

⚡ Happy learning!

