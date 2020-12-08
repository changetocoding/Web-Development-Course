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
 
 
