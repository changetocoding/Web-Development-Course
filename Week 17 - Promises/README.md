# What is a promise

Promises are a way of handling asynchronous code, specifically for what happens after an asynchronous task is completed.

Promises can only be resolved once if there is more than one resolve in a promise only the first action in the promise will be resolved, the second resolve will do nothing.

 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});

We should use Promises when working with ajax requests or any async task that requires an action after it has been complete.

# What is async?

Asynchronous task is a task that can be executed on a seperate thread while another process is running. (So you don't have to wait for something else to finish before executing the task),
Think of making washing the dishes or grabbing a cup while boiling a hot water in a kettle.

# Promise constructor

Two ways of creating a promise, 

1. We can store a promise as a variable 

```html
 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});
```

2. Or call the promise when we need it

```html
 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});
```

# .Then

# Promise states

Fulfilled / Resolved - The action related to promise succeeded

Rejected - Promise action failed

Pending - The promise action hasn't yet been fulfilled or rejected

Settled - Either the promise action has been fulfilled or rejected

Homework 

Go through the Udacity course on Promises 

How to set up exoplanet explorer

1. Open up git Bash and clone the repo using git clone https://github.com/udacity/exoplanet-explorer
2. Go to the folder using cd exoplanet-explorer and install gulp using npm install -g gulp bower
3. Install the polymer starter kit npm install && bower install -f polymer-starter-kit
4. Create a json file called npm-shrinkwrap.json and add the following line

https://timonweb.com/javascript/how-to-fix-referenceerror-primordials-is-not-defined-error/
