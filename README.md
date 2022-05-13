

# JavaScript Primer

JavaScript is a high-level, object-based, dynamic scripting language popular as a tool for making web pages interactive.

## Basic need-to-know

EVERYTHING is case-sensitive
```
var stringA = "String A"; 
var stringa = "String a"; 
alert(stringA == stringa); // false
```
Semicolons are JavaScript's equivalent of a period. 
  - After you complete a statement (sentence), end it with a "```;```" character. 

When defining string values (```"this is a string of characters"```), single (```'```) and double (```"```) quotes are interchangeable, as long as the closing matches the opening.

Parentheses are used for 2 reasons:
  - Checking equality (evaluating 2 or more items to simply "true" or 'false') 
  - Sending or receiving a value 
```
if (stringA == stringa){ // do something }
var product = multiply(7, 3); // send 7 and 3
function multiply(a, b){return a*b;} // receive 7 as "a" & 3 as "b"
```
Comments are a way to explain to others (or leave reminders for yourself) what you're doing, and are denoted one of two ways:
  - Single- line comments are denoted by a double slash "```//```".
  - Multi-line comments are denoted by a slash-star to start "```/*```" and a star-slash "```*/```" to end. 
```
var product = multiply (4, 6); // This is a friendly reminder
/*
var product = multiply(8, 7); 
product = multiply(product, 7); 
*/
```
## Node js Variables

**Definition**: Variables are the workhorse of JavaScript. They allow you to create a container which holds a piece of data, then reference and manipulate what it contains. One thing to remember about JavaScript is a variable can contain any type of data— string values, integers, objects, arrays, functions.
```
var myVariableName = "My Variable Value";
```

There are three keywords used to declare a variable — ```var```, ```let```, and ```const```.

A variable is a named location for storing a value. 
  - You start by declaring a variable with the ```var``` keyword, followed by any name you want to call it.
```
Var newContainer;
```
  - We can assign any value to this variable.
```
newContainer = ‘sample’;
```
  - We can declare and assign the variable in single line as well:
```
Var newContainer = ‘sample’;
```
  - Variables are not type specific and can hold any values which have different data types.

### Differences between var, let, and const keywords as well.

// Assign the string value ```firstName``` ```LastName``` to the ```username``` identifier

```
var username = "firstName lastName";
```
The above statement consists of a few parts:

  - The declaration of a variable using the ```var``` keyword
  - The variable name (or identifier), ```username```
  - The assignment operation, represented by the ```=``` syntax
  - The value being assigned, ```"firstName lastName"```

Variables can be used to represent any JavaScript data type. Variables store data in memory which can later be accessed and modified. 
  - Variables can also be reassigned and given a new value. 
  - Variable names can consist only of letters (a-z), numbers (0-9), dollar sign symbols ($), and underscores (_). 
  - Variable names cannot contain any whitespace characters (tabs or spaces). 
  - Numbers cannot begin the name of any variable. 
  - There are several reserved keywords which cannot be used as the name of a variable. 
  - Variable names are case sensitive.

**Differences**:


| Keyword  | Scope | Hoisting  | CanBeReassigned | CanBeRedeclared |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| var | function  |  yes             |      yes         |       yes        |
| let  | block  |  no             |         yes      |         no      |
| const  | block  | no              |       no        |         no      |


## Understanding JavaScript Data Types

Five basic data types in JavaScript are **strings**, **numbers**, **Boolean**, **array**, and **object**.

```
var myInt = 0;
var myFloat = 2.5;
var myBoolean = true; //The equivalent of a 1 or 0 (on/off, true/false)
var myString = "This is a string";
var myArray = [1,”two”,3]; //not all the values have to match data types, be careful
// Objects to hold structured data – like an array, but with “named” properties
var myJSONObject = { myField : "Some value" };
// Object instantiation using new
var myDate = new Date();
```

Dynamic Typing is possible with Javascript variables.

```
var t = 16;     // t is a number
var t = "Teresa";   // t is a string
var t = true;   // t is a Boolean
var t;          // t is undefined
```
**Note**: Numbers in JavaScript are considered to be accurate up to 15 digits. That means numbers will be rounded after the 16th digit is reached.

Examples:

