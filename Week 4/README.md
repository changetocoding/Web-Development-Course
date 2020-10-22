# Homework Review - Bootstrap Form Page

Last week's homework review - Creating a form page with input fields, radio buttons, checkboxes, selection and a button that has an alert pop up.

# History of Javascript

Invented in 1995 by Brendan Eich, while he was working for Netscape Communications,

Was first known as Mocha before it was renamed to Livescript for the release of Netscape Navigator 2

Was designed to add interactivity to webpages 

Was renamed from Livescript to Javascript to capitalise on Javascript's popularity

ECMAScript was created as a standard for Javascript when Netscape submitted JavaScript to ECMA International 

Microsoft reverse engineered their own version of Javascript in 1996 after the release of Internet Explorer called JScript.

Throughout most of the early 2000s Javascript was stagnant until 2004 when Mozilla released Firefox and began wroking 

AJAX - A term coined by Jesse James Garrett used to described a set of technologies where Javascript acted as the backbone to create web applications where data could be loaded in the background without needed to refresh the whole page.

Chrome released in 2008 using the V8 Javascript engine - faster than competition at the time.

Node.JS - Used for server side development, is an open source server enviroment

Vue.JS - Developed by Evan You, A Javascript framework used to build user interfaces and single page applications.

Amgular - Developed by Google, A javascript framework used to build user interfaces.

# Variables
What is a variable?
A variable is a storage for data values '

Example of variable declaration

var name = "Johnny"

# var and let and const

There are two ways of declaring a variable in Javascript 

var - The old way of declaring a variable in JS.
```js
var number = 5 
```

let - The modern way of declaring a variable in JS. Defines a variable with a restricted scope - not supported in older browsers 

```js
let number = 5
```

const - A declaration for a variable's value that reassigned after it is declared - A value that is always the same

const example

```js
const pi = 3.14159
```

# Variable declaration

# Data types
A data type is a type of data that we assign to variables

# String
String is a data type used to represent text characters
```js
let name = "Emmanuel"
```

# Number
Number is a data type that we use to represent numbers
Can represent up to 2^53 - 2^53-1 = 9,007,199,254,740,992 to -9,007,199,254,740,992

```js
let numnber = 112
```

# BigInt
BigInt is a data type that we can use to represent numbers that are larger than the range that the Number data type can represent 
We can declare a number as a BigInt by adding n to the end of the number

```js
let bigNumber = 13142144212441n
```

# Boolean
Boolean is a data type that has two values true and false, we use boolean values to represent yes and no values 

```js
let age = 22
let isOlderThan18 = true
```

# Null

Null refers to a variable that is empty

```js
let age = null
```

# Undefined
Undefined refers to a variable that hasn't been assigned a value

```js
let name;

alert(name) - Will print undefined 
```

# Homework for this week

Create a javascript application that displays the name, age of a person.
