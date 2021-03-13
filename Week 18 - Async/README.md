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
function getDataFromAPI()
{
  data = await fetch('http://example.com/movies.json') 
};
```

# Writng async functions as .thens and vice versa

We can write any function that we can use .then on as an async function
```js
// callback is the function to call on success
function getAnswer(id, callBack){
   axios.get(`/api/auth/`)
    .then(function(hasPermission){
      if(hasPermission){
        return axios.get(`/api/answer/${id}`).then(answer => callBack(answer))
      }else{
        return callBack("You don't have permision to view the answer");
      }
    })
}

function logAnswer(){
  const id = 1;
  getAnswer(id, answer => {
    console.log("The answer to question 1 is: ", reanswers)
  })
}
```

We can rewrite getAnswer as an async function
```js
async function getAnswer(id){
  const hasPermission = await axios.get(`/api/auth/`);
  if(hasPermission){
    const answer = await axios.get(`/api/answer/${id}`)
    return answer;
  }else{
    return "You don't have permision to view the answer"
  } 
}
```

and then write logAnswer as an async function
```js
function logAnswer(){
  const id = 1;
  getAnswer(id).then(function(answer){
    console.log(answer)
  })
}
```

# Async Error Handling

We can handle async promises using try and catch
```js
async function getAnswer(id){
  try {
    const data = await axios.get(`/api/answer/${id}`)
    // do something with data
  } catch (error) {
    // Equivalent to the .catch()
    // we just log the error here, but normally should properly handle the error
    console.log(err)
  }
}
```
The same as 
```js
function getAnswer(id){
   axios.get(`/api/answer/${id}`)
    .then(function(data){
      // do something with data
    })
    .catch(function(err){
      // we just log the error here, but normally should properly handle the error
      console.log(err)
    })
}
```

# Homework

Go through the following resources on the async method and await, start with the visualised promises dev.to page first, watch the freecampcode video after and follow along with the tasks and read the javascript tutorial page on async last.


Javascript Visualised Promises and async - https://dev.to/lydiahallie/javascript-visualized-promises-async-await-5gke

Javascript Async and Promises https://www.freecodecamp.org/news/learn-promise-async-await-in-20-minutes/ 

Javascript tutorial - Async / Await - https://javascript.info/async-await

and complete the tasks on the javascript tutorial and the FreeCodeCamp site.

