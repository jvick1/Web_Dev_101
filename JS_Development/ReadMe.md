# JS (JavaScript)

JavaScript enables interaction with HTML elements through the Document Object Model (DOM), allowing developers to manipulate the structure, content, and style of web pages. 

```html
<html>
  <head>
    <title> My First Web Page </title>
  </head>

  <body>
    <script>
    function changeText(id) {
         id.innerHTML = "New Text";
    }
    </script>

    <h1 onclick = "changeText(this)">Click here</h1>

  </body>

</html>
```

Functions like the one defined in the provided code snippet can target specific elements by their IDs or other attributes and modify their properties, such as changing text content in response to user actions like clicks.

## Introduction

JavaScript is an object-oriented programming language primarily used for client-side web development. It enables interactive features on web pages by allowing developers to manipulate the Document Object Model (DOM) and create dynamic content and functionality.

HTML and CSS are primarily used for structuring and styling web pages, providing static elements and layout. In contrast, JavaScript is a client-side programming language, facilitating interactive behavior within web browsers. JavaScript enables dynamic communication with the browser, enhancing user experience through features like interactivity and real-time updates on web pages.

## Placement

You can enter JavaScript directly into your HTML or you could reference an external JS file with ` <script type="text/javascript" src="fileName.js">`. In the example below we calculate the user's age in dog years, we do this by multiplying their age by 7. 

```html
<html>
  <head>
    <title> Sample JavaScript </title>

  <script type="text/javascript">
    function dogYears(form) {
         form.dogage.value = form.myage.value * 7
    }

  </script>
  </head>

  <body>
    <b>FIND OUT YOUR DOG YEARS!</b>

    <form method = "post">
      <table>

      <tr>
          <td>Enter your age:</td>
          <td><input type="text" name="myage" size=15></td>
      </tr>

      <tr>
          <td>
          <input type="button" value="Calculate" onclick="dogYears(this.form)">
          </td>
      </tr>

      <tr>
          <td>Your age in Dog Years is:</td>
          <td><input type="text" name="dogage" size=15></td>
      </tr>

      </table>
    </form>
  </body>
</html>
```

## Output

There are a few types of outputs ranging from:
1. `document.write()`: Dynamically writes content to a document
2. `console.log()`: Outputs messages to the web browser's console (common for debugging)
3. `alert()`: Displays a modal dialog box with a message and an OK button
4. `prompt()`: Displays dialog box with a message, input field, and OK and Cancel buttons
5. `confirm()`: Message box with OK and Cancel buttons, prompting the user for confirmation
6. `innerHTML property`: Allows you to set the HTML content of an element dynamically. For example, `element.innerHTML = "New content";`
7. `textContent property`: Similar to `innerHTML` but sets only the text content of an element without interpreting HTML.

## Commenting Code

```HTML
<html>
<body>

<script>

  //for single line comments
  
  /*
  for
  multi
  line
  comments
  */

</script>

</body>
</html>
```
## Data Types 
In JavaScript, there are several data types used to represent different kinds of values:

1. Primitive Data Types:

- String: Represents textual data, enclosed in single or double quotes.

- Number: Represents numeric data, including integers and floating-point numbers.

- Boolean: Represents a logical value, either true or false.

- Null: Represents the intentional absence of any value.

- Undefined: Represents a variable that has been declared but not assigned a value.

- Symbol: Represents a unique identifier. Introduced in ECMAScript 6 (ES6).

2. Complex Data Types:

- Object: Represents a collection of key-value pairs, where keys are strings (or symbols) and values can be any data type, including other objects.

- Function: A special type of object that can be invoked.

- Array: A special type of object used to store ordered collections of data, indexed by integers starting from 0.

JavaScript is a dynamically typed language, meaning variables can hold values of any data type, and data types are automatically converted as needed during operations.

### Constants

Below is an example of `innerHTML` which uses `id="math"` and is set to a constant `5+6`.

```html
<html>
<head>
<title>Sample JavaScript</title>
</head>

<body>

<p id="math"></p>

<script type="text/javascript">
  document.getElementById("math").innerHTML = 5+6;
</script>

</body>
</html>
```

### Variables 

```html
<html>
<body>

<h1> JavaScript Variables </h1>

<p> Working with Variables </p>

<p id="demo></p>

<script>
var x = 10;
var y = 15;
var z = x + y;

document.getElementById("demo").innerHTML = z;

</script>

</body>
</html>
```

### Objects

A JavaScript object is a collection of key-value pairs where keys are strings (or symbols) and values can be of any data type, including other objects. Objects in JavaScript provide a way to organize and structure data.

Here's an example of a simple JavaScript object:

```js
let person = {
    name: "John",
    age: 30,
    city: "New York"
};
```

In this object keys are `name`, `age`, and `city` while `"John"`, `"30"`, and `"NYC"` are the values.

These objects can be outputted using console logging `console.log(person);`, displayed in html `document.getElementById("output").innerHTML = "Name: " + person.name + "<br>Age: " + person.age + "<br>City: " + person.city;`, alerting `alert(JSON.stringify(person));`, and string conversion like so:

```js
let personAsString = JSON.stringify(person);
console.log(personAsString);
```

### String

```html
<html>
<body>

<p id="demo></p>

<script>
var string1 = "hello world"; //normal string
var string2 = "hello 'world'"; //strings can contain quotes as long as they are the opposite
var string3 = 'hello "world"'; //opposite
var string4 = "hello \"world\""; //use a backslash for a special character

document.getElementById("demo").innerHTML = string1;

</script>

</body>
</html>
```

## Arithmetic Operators 

- `+` Addition
- `-` subtraction
- `*` multiplication
- `/` Division
- `%` Modulus
- `++` Increment
- `--` Decrement

### Random Numbers

This is a built-in JavaScript function that generates a random floating-point number between 0 (inclusive) and 1 (exclusive). It returns a random number each time it's called.

```html
<html>
<body>

<p id="demo></p>

<script>

document.getElementById("demo").innerHTML = Math.random();

</script>

</body>
</html>
```

### Min and Max Functions

The `Math.min()` function returns the smallest of zero or more numbers. `Math.max()` will return the max of the numbers. 

You can pass any number of arguments to it, separated by commas, and it will return the smallest value among those numbers.

```html
<html>
<body>

<p id="demo></p>

<script>

document.getElementById("demo").innerHTML =
Math.min(600,200,100,-20); // Returns -20

</script>

</body>
</html>
```

### Round

```html
<html>
<body>

<p id="demo></p>

<script>

document.getElementById("demo").innerHTML = Math.round(15.4); // Returns 15

</script>

</body>
</html
