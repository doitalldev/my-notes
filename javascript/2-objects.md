## Objects

Each object is a unique instance of an object prototype

Can contains other objects

### Methods

Methods are property-changing features inside objects.

When the properties are changed, they do not change other objects properties

Instantiating an object:

```javascript
const myObject = {}; //I'm an object \( ﾟヮﾟ)/
```

The structure of an object:

```javascript
const backpack = {
  name: 'my backpack', //Can contain strings
  volume: 15, //Can contain numbers
  color: 'white',
  strapLength: {
    //Properties can contain sub-objects with their own properties
    left: 12,
    right: 20,
  },
  lidOpen: false, //Can contain booleans
  toggleLid: function (lidStatus) {
    //They can even contain methods which are properties containing functions
    this.lidOpen = lidStatus;
  },
  blah: {
    hi: 'hi',
  },
};
```
### This
You will often see the 'this' keyword used in objects.

The 'this' keyword refers to the current object

### Objects are typically constants

We can change the properties of the object inside the container, but we connot remove or replace the object from the container. 
