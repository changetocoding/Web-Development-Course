
# What is async?

Asynchronous task is a task that can be executed on a seperate thread while another process is running. (So you don't have to wait for something else to finish before executing the task),
Think of making washing the dishes or grabbing a cup while boiling a hot water in a kettle.


# What is a promise

Promises are a way of handling asynchronous code, specifically for what happens after an asynchronous task is completed.

Promises can only be resolved once if there is more than one resolve in a promise only the first action in the promise will be resolved, the second resolve will do nothing.

 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});

We should use Promises when working with ajax requests or any async task that requires an action after it has been complete.

# Promise 

A promise conists of three parts, the task usually connecting to an api route through a url, then - what happens once we recieve a response from the server, catch - what happens if the promise or response fails.

# .Then
.then is used after we receive a response and want to do something with that response, for example if we want to display a list of data after doing a GET Request

```js
axios.get('/api/PhoneBook/getAll')   // Your promise object
            .then(...)  // Instructing the promise object to call the function in the brackets once it completes successfully
            .fail(...);  // Instructing the promise object to call the function in the brackets if it fails
```

# .Catch
.catch is used for error handling promises and will catch any errors if a promise is rejected (the promise action fails). for example if the then in this case failed. The promise object would go to the .catch block and handle the error there

```js
axios.get('/api/PhoneBook/getAll')   // Your promise object
            .then(...)  // Instructing the promise object to call the function in the brackets once it completes successfully
            .catch(...);  // Instructing the promise object to call the function in the brackets if it fails
```

# Promise states

Resolve - The action related to promise succeeded

Reject - Promise action failed


# Homework 

Go through the Udacity course on Promises 

https://classroom.udacity.com/courses/ud898

How to set up exoplanet explorer

1. Open up git Bash and clone the repo using git clone https://github.com/udacity/exoplanet-explorer
2. Go to the folder using cd exoplanet-explorer and install gulp using npm install -g gulp bower
3. Install the polymer starter kit npm install && bower install -f polymer-starter-kit
4. Create a json file called npm-shrinkwrap.json and add the following line

https://timonweb.com/javascript/how-to-fix-referenceerror-primordials-is-not-defined-error/

```js
let trees;
fetch('
http://example.com/movies.json
') //  first  0sec
.then(response => response.json())  //second  5sec
.then(data => trees = data)
.catch(err => console.log(err));  // third   5sec

Element.val(trees);


fetch('
http://example.com/movies.json
') 
.then(response => 
response.data
...) 


response = {
  json:function(){
    new Promise()
  }
}

response = {
  data:data
}

fetch('
http://example.com/movies.json
')
.then(response => fetch(response.json()))


console.log("test") // 1sec


axios
  .get('
https://maps.googleapis.com/maps/api/geocode/json?&address=
' + this.props.p1)
  .then(response => {
    this.setState({ p1Location: 
response.data
 });
    return axios.get('
https://maps.googleapis.com/maps/api/geocode/json?&address=
' + this.props.p2);
  })
  .then(response => {
    this.setState({ p2Location: 
response.data
 });
    return axios.get('
https://maps.googleapis.com/maps/api/geocode/json?&address=
' + this.props.p3);
  })
  .then(response => {
    this.setState({ p3Location: 
response.data
 });
  }).catch(error => console.log(error.response));
  
  ```
