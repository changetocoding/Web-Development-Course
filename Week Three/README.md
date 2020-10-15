# Homework Review

Review of last week's homework - Going through the bootstrap tutorial and creating a table using bootstrap with a required address line formatted using line break tags.

# Input fields
- Up till now we have been working hard coded data

- data that we declare and create in our program but websites work with data that is provided from the user in this case our input fields will act as a method for our users to enter data that we can use.

Think for example - when you register for an account on a website or login to a website

```html
<body>
      <div class="container">
          <h1>Form Page Tutorial</h1>
      </div>

      <div class="form-group">
        <label for="formFirstName">First Name</label>
        <input type="text" id="formFirstName" placeholder="Enter your first name">
      </div>

      <div class="form-group">
        <label for="formLastName">Last Name</label>
        <input type="text" id="formLastName" placeholder="Enter your last name">
      </div>

  </body>
```

# Buttons

We can also add a button to our form - Buttons can handle an event when we click on them but for now we will just have a button that doesn't do anything when pressed.

```html
<body>
      <div class="container">
          <h1>Form Page Tutorial</h1>
      </div>

      <div class="form-group">
        <label for="formFirstName">First Name</label>
        <input type="text" id="formFirstName" placeholder="Enter your first name">
      </div>

      <div class="form-group">
        <label for="formLastName">Last Name</label>
        <input type="text" id="formLastName" placeholder="Enter your last name">
      </div>

      <button type="submit" class="btn btn-primary">Submit</button>
  </body>
```
# Checkboxes
```html
 <div class="form-check">
          <input type="checkbox" class="form-check-input" id="checkbox1">
          <label class="form-check-label" for="checkbox1">Check this out</label>

          <input type="checkbox" class="form-check-input2" id="checkbox2">
          <label class="form-check-label2" for="checkbox2">I found you checkbox</label>
          
          <input type="checkbox" class="form-check-input3" id="checkbox3">
          <label class="form-check-label3" for="checkbox3">Have a third checkbox</label>
      </div>
```
# Dropdown selection

# Single Selection 

<div class="form-group">
          <label for="exampleFormControlSelect1">Select an option</label>
          <select class="form-control" id="exampleFormControlSelect1">
              <option>1</option>
              <option>2</option>
              <option>3</option>
              <option>4</option>
              <option>5</option>
          </select>
      </div>

# Multiple selection

 <div class="form-group">
        <label for="exampleFormControlSelect1">Select an option</label>
        <select multiple class="form-control" id="exampleFormControlSelect1">
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
            <option>5</option>
        </select>
    </div>

# Radio buttons
```html
  <div class="form-check-inline">
          <input class="form-check-input" type="radio" value="option1" id=defaultCheck1>
          <label class="form-check-label" for="defaultCheck1">Default checkbox</label>
      </div>

      <div class="form-check-inline">
        <input class="form-check-input" type="radio" value="option2" id=defaultCheck2>
        <label class="form-check-label" for="defaultCheck2">Second checkbox</label>
      </div>

      <div class="form-check-inline">
        <input class="form-check-input" type="radio" value="option3" id=defaultCheck3>
        <label class="form-check-label" for="defaultCheck3">Third checkbox</label>
    </div>
```

# Homework
Go through the Bootstrap tutorial for forms and create a form page - For now don't worry about page functionality we will expand on that later on

# Resources
```html
 <div class="form-group">
        <label for="exampleFormControlSelect1">Select an option</label>
        <select multiple class="form-control" id="exampleFormControlSelect1">
            <option>1</option>
            <option>2</option>
            <option>3</option>
            <option>4</option>
            <option>5</option>
        </select>
    </div>
```
- Bootstrap - Form page - Documentation and examples: https://getbootstrap.com/docs/4.0/components/forms/#select-menu

- Html buttons - https://www.w3schools.com/tags/tag_button.asp


