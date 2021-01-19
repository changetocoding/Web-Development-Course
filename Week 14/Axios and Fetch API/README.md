# What is Axios

# Setting up and installing Axios

# Making a GET Request to Server using Axios

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

https://jsonplaceholder.typicode.com/ - Placeholder server for testing GET and POST requests on.

https://javascript.info/fetch - Fetch API - POST and GET

