# String Output using JS

Typical use of Javascript is to generate HTML, modify HTML, or remove HTML from a live document.

We can use document.innerHTML to output a string of HTML to the page.

We can use template literals, or string concatenation to provide dynamic data to the HTML of a page.

```javascript
const text = "Hello World";
const stringConcat = "<h1>" + text + "</h1>";
const templateLiteral = `<h1>${text}</h1>`;
```

With template literals, we use "${}" to insert data into the template, and backticks to let the engine know we are using template literals.