```
var num1 = 93;  // 93
var num2 = 93.00;  // 93
var num3 = 987e8;   // 98700000000
var num4 = 987e-8;  // 0.00000987
var num5 = 999999999999999; // remains as 999999999999999
var num6 = 9999999999999999; // rounded up to 10000000000000000
var num7 = 5 / 0;   // will return Infinity
var num8 = -5 / 0;  // will return -Infinity
var x = 20 / "Shark";   // x will be NaN
var y = 20 / "5";   // y will be 4
```

**Multiple data types**:

Concatenation of string and number:
```
var o = "Ocean" + 5 + 3; // Ocean53
var p = 5 + 3 + "Ocean"; //8Ocean
```
Using Operators
  - Numeric operators include ```+``` (addition) ```-``` (subtraction) ```/``` (division) ```*``` (multiplication) ```%``` (modulo)

```
var x = 4;
x = x + 1; // x is 5
y = x % 2; // y is 1
x++; // x is 6
x--; // x is 5
x += 3; // x is 8
var aString = "The value of x is " + x;
```

Comparison operator:

| Operator  | Description |
| ------------- | ------------- |
| ```==```  | equal  |
| ```!=``` | not equal  |
| ```>``` | greater than|
| ```>=```  | greater than or equal to|
| ```<``` | less than |
|```<=``` | less than or equal to |
|```===```  | equal to, and same data type  |
|```!==```  | not identical |


**Implementing Looping**

‘For’, ‘while’, ‘do…while’ are looping available.

for (initialization; condition; final expression) {
// code to be executed
}
// Declare array with 3 items
let languages = [ "javascript", "java", "python" ];
// Initialize for loop to run for the total length of an array
for (let i = 0; i < languages.length; i++) {
// Print each item to the console
console.log(languages[i]);
}
// Print out each type of languages
for (let language of languages) {
console.log(language);
}
Creating Functions: 

Below is an example of a function creation and its usage

// Initialize greeting function
function greet() {
console.log("Hello, World!");
}
// Invoke the function
greet(); // Hello, World!
Function Expression: Function creation as an expression

// Assign add function to sum constant
const sum = function add(x, y) {
return x + y;
}
// Invoke function to find the sum
sum(20, 5); //output: 25
Anonymous expression: 

// Assign function to sum constant
const sum = function(x, y) {
return x + y;
}
// Invoke function to find the sum
sum(100, 3); //output: 103
 Arrow functions: New way of function creation.

// Define multiply function
const multiply = (x, y) => {
return x * y;
}
// Invoke function to find product
multiply(30, 4); // output: 34
Variable Scope
The scope is basically the current context of execution.Context is basically in which variables are visible or can be referenced. If variables are not accessible or can’t be referenced, then they will become out of context. 

Scopes are basically hierarchy in nature i.e. a variable available in the parent context is also available to child context but variable declared in child context are not accessible in the parent context. Let's understand this with an example:

Any variable declared inside a function has its context within the function only. If we try to access that variable outside the function then we get an undefined error.

Function VariableScope() {
Var scope = ‘sample’;
console.log(scope); // no error 
}
console.log(scope); // this will raise an error
Let’s declare the variable outside the function and access it.
var scope = ‘sample’;
Function variableScope() {
console.log(scope); // no error
}
console.log(scope); // no error
Let's understand the reason why let is needed if we have var already with an example:

Note: Blocked scope is the code region within curly braces like if, switch, for/while loops, etc.

Var blockedScope = ‘test’;
If (true) {
Var blockedScope = ‘test-updated’; 
console.log(blockedScope);
}
console.log(blockedScope);
Output:
test-updated
test-updated
If we replace the var keyword with let…Output will be 

test-updated

test

So, var declared with the same name is same within and outside blocked scope, so gets update whereas let is scoped within a block and doesn’t override outside declaration and let variable is different from the one inside block scope and outside.

Const is also blocked scope similar to let but once assigned value can’t be changed.

Hoisting

This is an interesting concept and applicable only to the var declarations. During compile-time, variables and functions declarations are loaded in memory because of which this are available and accessible before where this is actually typed in their scope. Let's understand this with a simple example:

 console.log(hoisted);
var hoisted = ‘variable is hoisted’;
We would expect a reference error which is the case with let. But in this case, we get Output: undefined and not an error.

For understanding this concept better, let's see how this code behaves:

