# EXERCISE 02: Introduction to Javascript

In this lesson, we will discuss what JavaScript is. We will also go over some basic grammar, variable declarations, data types, and literals.

---

## What is Javascript?

**What is Javascript?**

JavaScript is a cross-platform, object-oriented scripting language used to add functionality and interactivity to web pages. For example, having clickable buttons, popup menus, etc. There are also more advanced server-side versions of JavaScript like Node.js, which allow you to add more functionality to a website, like real-time collaboration between multiple computers. Inside a host environment such as a web browser, JavaScript can be connected to the objects of its environment to provide programmatic control over them.

JavaScript contains a library of objects, such as `Date`, `Math`, and `Array`, and a core set of language elements such as operators, control structures, and statements. Core JavaScript can be extended for a variety of purposes by supplementing it with additional objects; for example:

Client-side JavaScript extends Javascript's core language by providing objects to control a browser and its Document Object Model (DOM). For example, client-side extensions allow an application to place elements on an HTML form and respond to user events such as mouse clicks, form input, and page navigation.

Server-side JavaScript extends Javascript's core language by providing objects relevant to running JavaScript on a server. For example, server-side extensions allow an application to communicate with a database, provide continuity of information from one invocation to another of the application, or perform file manipulations on a server.
This means that in the browser, JavaScript can change the way the webpage (DOM) looks. And, likewise, Node.js JavaScript on the server can respond to custom requests from code written in the browser.

---

## Basic Grammer

Javascript is case-sensitive, so the variables `fun` and `Fun` are not equal. Instructions in Javascript are called statements and are separated by a semicolon. `(;)`
Writing a semicolon after a statement even when it is not strictly needed, is considered best practice. This reduces the chances of introducing bugs into the code.

### Declarations

There are 3 types of variable declarations in Javascript, `var`, `let`, `const`.

`var`

Declares a variable, optionally initializing it to a value.

```js
var age = 10;
```

or...

```js
var ages = [];
```

`let`

Declares a block-scoped, local variable, optionally initializing it to a value.

```js
let currentAge =  10;
```

`const`

Declares a block-scoped, read-only named constant.

---

## Variables

Variables are used as symbolic names for values in your application. The names of variables, called "identifiers", conform to certain rules.

JavaScript identifiers must start with a letter, underscore (_), or a dollar sign ($). Subsequent characters can also be digits (0–9).

JavaScript is case-sensitive. It is important to remember that letters include the characters "A" through "Z" (uppercase) as well as "a" through "z" (lowercase).

There are two ways to declare a variable:

- Using the keyword `var`

```js
var a = 30
```

You can use this syntax to declare both local and global variables, depending on the execution context.

- Using the keyword `let` or `const`

```js
let b = 10

const c = 12
```

You can use this syntax to declare a block-scope local variable.

A variable is considered a global variable when it is declared outside of any function. It is available to any other code in the current document.

A variable is considered a local variable when it is declared within a function. It is only available within that function.

If a variable is declared without being assigned a value, the value is considered undefined.

Attempting to access an undeclared variable will throw a ReferenceError.

```js
var n;
console.log('The value of n is equal to' + n); // The value of n is equal to undefined
```

### Constants

Constants are read-only variables. You can create them using the keyword `const`.

The syntax is the same as `var` and `let`: it must start with a letter, underscore, or a dollar sign ($), and can contain alphabetic, numeric, or underscore characters.

```js
const number = 9;
```

Just like the name implies a constant cannot change value through assignment or be re-declared while the script is running. It must be initialized to a value.

The scope rules for constants are the same as those for `let` block-scope variables. If the   `const` keyword is omitted, the identifier is assumed to represent a variable.

You cannot declare a constant with the same name as a function or variable in the same scope. For example:

```js
// THIS WILL CAUSE AN ERROR
function i() {};
const i = 4;

// THIS WILL ALSO CAUSE AN ERROR
function f() {
  const g = 5;
  var g;

}

```

## Data types

There are eight data types:

### Seven primitive

1. Boolean -  means either `true` or `false`
2. null - a special keyword denoting a null value (Nothingness).
3. undefined - value is not defined.
4. Number - an integer or floating-point number. For example 42 or 3.14159.
5. Big-Int - an integer with arbitrary precision. For example: 9007199254740992n.
6. String - a sequence of characters that represent a text value. For example: "Hello"
7. Symbol -  a data type whose instances are unique and immutable.
8. Object - you can think of Objects as a named container for values.

Variables and data types go hand in hand. A variable's purpose is to store data. Data types are simply the types of data that can be stored in variables.

Let's take a look at how changing the data type affects our result.

```js
var firstNum = 1;

var secondNum = 5;

var result = firstNum + secondNum;

console.log(result);

// This will log: 6
```

```js
// However if we changed the numbers to strings
var firstNum = "1";

var secondNum = "5";

var result = firstNum + secondNum;

console.log(result);

// This will log: 15
```
