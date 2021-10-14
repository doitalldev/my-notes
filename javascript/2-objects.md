## 1. Objects

Each object is a unique instance of an object prototype

Can contains other objects

### 1.1. Methods

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

### 1.2. This

You will often see the 'this' keyword used in objects.

The 'this' keyword refers to the current object

### 1.3. Objects are typically constants

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

### 1.4. Object Properties

Describe the different aspects of the object

```javascript

const cup = {

color: 'blue';
//^       ^
//Key   Value
}
```

### 1.5. Accessing objects

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

### 1.6. Practice

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

### 1.7. Methods

A method is a function, defined as a property, inside an object. At least that is how I would describe it. It looks something like this:

```javascript
const cup = {
  lidOpen: true,
  //Below is a method
  toggleLid: function (lidStatus) {
    this.lidOpen = lidStatus;
  },
  // It sets the object's lidOpen property to whatever the parameter lidStatus is: cup.toggleLid(false)
};
```

### 1.8. Classes

Classes work as a template for an object type. When you create a new object from a class, the object automatically gets the properties and methods from that class.

When changing a property or method of the class, that change will cascade to every object made with that class.

There are 2 ways to create a class:

- Declaration: class Name{}
- Expression: const Name = class {}

Class Example:

```javascript
class Bucket {
  //The constructor is exactly as the name suggests. It "constructs" the object created from this class
  // We define the parameters in the ()
  // Then define the properties in {}
  constructor(name, color, handle, spout, lid) {
    // Define properties
    this.name = name;
    this.color = color;
    this.handle = handle;
    this.spout = spout;
    this.lid = lid;
  }
}

// then we can use the class to create a new object with the same properties:

const myBucket = new Bucket('My Bucket', 'Blue', true, 'Wide', 'Open');
```

There are also "constructor functions". The end result is effectively the same, but Classes allow us to do more things like extending it.

### 1.9. Global Object

Global objects are standard built-in objects

Lets say we want to add add a property to our Bucket class that shows us when we acquired to the bucket:

```javascript
class Bucket {
  //The constructor is exactly as the name suggests. It "constructs" the object created from this class
  // We define the parameters in the ()
  // Then define the properties in {}
  constructor(name, color, handle, spout, lid, dateAcquired) {
    // Define properties
    this.name = name;
    this.color = color;
    this.handle = handle;
    this.spout = spout;
    this.lid = lid;
    this.dateAcquired = dateAcquired;
  }

  bucketAge() {
    let now = new Date();
    let acquired = new Date(this.dateAcquired);
    let elapsed = now - acquired;
    let daysSinceAcquired = Math.floor(elapsed / (1000 * 3600 * 24));
    return daysSinceAcquired;
  }
}

const myBucket = new Bucket(
  'My Bucket',
  'Blue',
  true,
  'Wide',
  'Open',
  'December 5, 2020 1:00:00 MST'
);
```
