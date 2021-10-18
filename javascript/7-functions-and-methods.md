# Functions
Functions are a series of steps, and based on the outcome of these steps, we decide what to do next.

You can have a function "return" data or just have it output or modify data directly

```javascript
// Function declaration
function doSomething(){
return 'something';
}

// Function expression
const doSomethingSomething = function () {
return 'something something'
}

// IIFE or immediate invoked function expression
(function () {
let do = 'do';
let something = 'something';
console.log(do + ' ' + something)
})(); 
// This function is immediately invoked and ran. An antipattern, but can be handy
```


### Arrow functions
We remove the word 'function' and add an arrow:
```javascript
(a) => {
return a;
}

// You could even omit the parentesis as if you are just passing one parameter
// You can do it, but it's not as easy to read so not recommended
const test = a => {
return a;
}

// Further examples are ways you may come across, but not necessarily recomended due to their difficulty in reading sometimes
(a) => a + 100;
a => a + 100;
```

### Parameters
Parameters are the info you pass in that are defined at the beginning of the function.
```javascript
const parameterFunction = (parameter1, parameter2) => {
// these params act as 'placeholders' or names to the info that is passed in when the function is called
return parameter1 + parameter2;
}

parameterFunction(1,1)
```

### Callbacks
Callback functions are used to allow the control of order of completiong within your program. Let's say a function is dependant on another function to finish, maybe it was grabbing data. You use a callback function to then process that data once the getData function is complete.

```javascript
const function0 = (num3, num4) => {
return num3 + num4;
}

const function1 = (num1, num2, callback) => {
let numbers = num1 + num2;

let otherNumbers = callback(3,4)

return numbers + otherNumbers;
}

function1(1,2, function0)


```