First thing happens is - all variables in the current context declarations are hoisted in memory.  So, var hoisted is declared in memory

Console.log tried to log the hoisted variable but since it is unassigned at this instance, the undefined value is logged.

A hoisted variable is assigned post console.log.

Let’s revise this example little differently:

hoisted = “variable is hoisted”;
console.log(hoisted);
var hoisted;
This time the output is “variable is hoisted”. As mentioned previously, variable declaration happens first and then assignment followed by reading and logging it.

// Initialize a global variable
var species = "werewolf";
const SPECIES = "human"; // Assign value to const
SPECIES = "werewolf"; // Attempt to reassign value
console.log(SPECIES);
Output: Uncaught TypeError: Assignment to constant variable.
const TODO; // Declare but do not initialize a const
console.log(TODO);
Output: Uncaught SyntaxError: Missing initializer in const declaration
// Create a CAR object with two properties
const CAR = {
color: "blue",
price: 15000
}
CAR.price = 20000; // Modify a property of CAR
console.log(CAR);
Output: { color: 'blue', price: 20000 }
Using JavaScript Objects
An object in JavaScript is a data type that is composed of a collection of names or keys and values, represented in name: value pairs. The name: value pairs can consist of properties that may contain any data type — including strings, numbers, and Booleans — as well as methods, which are functions contained within an object.

 Two ways to construct an object in JavaScript:

The object literal, which uses curly brackets: {}
// Initialize object literal with curly brackets
const objectLiteral = {};

The object constructor, which uses the new keyword
// Initialize object constructor with new Object
const objectConstructor = new Object();

Two ways to access an object's properties say 

Say we have const employee = { id: 1, age: 23 };

Dot notation: .
employee.id
Bracket notation: []
employee[‘id’]
We can add or modify an object property

employee.age = 32; //modifies property
employee.gender = female; // adds new property
delete employee.gender; // removing existing property
// Iterate through properties of employee
for (let key in employee) {
console.log(employee[key]);
}
Manipulating Strings

A string is a sequence of one or more characters that may consist of letters, numbers, or symbols. Strings in JavaScript are primitive data types and immutable, which means they are unchanging.

// Storing a String in a Variable
const newString = "This is a string assigned to a variable.";
// String concatenation
"Sea" + "horse";
Output : Seahorse
const string1 = "Sample string1";
const string2 = "Sample string2";
// template Literals
const finalString = `String concatenation with template literals: ${string1} and ${string2}.`;
const brokenString = 'I'm a broken string';
console.log(brokenString); //output: unknown: Unexpected token
In order to avoid an error being thrown in these situations, we have a few options that we can use:

Opposite string syntax
"We're safely using an apostrophe in double-quotes."
'Then he said, "Hello, World!"'
Escape characters
'We're safely using an apostrophe in single quotes.'
 Template literals
`We're safely using apostrophes and "quotes" in a template literal.`
Working with Arrays

An array in JavaScript is a type of global object that is used to store data. Arrays consist of an ordered collection or list containing zero or more data types, and use numbered indices starting from 0 to access specific items.

Arrays are very useful as they store multiple values in a single variable, which can condense and organize our code, making it more readable and maintainable. Arrays can contain any data type, including numbers, strings, and objects.

// Assign the five oceans
let oceans = ["Pacific", "Atlantic", "Indian", "Arctic", "Antarctic"];
// Print out the first item of the oceans array
oceans[0]; //accessing elements through index
Output:Pacific
// Initialize array of shark species with array literal
let sharks = [ "Hammerhead", "Great White", "Tiger"];
// Initialize array of shark species with array constructor
let sharks = new Array("Hammerhead", "Great White", "Tiger");
// Create an array of countries
let countries = [ "India", "England", "NewZealand", "Australia"];
// Loop through the length of the array
for (let i = 0; i < countrieslength; i++) {
  console.log(i, countries[i]);
}
// Loop through each countries
for (let country of countries) {
    console.log(country);
}
The array has some inbuilt method which are listed down:

Array.isArray(shellfish); // Test if fish variable is an array
Pop: is used to remove the last item from the array
Shift: is used to remove the first item from the array
Push: adds a new element to end of the array
Unshift: adds a new element to start of the array
Reverse: reverses the order of elements
Splice: adds or removes any element inside the array from any position simultaneously
 splice(index number, number of items to remove, items to add)
