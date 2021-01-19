# What is Axios
Axios is a promise-based HTTP client which works in both the browser and Node.js enviroment. Providing a single API for dealing with XMLHttpRequests and node's http interface. For any project where we need to make calls to a server or database to send data and retrieve data we can use Axios to make calls to a server.

# Setting up and installing Axios

We can set up Axios in our project in two ways the first way is to use the Node.js and install it using the following command

```
npm install axios
```

The other way we can set up Axios in our project is by using the CDN version and attaching it to our html page.

```hmtl
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

# Making a GET Request to Server using Axios

For all the server requests on this page that we will be making we will be using JSON Placeholder https://jsonplaceholder.typicode.com/

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

# What is the Fetch API

The Fetch API is a built in interface in Javascript for making calls to fetch resources from a server.

# Making a GET Request using Fetch API

```js
getRequestUsingFetchAPI = () => {
    fetch('https://jsonplaceholder.typicode.com/posts/2')
    .then ((response) => response.json())
    .then ((json) => console.log(json));
}
```

# Making a POST Request using Fetch API

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

# Error Validation

# Resources

https://github.com/changetocoding/WebLessonPlan/blob/main/Lesson14-TalkingServers.md - Axios GET and POST
https://jsonplaceholder.typicode.com/ - Placeholder server for testing GET and POST requests on.
https://javascript.info/fetch - Fetch API - POST and GET


