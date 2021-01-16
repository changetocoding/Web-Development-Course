# Week 13 - Function Expressions and Arrow Functions

# What is a function declaration?
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

[info-graphic](https://github.com/emarkexe2001/Web-Development-Course/blob/main/Week%20Nine/)
![Function Declaration and Function Expression.](Function%20Declaration%20and%20Function%20Expression.png)

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

https://stackoverflow.com/questions/336859/var-functionname-function-vs-function-functionname

# Homework

Create a filter, map and sum function, Each one must contain a function declaration version, function expression and arrow function version

Starting code to help you out. Also make sure that your function names are clear and concise, Naming conventions will be checked next week.
- filter
```js
// Your code
var youngsters = filterIt(peopleArrary, function (item) {
	return item.age < 30;
});

// Must match
var expected = peopleArray.filter(function (item) {
	return item.age < 30;
});
```
- map
```js
// Your code
var names = mapIt(peopleArray, (item) => return item.name);

// Must match
const expected = peopleArray.map((item) => return item.name; );
```

- some
```js
// Your code
var names = hasSome(peopleArray, (item) => return item.age < 30);

// Must match

var anyUnder30 = peopleArray.some(function (item) {
	return  item.age < 30;
});
```