let fish = [ "piranha", "barracuda", "koi", "eel" ];
// Remove two items and add one
fish.splice(1, 2, "manta ray");
fish;
output: [ 'piranha', 'manta ray', 'eel' ]
Fill: replaces all elements in an array
let fish = [ "piranha", "barracuda", "koi", "eel" ];
// Replace all values in the array with "shark"
fish.fill("shark");
fish; 
output:[ 'shark', 'shark', 'shark', 'shark' ]
Sort: Sorting items in the list. The sort will not sort an array of numbers by size by default. Instead, it will only check the first character in the number.
let numbers = [ 42, 23, 16, 15, 4, 8 ];
numbers.sort(); //[ 15, 16, 23, 4, 42, 8 ]
// Function to sort numbers by size
const sortNumerically = (a, b) => {
  return a - b;
}
numbers.sort(sortNumerically); //[ 4, 8, 15, 16, 23, 42 ]
Concatenate
// Create arrays of monovalves and bivalves
let monovalves = [ "abalone", "conch" ];
let bivalves = [ "oyster", "mussel", "clam" ];
// Concatenate them together into shellfish variable
let shellfish = monovalves.concat(bivalves); 
output: [ 'abalone', 'conch', 'oyster', 'mussel', 'clam' ]
Join
shellfish.join()
output: ‘abalone,conch,oyster,mussel,clam’
Slice Method copies a portion of an array to a new array.
let newShellfish = Shellfish.slice(2,4)

output: ['oyster', 'mussel']

Arrow Functions usage on arrays
let fish = [ "piranha", "barracuda", "cod", "eel" ];
// Print out each item in the array
fish.forEach(individualFish => console.log(individualFish);)
// Pluralize all items in the fish array
let pluralFish = fish.map(individualFish => `${individualFish}s`);
// Filter all creatures that doesn’t start with "p" into a new list
let filteredList = fish.filter(individualFish => {
  return individualFish[0] !== "p";
});
let numbers = [ 42, 23, 16, 15, 4, 8 ];
// Get the sum of all numerical values
let sum = numbers.reduce((a, b) => a + b);
let findNumber = numbers.find((num) => {
     return num === 15;
});
findNumber; //output: 15
Adding Error Handling
Error: The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions.

Syntax: new Error([message[, fileName[, lineNumber]]])

Types of error:

EvalError : Creates an instance representing an error that occurs regarding the global function eval().
InternalError : Creates an instance representing an error that occurs when an internal error in the JavaScript engine is thrown. E.g. "too much recursion".
RangeError: Creates an instance representing an error that occurs when a numeric variable or parameter is outside of its valid range.
ReferenceError: Creates an instance representing an error that occurs when de-referencing an invalid reference.
SyntaxError: Creates an instance representing a syntax error that occurs while parsing code in eval().
TypeError: Creates an instance representing an error that occurs when a variable or parameter is not of a valid type.
URIError: Creates an instance representing an error that occurs when encodeURI() or decodeURI()are passed invalid parameters.
Handling generic Error:

try {
  throw new Error('Whoops!');
} catch (e) {
  console.log(e.name + ': ' + e.message);
}
Handling specific error:

try {
  foo.bar();
} catch (e) {
  if (e instanceof EvalError) {
    console.log(e.name + ': ' + e.message);
  } else if (e instanceof RangeError) {
    console.log(e.name + ': ' + e.message);
  }
  // ... etc
}
Creating a Custom Error and handling it:

class CustomError extends Error {
  constructor(foo = 'bar', ...params) {
// Pass remaining arguments (including vendor specific ones) to parent constructor
    super(...params);
// Maintains proper stack trace for where our error was thrown (only available on V8)
    if (Error.captureStackTrace) {
      Error.captureStackTrace(this, CustomError);
}
    this.name = 'CustomError';
// Custom debugging information
    this.foo = foo;
    this.date = new Date();
  }
}
try {
  throw new CustomError('baz', 'bazMessage');
} catch(e){
  console.log(e.name); //CustomError
  console.log(e.foo); //baz
  console.log(e.message); //bazMessage
  console.log(e.stack); //stacktrace
}
The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions.

Summary: 

This provides an overview of the basics of javascript with code examples. 
