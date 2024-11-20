# Javascript Learning

## Why do we use javascript?

We use javascript because it enable us to add functionality to our HTML and CSS.

#### For Example:
- Adding an alert function when a button is clicked
- Add a function which will save form data

## Ways to use javascript in an HTML?

#### On Page Script
Adding internal JavaScript to HTML 
 
 
`<script type="text/javascript"> //JS code goes here </script>`

#### External JS File
Adding external JavaScript to HTML
 
 
`<script src="filename.js"></script>`

## Defining a variable?
3 ways to define a variable

### 1. var
#### Scope: Function-scoped.
- Hoisting: Variables are hoisted but initialized as undefined.
- Reassignment: Can be reassigned and redeclared.
- Usage: Avoid using var in modern JS; prefer let or const. 
 
`function example() {
   console.log(x); // undefined (hoisted)
   var x = 5;
   console.log(x); // 5
 }`

### 2. let
#### Scope: Block-scoped.
- Hoisting: Variables are hoisted but remain uninitialized (Temporal Dead Zone).
- Reassignment: Can be reassigned but not redeclared within the same scope.
- Usage: Use for variables that may need reassignment. 
 
`{
   let y = 10;
   console.log(y); // 10
 }
 // console.log(y); // ReferenceError: y is not defined`

### 3. Const
#### Scope: Block-scoped.
- Hoisting: Same as let (Temporal Dead Zone).
- Reassignment: Cannot be reassigned or redeclared.
- Usage: Use for constants or variables that won't change
 
`const z = 15;
 // z = 20; // TypeError: Assignment to constant variable`

### Data Types in JavaScript
JavaScript has two main categories of data types:
1. Primitive Types
2. Reference Types

#### 1. Primitive Data Types
String
    • Represents textual data.
    • Enclosed in single ('), double ("), or backticks (`) for template literals.
<code>let name = "Hamid";
 let greeting = `Hello, ${name}`;</code>

Number
    • Represents numeric values
int
float
let age = 25;
let pi = 3.14;
Boolean 
Represents logical values 
true
false
let isDeveloper = true;
Undefined 
A variable that has been declared but not assigned a value. 
let x; // undefined
Null
    • Represents an intentional absence of any value (manually assigned).
let result = null;

BigInt

Used for very large integers.
let bigNumber = 123456789012345678901234567890n;

Symbol

Unique and immutable value, often used as object keys.
let id = Symbol("uniqueID");

## 2. Reference Data Types
These are mutable and stored as references in memory.

### Object
A collection of key-value pairs.

let user = { name: "Hamid", age: 25 };

Array

Ordered collection of values.
let numbers = [1, 2, 3, 4];

Function

Block of reusable code.
function greet() {
  console.log("Hello, world!");
}


Yes, you're correct! After understanding variable declarations (var, let, const), the next step in JavaScript basics is Data Types.

Data Types in JavaScript
JavaScript has two main categories of data types:

Primitive Types
Reference Types
1. Primitive Data Types
These are immutable and stored directly in the memory.

String

Represents textual data.
They are enclosed in single ('), double ("), or backticks (`) for template literals.
Example:
javascript
Copy code
let name = "Hamid";
let greeting = `Hello, ${name}`;

### Boolean
Represents logical values (true or false).
`let isDeveloper = true;`

### Undefined
A variable that has been declared but not assigned a value.
`let x; // undefined`

### Null
Represents an intentional absence of any value (manually assigned).
`let result = null;`

### Number(int)
Called integer data type and it represents non-decimal numeric values.
`let age = 25;`

### Number(float)
Called float data type and it represents decimal numeric values.
`let pi = 3.14;`

### Number(BigInt)
Called big integer data type and it is used for very large integers.
`let bigNumber = 123456789012345678901234567890n;`

### Symbol
Unique and immutable value, often used as object keys.
`let id = Symbol("uniqueID");`

## 2. Reference Data Types
These are mutable and stored as references in memory.

### Object
A collection of key-value pairs. 
`let user = { name: "Hamid", age: 25 };`

### Array
Ordered collection of values. 
`let numbers = [1, 2, 3, 4];`

### Function
Block of reusable code. 
`function greet() {
   console.log("Hello, world!");
 }`

### Type Checking
To check the type of a value:

console.log(typeof "Hello"); // "string"
console.log(typeof 42); // "number"
console.log(typeof null); // "object" (quirk in JavaScript)
console.log(typeof undefined); // "undefined"


