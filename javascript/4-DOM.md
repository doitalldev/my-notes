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

### Attributes
When grabbing attributes, we will get back a NamedNodeMap which is NOT and array and won't accept array methods. It is a key/value pair of strings. 

For attributes, we have dedicated methods:
```javascript
element.getAttribute('attributeName'); // returns the value of the attribute
element.hasAttribute('attributeName'); // returns true of false if the attribute exists
element.setAttribute('attributeName', 'attributeValue'); // sets a new or modifies an existing attribute
element.removeAttribute('attributeName'); // removes and attribute
```
The class is also show up as an attribute. Of course there are dedicated methods for this, but it's possible.

### Inline Styles
We can of course set inline style in HTML:
```html
<div style="color: black;">Hi</div>
```
But what about using Javascript to set or modify those styles?

With "querySelector" we can target the element, and use dot notation to acces the style property, then target color:
```javascript
document.querySelector('div').style.color = "blue";
```
And now our div would be blue.

There is also a cssText property, this contains the entirety of the style attribute, but it is recommended to stick to tergeting the property individually.
