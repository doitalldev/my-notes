# The DOM

### What is the DOM?

The DOM, or Document Object Model, is a hierarchical tree that represents the structure of a web page.

Being able to traverse the DOM is an essential skills to learn with Javascript.

### Accessing elements

We have multiple ways to access elements in the DOM. The 2 most popular are:

- querySelector
- querySelectorAll

With these methods, we use CSS selectors ("#", ".") to target the elements

```javascript
// This variable would target the first element with the id "id"
const element = document.querySelector('#id');

// This variable would return all elements with the class "class"
const allElements = document.querySelectorAll('.class.);
```


### Older ways to access elements

There are older methods you can use to access elements:
- getElementById
- getElementsByClassName

These are still perfectly valid, and you may see them in older code, but using querySelector is much mor efficient and cleaner.

### Modifying Element Classes
