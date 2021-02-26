# What is a form?

A form is a way of submitting data to a website. Forms tend to use POST Requests 

For a quick refresher on the difference between a POST request and GET Request

POST - for sending and updating data.

GET - for retrieving data

# What is the form tag?

The form tag is similar to div, is a way of organising the data that we are going to send over to the server

# Creating a form to submit using HTMl

```html
<html>
    <title>Sending data using HTML Form</title>

    <body>
        <form action="https://tbhpwebdevapi.azurewebsites.net/api/Message/save" method="POST">
            <div>
                <label for="to">Who do you want to say this to?</label>
                <input name="to" id="to" value="A">
            </div>

            <div>
                <label for="say">What do you want to say?</label>
                <input name="say" id="say" value="Mark">
            </div>
            <div>
                <button>Post this</button>
            </div>
            
        </form>
    </body>
</html>
```
When we are sending over data using the html form. The name of the input on the form is used to map the field to the value. Not the id.


# Creating a form to submit using Javascript Form Data class

Another way of sending over form data is using axios and the javascript formData class

```html
<html>
    <title>Sending data using FormData</title>

    <body>
        <form id="theForm">
            <div>
                <label for="to">Who do you want to say this to?</label>
                <input name="to" id="to" value="A">
            </div>

            <div>
                <label for="say">What do you want to say?</label>
                <input name="say" id="say" value="Mark">
            </div>
            <div>
                <button id="btnSubmitForm">Post this</button>
            </div>
            
        </form>
    </body>

    <script src="javascriptform.js"></script>
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
</html>
```

```js
document.getElementById("theForm").addEventListener("submit", function(e) {
    let form = document.getElementById('theForm');
    let formData = new FormData(form);
    axios.post('https://tbhpwebdevapi.azurewebsites.net/api/Message/save/usingFormData', formData);

    e.preventDefault();
})
```

The form data class will create an object containing the form fields.

# Creating a form to submit using a payload

The last way is using a payload to send over the data

```html
<html>
  <title>Sending data using Payload</title>

  <body>
    <form id>
        <div>
            <label for="to">Who do you want to say this to?</label>
            <input name="to" id="to" value="A">
        </div>

        <div>
            <label for="say">What do you want to say?</label>
            <input name="say" id="say" value="Mark">
        </div>
    </form>

    <button id="btnSubmitForm">Post this</button>
  </body>

  <script src="payloadform.js"></script>
  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
</html>
```

```js
document.getElementById("btnSubmitForm").onclick = function(e) {
    e.preventDefault();
    const toTxt = document.getElementById("to");
    const sayTxt = document.getElementById("say");
    const payload = {to:toTxt, say:sayTxt};
    axios.post('https://tbhpwebdevapi.azurewebsites.net/api/Message/save', payload);

}
```

When using a payload we need to grab all the fields by id that we want to send over then add the fields indiviually to the payload before posting it.

# Checking what data we sent over

We can check the data that was sent over by going right clicking Inspect Element, going to the network tab, look for the request to the controller route - usually the controller, click on it, go to Headers and at the both it will tell you what data was sent.

# Homework

Update the Bonzai website to talk to the server.

API server to work with -  https://tbhpwebdevapi.azurewebsites.net/swagger/index.html

Work with the Order api route and use it to talk to the server and send over data to the server.

# Extra resources 
Html form tag - https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data

Using FormData - https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects

Youtube video on creating forms - https://www.youtube.com/watch?v=c3qWHnJJbSY


