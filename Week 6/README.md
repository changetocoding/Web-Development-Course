# JQuery and Javascript HTML Document
# What is DOM
Stands for Document Object Model 
Used to create an object oriented representation of HTML documents which we can manupulate.

We can manupulate the DOM using JQuery or Javascript's HTML DOM.

# What is JQuery
JQuery is javascript library written by John Resig in 2006. 
Designed to si

# What do we use JQuery for
We use JQuery for Designed to simplify HTML DOM tree traversal and manupulation 
Can be used to select DOM elements.

JQuery setup - For this we will use the CDN libary in our HTML document

```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
```

and a document.ready in our JS file

```js
$(document).ready(function() {

});
```

# Getting elements using JQuery
We can get an html element using JQuery's document.ready(), then specifying the html id of the element we want to select 

```html
  <p id="text">Hello guys</p>
  <button id="btn1">Click me to change text</button>


```js
$(document).ready(function() {
    $("#btn1").click(function() {
      $("#text").text("Hello everybody");
    });
```

This will select the element with the id text and change the text of it to hello everybody.

```html
  <p id="text">Hello guys</p>
  <button id="btn1">Click me to change text</button>


```js
    $("#btn2").click(function() {
      $("#text").html("<h2>Hello everybody</h2>");
    });
```

# Adding elements using JQuery
We can add new elements in JQuery in one of the following ways 

- Append – will add after the specified element

- Prepend – will add before the specified element

- Before – will add to the document layout before the specified element (Above the element for example)

- After – will add to the document layout after the specified element (Below the element)

Examples

.append()
```js
    $("#btn3").click(function() {
      $("#heading").append(" Today we had ice cream for lunch");
    });
```

.prepend()
```js
 $("#btn4").click(function() {
      $("#heading").prepend("Yesterday I had crepes for snacks ");
    });
```
.before()
```js
    $("#btn5").click(function() {
        $("#text").before("text before paragraph ");
      });

```
.after()
```js
    $("#btn6").click(function() {
        $("#text").after("text after paragraph ");
      });
```
# Removing elements using JQuery
We can also remove elements using JQuery by specifiying the element id we want to remove, using the remove method

```js
   $("#myBtn").click(function() {
        $("#heading").remove();
    });
```
# Javascript DOM

Is an API for Javascript 
Using it allows Javascript to add, remove or change HTML elements
Add, remove or change HTML attributes
React to HTML Events

# Getting elements using Javascript DOM
We can access DOM Elements through three methods 
document.getElementById(id) - Will get the Element by it's id


```js
function changeHeading()
{
    document.getElementById("test").innerHTML = "Test";
}

function changeColour()
{
    document.getElementById("test").style.backgroundColor = "red";
}
```

```html

```

document.getElementsByTagName(name) - gets Element by Tag


```js
function changeParagraphText()
{
    var divParagraph = document.getElementById("div-paragraph");
    let numberOfParagraphs = divParagraph.getElementsByTagName("p").length;
    
    document.getElementById("display-paragraph-numbers").innerHTML = "The number of paragraphs in div-paragraphs is " + numberOfParagraphs;
}
```
document.getElementsByClassName(name) - get Element belonging to a html class by it's class name

```js
function getElementsFromClass()
{
    let parentClass = document.getElementById("dessert");
    let getElement = document.getElementsByClassName("cheese")[0].textContent;
    alert(getElement);
}
```
# Adding Elements using Javascript DOM
We can add new elements to our html documents using the createElement method and appendChild method

```js
function createNewButtonWithText()
{
    let myButton = document.createElement("BUTTON");
    myButton.innerHTML = "This button was made with Javascript HTML DOM";
    document.body.appendChild(myButton);

}
```

```html
 <button onclick="createNewButton()">Click me to create a new button</button>
```

# Removing Elements using Javascript DOM
We can remove an element from a html document using the remove method.s
```js
function removeExistingElement()
{
    let removeElement = document.getElementById("btn-show-numbers");
    removeElement.remove("btn-show-numbers");
}
```

```html
 <button onclick="removeExistingElement()">Click me to remove an existing element</button>
```
