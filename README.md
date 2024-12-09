# Javascript Learning

## Why do we use javascript?

We use javascript because it enables us to add functionality to our HTML and CSS.

#### For Example:
- Adding an alert function when a button is clicked
- Add a function that will save form data

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
 
`const z = 15;<br/>
 // z = 20; // TypeError: Assignment to constant variable`

## Data Types in JavaScript
JavaScript has two main categories of data types:

- Primitive Types
- Reference Types

1. Primitive Data Types
These are immutable and stored directly in the memory.

### String

Represents textual data.
They are enclosed in single ('), double ("), or backticks (`) for template literals.
`let name = "Hamid";`
`let greeting = Hello, ${name};`

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

## OPERTORS

### 1. Arithmetic Operators
These operators perform mathematical operations on numbers.

+ (Addition): Adds two operands.
- (Subtraction): Subtracts the second operand from the first.
* (Multiplication): Multiplies two operands.
/ (Division): Divides the first operand by the second.
% (Modulus): Returns the remainder of division.
++ (Increment): Increases the operand by 1.
-- (Decrement): Decreases the operand by 1.

### 2. Comparison Operators
These operators compare two values and return a Boolean value (true or false).

== (Equal to): Checks if two operands are equal.
=== (Strict equal to): Checks if two operands are equal in value and type.
!= (Not equal to): Checks if two operands are not equal.
!== (Strict not equal to): Checks if two operands are not equal in value or type.
> (Greater than): Checks if the first operand is greater than the second.
< (Less than): Checks if the first operand is less than the second.
>= (Greater than or equal to): Checks if the first operand is greater than or equal to the second.
<= (Less than or equal to): Checks if the first operand is less than or equal to the second.

### 3. Logical Operators
These operators are used to combine conditional statements.

&& (Logical AND): Returns true if both conditions are true.
|| (Logical OR): Returns true if at least one condition is true.
! (Logical NOT): Reverses the Boolean value of the condition.

### 4. Assignment Operators
These operators assign values to variables.

=: Assigns a value to a variable.
+=: Adds the right operand to the left operand and assigns the result to the left operand.
-=: Subtracts the right operand from the left operand and assigns the result to the left operand.
*=: Multiplies the left operand by the right operand and assigns the result to the left operand.
/=: Divides the left operand by the right operand and assigns the result to the left operand.
%=: Applies the modulus operation on the left operand and assigns the result to the left operand.

### 5. Ternary Operator (Conditional Expression)
The ternary operator provides a shorthand for if-else conditions. It returns one value if the condition is true and another if the condition is false.

#### Syntax:
condition ? value_if_true : value_if_false

- let x = 10;
- let result = (x % 2 === 0) ? "Even" : "Odd";
- console.log(result);  // Even

## Control Flow

### Conditional Statements:
- if
- else if
- else

### Switch statements

switch (expression) {
    case value1:
        // Code to execute if expression === value1
        break;
    case value2:
        // Code to execute if expression === value2
        break;
    default:
        // Code to execute if no case matches
}

### Loops:

- for
for (initialization; condition; increment) {
    // Code to execute on each iteration
} 

- while
while (condition) {
    // Code to execute while condition is true
}

- do-while
do {
    // Code to execute
} while (condition);

- for...of
for (let variable of iterable) {
    // Code to execute for each value
}

let fruits = ["apple", "banana", "cherry"];

for (let fruit of fruits) {
    console.log(fruit);
}
// Output:
// apple
// banana
// cherry

- for...in
for (let key in object) {
    // Code to execute for each key
}

let person = { name: "Hamid", age: 25, country: "Pakistan" };

for (let key in person) {
    console.log(`${key}: ${person[key]}`);
}
// Output:
// name: Hamid
// age: 25
// country: Pakistan

## Functions

### 1. What Are Functions?
Functions are defined once and can be executed (or called) as many times as needed.
They can accept inputs (parameters) and return outputs (return values).

### 2. Declaring Functions
Function Declaration
A standard way to define a function.

function functionName(parameters) {
    // Function body
    return value; // Optional
}

function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Hamid")); // Output: "Hello, Hamid!"

Function Expression
A function can also be stored in a variable. This is called a function expression.

const functionName = function(parameters) {
    // Function body
};

const add = function(a, b) {
    return a + b;
};
console.log(add(3, 4)); // Output: 7


Arrow Functions (ES6)
A shorter syntax for writing functions.

const functionName = (parameters) => {
    // Function body
    return value; // Optional
};


If the function has a single expression, you can omit the braces and return keyword.

const multiply = (a, b) => a * b;
console.log(multiply(2, 3)); // Output: 6

3. Parameters and Arguments
Parameters: Variables defined in the function declaration.
Arguments: Values passed to the function when called.

function greet(firstName, lastName) {
    return `Hello, ${firstName} ${lastName}`;
}
console.log(greet("Hamid", "Khan")); // Output: "Hello, Hamid Khan"


Default Parameters
You can assign default values to parameters if no argument is provided.

function greet(name = "Guest") {
    return `Hello, ${name}`;
}
console.log(greet()); // Output: "Hello, Guest"


4. Return Statement
The return statement specifies the value that a function should output. If no return is provided, the function returns undefined.

function square(num) {
    return num * num;
}
console.log(square(4)); // Output: 16


5. Function Scope
Functions define a new scope. Variables declared inside a function are not accessible outside of it.

function example() {
    let localVar = "I am local";
    console.log(localVar);
}
example();
// console.log(localVar); // Error: localVar is not defined

6. Anonymous Functions
Functions without a name are called anonymous functions. These are often used as arguments to other functions or as immediate invocations.

setTimeout(function() {
    console.log("This runs after 2 seconds");
}, 2000);


7. Immediately Invoked Function Expressions (IIFE)
An IIFE runs immediately after it is defined.

(function() {
    console.log("I run immediately!");
})();

8. Higher-Order Functions
Functions that take other functions as arguments or return a function are called higher-order functions.

function greet(callback) {
    callback();
}

greet(() => console.log("Hello, world!")); // Output: "Hello, world!"


9. Callback Functions
A callback is a function passed as an argument to another function. It allows asynchronous or sequential execution.

function processUserInput(callback) {
    let name = "Hamid";
    callback(name);
}

processUserInput((name) => {
    console.log(`Hello, ${name}`);
});
// Output: "Hello, Hamid"

10. Rest and Spread Operators in Functions

Rest Operator
Allows you to represent an indefinite number of arguments as an array.

function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1, 2, 3, 4)); // Output: 10


Spread Operator
Allows you to expand elements of an array or object.

const numbers = [1, 2, 3];
function multiply(a, b, c) {
    return a * b * c;
}
console.log(multiply(...numbers)); // Output: 6


11. Recursion
A function that calls itself is recursive. Useful for problems like factorial or traversing a tree.

function factorial(n) {
    if (n === 1) return 1;
    return n * factorial(n - 1);
}
console.log(factorial(5)); // Output: 120


12. Closures
A closure is a function that retains access to its outer scope, even after the outer function has executed.

function outer() {
    let count = 0;
    return function inner() {
        count++;
        return count;
    };
}
const increment = outer();
console.log(increment()); // Output: 1
console.log(increment()); // Output: 2



