## A step by step guide to functions in JavaScript

Functions are one of the basic concepts in programming. The name itself suggests, it performs a function. A function is a block of code that you can use whenever you need and wherever you required to avoid repeated code blocks. Once a function is written, it can be used over and over again. They usually take some input, perform some operations on it and produce some output.  

In this article, we will learn about functions in JavaScript, different ways of defining functions, how hoisting and function scope works and a few more concepts regarding functions. Let's begin.

## The function declaration 
Functions are defined, or declared, with the **function **keyword. The declaration begins with the function keyword, followed by the name of the function then set of parentheses, which can be used for optional parameters. The code of the function is contained in curly braces.

```javascript
function nameOfFunction(parameters) {
    // Code to be executed
}
```
Functions allow a programmer to divide a big program into several small and manageable functions.
For example, If you are building a simple calculator then sum() will be a function. It will take two or more integers as input and return the sum as the result. 

```javascript
//function declaration
function sum(a,b){
return a+b;
}
```
The name of the function can be anything, as long as it follows the same rules as declaring variables.
JavaScript functions are written in camel case too. It's a best practice to tell *what the function is doing *by giving the function name a verb as a prefix. Also, the function should perform only one task and have a single responsibility. Thus naming should be based on that one responsibility.

### 📌 Calling Functions
Defining a function does not execute it. Defining it simply names the function and specifies what to do when the function is called. Calling the function performs the specified actions with the indicated parameters. We can call it by writing the name of the function, followed by parenthesis ().

```javascript
//function call
sum(5,3);
//output : 8
```
### 📌 Function Parameters 
Parameters are input that gets passed into functions as names and behave as local variables. A function can have multiple parameters or no parameters at all.
> 
**If you declared a parameter but did not pass an argument to it, your parameter would be undefined. It means that function parameters default to undefined.
**

### 📌 Function arguments
The argument is the actual value that gets passed into the function.

![functionblog1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587151140206/6UMKRMJdW.png)

*You define a function with parameters, you call a function with arguments.* In function sum() a and b are parameters whereas 5 and 3 are arguments.

### 📌 The return Statement
A JavaScript function can have an optional return statement. This is required if you want to return a value from a function. This statement should be last in a function. The return statement stops the execution of a function and returns a value from that function.
A function always returns a value, If the return value is not specified then *undefined* is returned.

## The function expression 
A function expression looks similar to function declarations, except that the function is assigned to a variable name. 
```javascript
var sum=function(a,b){
return a+b;
};

sum(5,3);
//output : 8
```
Functions stored in variables do not need function names. They are always invoked (called) using the variable name. The function above ends with a semicolon because it is a part of an executable statement.

## Hoisting 
Hoisting was thought up as a general way of thinking about how execution contexts work in JavaScript. Hoisting means variable and function declarations are moved to the top of scope before execution. It allows you to use a function before you declare it in your code.

### 📌 Difference between function declaration and function expression
> 
**Function declarations are hoisted but function expressions are not. 
**

Functions defined in a function declaration are hoisted, which means that you can use the function although it's defined below the code using it. Hoisted functions are made available everywhere within the current scope. For example

```javascript
//function is invoked before the declaration
sum(5,3);  //output : 8
//function declaration
function sum(a,b){
return a+b;
}

```
As opposed to function declarations, function expressions are not hoisted and can therefore not be used before they're defined. 
```javascript
sum(5,3);  //output :  // TypeError: sum is not a function
//function expression
var sum =function(a,b){
return a+b;
}
```
## IIFE (Immediately Invoked Function Expressions)
Functions that are executed as soon as they are declared, these functions are known as Immediately Invoked Function Expressions or IIFEs. 
IIFEs follows a particular syntax as shown below.
```javascript
(function (){ 
// code to be executed
})();
```
Let's break it down to make more sense. We have a function defined inside parentheses, and then we append () to execute that function.
```javascript
( /*function*/ )();
```
The function becomes a function expression that is immediately executed. 
Here are few important things about IIFEs

