# Week 9 - Function Expressions and Arrow Functions

# What is a function declaraiton?
A function declaration is a syntax for creating a function by creating a block of code.

```JS
addNumbers(1, 3);

function addNumbers(firstNumber, secondNumber)
{
    return firstNumber + secondNumber;
}
```

We can also create a function using another type of syntax for creating a function known as Function Expression.

# What is a function expression?

Another syntax for creating a function. We create a function in Function expression by assigning the function valve and storing it in a variable. (The assignment of the function value is explicit)

Unlike function declaration when create a function using function expression we need a semicolon as setting the variable value as a function is treated as an assignment.

```JS
let addNumbers = function(firstNumber, secondNumber) {
    return firstNumber + secondNumber;
};
```

The same as the function declaration version.

```JS
function addNumbers(firstNumber, secondNumber)
{
    return firstNumber + secondNumber;
}
```
We can only use the function expression version of AddNumbers after it is defined. As it is defined when the line it is created on is reached.

```JS
addNumbers(1, 3);

let addNumbers = function(firstNumber, secondNumber) {
    return firstNumber + secondNumber;
};
```

# Difference between Function Expression and Function Declaration

[info-graphic](https://github.com/emarkexe2001/Web-Development-Course/blob/main/Week%20Nine/Function%20Declaration%20and%20Function%20Expression.png?raw=true)

# Callback functions

A callback function is a function or one or more functions that we pass into another function expecting to "call them back" later when we need them.

We can create a callback function using both Function Declaration and Function Expression.

Function Declaration example here:
```JS
function displayName(name)
{
    alert(name);
}

function createFullName(firstName, lastName, nameDisplayer)
{
    let fullName = firstName + " " + lastName;

    nameDisplayer(fullName);
}

createFullName("Jo", "Ray", displayName);
```

Function Expression example here:
```JS
createFullName(firstName, lastName, function() {return firstName + " " + lastName});
```
# Arrow functions
An arrow function is another function syntax for creating functions.

```JS
let addNumber = (firstNumber, secondNumber) => firstNumber + secondNumber;
```

Second Example:
```JS
let sayHi = () => alert("Heya");
```

Is the same as a function expression but more of a shorthand version of it

Function Expression version

# Multiline arrow functions

We can also assign arrow functions using curly braces these are known as Multiline arrow functions

Example:

```JS
let addNumbers = (firstNumber, secondNumber) => {
    let result =  firstNumber + secondNumber;
    return result;
}
```

# Resources

https://javascript.info/function-expressions - For function expressions

https://javascript.info/arrow-functions-basics - For arrow functions

# Homework

Create three functions, One with function declaration, function expression and arrow functions. Make sure the functions are clearly named and easy to understand. Bad naming conventions eg. function1 will no longer be allowed.
