 # Week 7 - Bootstrap Revision
 
 # BootStrap Recap
 
 Bootstrap is a CSS framework used to create responsive and mobile-first websites
 
 # Bootstrap containers
 A bootstrap container is a layout element that allows us to create a layout for our html pages
 
 There are two ways of creating a bootstrap container
 ```html
 <div class="container">
 
 </div>
 ```
 
 ```html
 <div class="container-fluid">
 
 </div>
 ```

 # Bootstrap grid layout
 Bootstrap allows us to use a grid layout on our containers to create a set of rows and columns to divide our content layout into.
  ```html
<div class="container">
      <div class="row">
        <div class="col-sm">
            Column 1
        </div>

        <div class="col-6">
          Column 2
        </div>

        <div class="col-sm">
          Column 3
        </div>
      </div>

      <div class="row">
        <div class="col">
          Column 1
        </div>

        <div class="col-5">
          Column 2
        </div>
      </div>
    </div>
  ```
 # Cards
 A card is a content container that has options for headers and footers, images, text and links
 
  ```html
     <div class="card" style="width: 18rem;">
    <img class="card-img-top" src="..." alt="Card image cap">
    <div class="card-body">
      <h5 class="card-title">Card title</h5>
      <p class="card-text">Example text</p>
      <a href="#" class="btn btn-primary">Go here</a>
    </div>
    </div>
  ```

We can use BootStrap's grid layout for cards

 ```html
    <div class="row">
      <div class="col-sm-6">
        <div class="card">
          <h3 class="card-title">Special title</h3>
          <p class="card-text">AAAAAAAAAAAAAAAAAAAAAAAAAA</p>
          <a href="#" class="btn btn-primary">Go</a>
        </div>
      </div>
      <div class="col-sm-6">
        <div class="card">
          <h3 class="card-title">Special title</h3>
          <p class="card-text">AAAAAAAAAAAAAAAAAAAAAAAAAA</p>
          <a href="#" class="btn btn-primary">Go</a>
        </div>
      </div>
    </div>
 ```  
 # Collapse
 We can collapse elements using BootStrap's collapse component
 
  ```html
 <p>
      <a class="btn btn-primary" data-toggle="collapse" href="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
         Link with href
      </a>
      <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
        Button with data-target
      </button>
    </p>

    <div class="collapse" id="collapseExample">
      <div class="card">
        <div class="card-body">
          This is a card body
        </div>
      </div>
    </div>
  ```
  
 # Navbar
 We can create a navigation bar to move between pages using bootstrap
   ```html
 <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#"></a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home <span class="sr-only">(current)></span></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Pricing</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#">Disabled</a>
          </li>
        </ul>
      </div>
    </nav>
  ```
  # List Group
  We can create a group of list items in BootStrap using Bootstrap's list group.
  
  ```html
  <ul class="list-group">
      <li class="list-group-item">Cras justo odio</li>
      <li class="list-group-item">Dapibus ac facilisis in</li>
      <li class="list-group-item">Morbi leo risus</li>
      <li class="list-group-item">Porta ac consectetur ac</li>
      <li class="list-group-item">Choco chip</li>
    </ul>
  ```
  
  # Lesson Links
  
  Bootstrap Grid Layout - https://getbootstrap.com/docs/4.0/layout/grid/
  Cards - https://getbootstrap.com/docs/4.0/components/card/
  Collapse - https://getbootstrap.com/docs/4.0/components/collapse/
  Navbar - https://getbootstrap.com/docs/4.0/components/navbar/
  Buttons - https://getbootstrap.com/docs/4.0/components/buttons/
  List group - https://getbootstrap.com/docs/4.0/components/list-group/
  
