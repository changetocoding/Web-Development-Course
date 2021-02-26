# What is a form?

A form is a way of submitting data to a website. Forms tend to use POST Requests 

For a quick refresher on the difference between a POST request and GET Request

POST - for sending and updating data.

GET - for retrieving data

# What is the form tag?

The form tag is 

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

# What is the FormData class?

# Creating a form to submit using Javascript Form Data class

```html
<html>
    <title>Sending data using HTML Form</title>

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
    axios.post('https://tbhpwebdevapi.azurewebsites.net/api/Message/save', formData);

    e.preventDefault();
})
```

# Creating a form to submit using a payload

```html
<html>
  <title>Sending data using HTML Form</title>

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

# Homework

Update the Bonzai website to talk to the server.

API server to work with -  https://tbhpwebdevapi.azurewebsites.net/swagger/index.html

Work with the Order api route and use it to talk to the server and send over data to the server.

# Extra resources 
Html form tag - https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data
