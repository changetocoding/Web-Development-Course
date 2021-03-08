# Async 

# What is Async?

Async is a keyword that allows us to return a promise - for example if we place the async keyword before a function, the function will return a promise. Async is a much cleaner and easier way of writing a promise. An async function will always return a promise.
```js
async function returnNumber()
{
  return 5;
}

returnNumber().then(console.log);
```
We can also write an async function like this
```js
const returnNumber = async () => {
return 5
}
```

# Await

Await can be used inside of an async function to wait for a promise to resolve before performing an action once the promise has resolved. The key bit about the Await keyword is that it can only be used inside of an async function

```js
async function getDataFromAPI()
{ 
  data = await fetch('http://example.com/movies.json') 
}
```

This will not work because the await keyword can only be used inside an async function.
```js
function returnNumber()
{
 let promise = Promise.resolve(2);
 
 result = await promise;
 
 return result
};
```

# Homework

Go through the following resources on the async method and await

Javascript tutorial - Async / Await - https://javascript.info/async-await

Javascript Visualised Promises and async - https://dev.to/lydiahallie/javascript-visualized-promises-async-await-5gke

Javascript Async and Promises https://www.freecodecamp.org/news/learn-promise-async-await-in-20-minutes/ 

and complete the tasks on the javascript tutorial and the FreeCodeCamp site.

