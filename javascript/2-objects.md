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

Example:

```javascript
const cup = {
  color: blue,
  capacity: 8,
  capacityType: 'oz',
};

----------
cup = 5; // Doesn't work because we are reassigning a const variable
----------
cup.radius = 5; // Works because we are modifying or creating a property of the object
```

### Object Properties

Describe the different aspects of the object

```javascript

const cup = {

color: 'blue';
//^       ^
//Key   Value
}
```

### Accessing objects

Usually people use in order to test accessing objects. You can access and objects properties by using dot notation.

```javascript
console.log(cup);
console.log(cup.color);
```

Dot notation is called dot notation because you literally use dots (periods) to drill down into an object.

There is also bracket notation, this gives slightly more control but is usually harder to read. We are able to pass variables as name into bracket notation.

```javascript
const test = color;
cup[test];
```

Now why would you need to use bracket notation? This is because you may get non-standard property names in data. Maybe it starts with (or contains) a number or hyphen or underscore. Bracket notation allows you to specify that property by passing a string. Ex:

```javascript
cup['color'];
```

### Practice

- Give object and identifiable name
- Create properties to describe the object and set the values
- Give it another object inside of it
  ```javascript
  const babyCrib = {
    color: 'white',
    bed: true,
    feet: 4,
    blanket: {
      color: 'white',
      animals: true,
    },
  };
  ```
