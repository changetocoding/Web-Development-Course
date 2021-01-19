# What is Axios
Axios is a promise-based HTTP client which works in both the browser and Node.js enviroment. Providing a single API for dealing with XMLHttpRequests and node's http interface. For any project where we need to make calls to a server or database to send data and retrieve data we can use Axios to make calls to a server.

# Setting up and installing Axios

We can set up Axios in our project in two ways the first way is to use the Node.js and install it using the following command (In git with node installed)

```
npm install axios
```

The other way we can set up Axios in our project is by using the CDN version and attaching it to our html page.

```html
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

# Making a GET Request to Server using Axios

For all the server calls on this page that we will be making we will be using JSON Placeholder https://jsonplaceholder.typicode.com/, First we use a GET request to make a call to the server.

```js
getRequestUsingAxios = () => {
    axios.get('https://jsonplaceholder.typicode.com/posts/1')
    .then(function (response) {
        debugger;
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error);
    }); 
}
```

# Making a POST Request to Server using Axios
Next we make POST request using Axios.

```js
postRequestUsingAxios = () => {
    axios.post('https://jsonplaceholder.typicode.com/posts', {title: 'My Posting', body: "From here to there, The Daily Life", userID: 3})
    .then(function (response) {
        debugger;
        console.log(response.data);
    })
    .catch(function (error) {
        console.log(error)
    })
    
}
```

# The difference between a POST and GET Request

A POST request is used when we want to send data over to our server, we include the data and format of the data inside of the call.

A GET Request is used to retrieve data from the server, we only need the route to retrieve the data from.

# What is the Fetch API

The Fetch API is a built in interface in Javascript for making calls to fetch resources from a server.

# Making a GET Request using Fetch API

Next is making a GET Request using the Fetch API

```js
getRequestUsingFetchAPI = () => {
    fetch('https://jsonplaceholder.typicode.com/posts/2')
    .then ((response) => response.json())
    .then ((json) => console.log(json));
}
```

# Making a POST Request using Fetch API

Making a POST Request using the Fetch API

```js
postRequestUsingFetchAPI = () => {
    fetch('https://jsonplaceholder.typicode.com/posts', {
        method: 'POST',
        body: JSON.stringify({
            title: 'Hey yo',
            body: "Welcome to Fresh Funky",
            userId: 4,
        }),
        headers: {
            'Content-type': 'application/json; charset=UTF-8',
        }
    })
    .then((response) => response.json())
    .then((json) => console.log(json));
}
```

# HTTP Success Codes
Whenever we make a call to a server, the server takes our call as a request and returns a server response which is a three-digit code known as a HTTP status code

The important ones to know are 

200 - Success 

404 - Not found (Error on the client side -> Can happen for example if we use a route that doesn't exist)

500 - Internal Server Error (Error on the server side)

# Error Validation
We need to use Error Validation when making calls to a server if the case that an error occurs, Both axios and the fetch API have methods for doing this

Error Validation in Axios
```js
    .catch(function (error) {
        console.log(error);
    }); 
``` 
The .catch statement is used catch any possible errors that can happen if the call to the server fails, we log it using the console and print what error occured as a HTTP Status code

Error Validation in Fetch API
```js
 .catch(error => console.log(error) );
 ```
 
 Same as Axios.

# Resources

https://github.com/changetocoding/WebLessonPlan/blob/main/Lesson14-TalkingServers.md - Axios GET and POST
https://jsonplaceholder.typicode.com/ - Placeholder server for testing GET and POST requests on.
https://stackoverflow.com/questions/50330795/fetch-api-error-handling - Error validation in Fetch API
https://javascript.info/fetch - Fetch API - POST and GET
https://httpstatusdogs.com/ - HTTP Requests



