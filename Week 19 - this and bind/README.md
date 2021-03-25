# this

this keyword refers to the calling function, 

Example code using this


# The problem with the code
```js
convertToDataURI() {
      //const preview = document.querySelector('img');
      const file = document.querySelector('input[type=file]').files[0];
      const reader = new FileReader();
      const self = this;
      reader.addEventListener(
        'load',
        function () {
          // convert image file to base64 string
          this.imageURL = reader.result;
          console.log(this.imageURL);
        },
        false
      );

      if (file) {
         reader.readAsDataURL(file);
         
      }
    },
    
    SubmitChanges() {
      
      const payload = {name: this.brokeragename, emailAddress: this.brokerageemail, importantInformation: this.brokerageinfo, logo: this.imageURL, disclaimerFooter: this.brokeragedisclaimer, tenant: this.brokeragetenant, primaryColour: this.primarycolor.toString(), secondaryColour: this.secondarycolor.toString()} ;
      axios.post(`/api/brokerage/brokerage/{brokerageid}/postbrokerage`, payload )
    },
  },
```

The problem with this code is that when we call imageURL for our payload, imageURL returns an empty string despite the imageURL value being set when we convert an image file into a data url to be stored in our database. 

We can solve this problem through in two ways

# self
We can create a new variable called self and assign it the value of this, when we call our imageURL variable we can use self instead.

```js
convertToDataURI() {
      //const preview = document.querySelector('img');
      const file = document.querySelector('input[type=file]').files[0];
      const reader = new FileReader();
      const self = this;
      reader.addEventListener(
        'load',
        function () {
          // convert image file to base64 string
          self.imageURL = reader.result;
          console.log(self.imageURL);
        },
        false
      );

      if (file) {
         reader.readAsDataURL(file);
         
      }
    },
    
    SubmitChanges() {
      
      const payload = {name: this.brokeragename, emailAddress: this.brokerageemail, importantInformation: this.brokerageinfo, logo: this.imageURL, disclaimerFooter: this.brokeragedisclaimer, tenant: this.brokeragetenant, primaryColour: this.primarycolor.toString(), secondaryColour: this.secondarycolor.toString()} ;
      axios.post(`/api/brokerage/brokerage/{brokerageid}/postbrokerage`, payload )
    },
  },
```

# bind
The other way we can do this is using the .bind keyword and binding our function

```js
convertToDataURI() {
      //const preview = document.querySelector('img');
      const file = document.querySelector('input[type=file]').files[0];
      const reader = new FileReader();
      reader.addEventListener(
        'load',
        function () {
          // convert image file to base64 string
          this.imageURL = reader.result;
          console.log(this.imageURL);
        }.bind(),
        false
      );

      if (file) {
         reader.readAsDataURL(file);
         
      }
    },
    
    SubmitChanges() {
      
      const payload = {name: this.brokeragename, emailAddress: this.brokerageemail, importantInformation: this.brokerageinfo, logo: this.imageURL, disclaimerFooter: this.brokeragedisclaimer, tenant: this.brokeragetenant, primaryColour: this.primarycolor.toString(), secondaryColour: this.secondarycolor.toString()} ;
      axios.post(`/api/brokerage/brokerage/{brokerageid}/postbrokerage`, payload )
    },
  },
```

# Homework

# Resources

Bind - https://javascript.info/bind

This - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this

This (Stack overflow) - https://stackoverflow.com/questions/3127429/how-does-the-this-keyword-work