- The variable within the expression can not be accessed from outside it. 
- IIFEs are very useful because they don’t pollute the global object, and they are a simple way to isolate variables declarations.
- While creating a bunch of variables and functions in the global scope that no one uses outside your code, just wrap all of that in an IIFE and Your code will continue to work, but now you are not polluting the global scope. 
- IIFE is useful while implementing [Module Pattern](https://addyosmani.com/resources/essentialjsdesignpatterns/book/#modulepatternjavascript) in JavaScript. 

## Arrow Functions
 Arrow functions are mainly syntactic sugar for defining function expressions. Arrow function allows us to write functions in a much shorter syntax. It’s one of the most popular features of ES6. We can now create more concise, cleaner, and more readable functions by using the **=>** operator. 
The syntax is as follows
```javascript
()=>{ /*code to be executed*/ }
```
Syntax wise it’s easier to understand, remove the function keyword, declare the function like a variable, and after arguments, put a fat arrow.
```javascript
// Regular function
function sum(a,b){
return a+b;
}

//Arrow Function
var sum=(a,b)=>{ return a+b;}
```
Even though arrow functions are more concise than normal functions, they can still be reduced.
If the function body has a single expression, it can be written as
```javascript
var sum =(a,b)=> return a+b;   //removed curly braces
```
Also if there is only one parameter, then there is no need for parenthesis. For example, consider a function that takes a number as input and returns its square as a result.
```javascript
const square = a =>return a*a;    //removed parenthesis
const square = a => a*a; 
// In this case, we can also omit the return keyword.
```
The primary use case of arrow functions is for functions that get applied over and over again to items in a list. For example, if you have an array of values that you want to transform using a [map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), an arrow function is ideal.
```javascript
const digits= [2,3,4,5,6];
const square = digits.map(num => num*num);

console.log(digits);
// output : [2, 3, 4, 5, 6]
console.log(square);
// output : [4, 9, 16, 25, 36]
```
Important points about arrow functions
- Just like function expressions, arrow functions aren't hoisted — only function declarations are. 
- Arrow functions cannot be named.
- Arrow functions lexically bind the current **this **value. That means  The treatment of this within an arrow function is different than within non-arrow function expressions.

There are a few more ways we can define functions, which aren't discussed in this article. The decision of which declaration type to choose depends on the situation. 

##  Function scope vs Global scope
When you declare a variable inside a function, you can access that variable only within the function. It is not visible outside of the function. For example
```javascript
function sayHi(){
    var message="Hello world";  //function scope
    console.log(message);
    }
   
 sayHi();   // output : Hello world
 console.log(message);   // output : message is not defined
```
Variables defined outside any function, block, or module scope have global scope. Variables in the global scope can be accessed from everywhere. Every function can have access to the global scope.
```javascript
    var message="Hello world";  //Global scope
    function sayHi(){
    console.log(message);
    }
   
 sayHi();   // output : Hello world
```

## Lexical scope
When a function is defined in another function, the inner function has access to the outer function’s variables. This behavior is called lexical scoping. However, the outer function does not have access to the inner function’s variables.
```javascript
function outerFunction() {
  var user='Rutik';

  function innerFunction() {
    var job = 'student';
    console.log(user +"is a " + job);   //output : Rutik is a student
  }

  console.log(job) //output : Error, job is not defined
}
```
So when we access *user* variable in *innerfunction()* ,it works. But accessing job variable outside *innerfunction()* shows error.

> 
**To visualize how scopes work, you can imagine one-way glass. You can see the outside, but people from the outside cannot see you.**


## Functions vs Methods
A method, like a function, is a set of instructions that perform a task. The difference is that a method is associated with an object, while a function is not. 
```javascript
var person ={
name:  'Rutik',
job: 'student',
//method
sayHi : function(name){
            console.log("Hi " + this.name);
            }
};
person.sayHi();  //output : Hi Rutik

```
When used as object properties, functions are called methods.

## Conclusion
So we learned what are functions, how to call them, the difference between parameters and arguments, different ways we can define functions, how hoisting and function scope works in JavaScript. And I hope you got a nice idea about functions in JavaScript.

I keep writing about the things I learned and applied. So you can connect with me on [Twitter](https://twitter.com/WankhadeRutik), [Github](https://github.com/rutikwankhade)  or [Linkedin](https://www.linkedin.com/in/rutik-wankhade).

⚡ Happy learning!




