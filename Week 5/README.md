# Classes

# What is a class

A class is an entity that we can use to create objects, they can contain variables and functions

A class also contains a constructor which is used to create an instance of the class when we need to use it

An instance of class is also known as an object

```js
class Dog {
    constructor(name, age)
    {
        this.name = name;
        this.age = age;
    }

    bark() {
    alert("Woof");
    }

    summary()
    {
        console.log("Dog name: " + this.name);
        console.log("Dog age: " + this.age);
    }
}
```

Let's break down what's happening here
# Class constructor
We use a constructor to construct our class at run time, the constructor will handle the creation of our class when we create an instance of it, We use the constructor keyword to tell our program where the constructor for our class is. 

Inside of our constructor we can declare variables that our class can use for methods.

```js
class Dog {
    constructor(name, age)
    {
        this.name = name;
        this.age = age;
    }
  }
```
In our constructor we set up our variables for use in our class methods - we set the values of name and age to the values that are passed in our constructor, 

```js
   summary()
    {
        console.log("Dog name: " + this.name);
        console.log("Dog age: " + this.age);
    }
```

We can call the values passed to our dog class using the this keyword to refer to the class field.

# this keyword

magine we have two variables with the same name how to tell them apart.

We can use the this keyword if we want to refer to the global variable.
```js
Fullname : function()
{
 Return this.firstname + " " + this.lastname
}
```

# getter / setter
We can also set class fields using getter and setters

A getter will return the class field it associated to

GetName() - 

A setter will change the value of the class field that is associated with

SetName(name) -

When we change the name in our class – the setter will be called

```js
class Cat {
    constructor(name)
    {
        this.name = name;
    }

    get name() {
        return this.name;
    }

    set name(newName) {
        this.name = newName;
    }
}
```


