# JavaScript 101

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
```


## Arrays 

Javascript starts its index at 0. 

```html
<html>
<body>

<p id="demo></p>

<script>

var fruits = ["Apple", "Orange", "Pear", "Grape"];
document.getElementById("demo").innerHTML = fruits[0]; // Returns Apple

</script>

</body>
</html
```

### Attributes

You can find the length of an array by added `fruits.length`. 
Want the output to be a string use `toString()` this seprates all elements in an array by a comma.
Want to separate on something besides a comma? use `join(" ")`

```html
<html>
<body>

<p id="demo></p>

<script>

var fruits = ["Apple", "Orange", "Pear", "Grape"];
document.getElementById("demo").innerHTML = fruits.toString(); // Returns full array separated by a comma

</script>

</body>
</html
```

### Pop, push, shift, and unshift 

- The `pop()` method removes the last element from an array and returns that element. It mutates the original array.
- The `push()` method adds one or more elements to the end of an array and returns the new length of the array. It mutates the original array.
- The `shift()` method removes the first element from an array and returns that element. It mutates the original array.
- The `unshift()` method adds one or more elements to the beginning of an array and returns the new length of the array. It mutates the original array.

```html
<html>
<body>

<p id="demo></p>

<script>

var fruits = ["Apple", "Orange", "Pear", "Grape"];
fruits.pop();
document.getElementById("demo").innerHTML = fruits.join(" "); //this will remove grape

</script>

</body>
</html
```

### Changing and Deleting Elements

Here we change orange to kiwi and remove or delete pear. 

```html
<html>
<body>

<p id="demo></p>

<script>

var fruits = ["Apple", "Orange", "Pear", "Grape"];
fruits[1] = "Kiwi";
delete fruits[2];
document.getElementById("demo").innerHTML = fruits.join(" "); 

</script>

</body>
</html
```

### Splicing an Array

Splicing an array in JavaScript refers to the process of removing, replacing, or adding elements at specific positions within the array.

In our example, `fruits.splice(2,0,"Kiwi","Banana");` we are putting the following elements at index 2, not removing any of the other elements, adding kiwi and banana. 

```html
<html>
<body>

<p id="demo></p>

<script>

var fruits = ["Apple", "Orange", "Pear", "Grape"];
fruits.splice(2,0,"Kiwi","Banana");
document.getElementById("demo").innerHTML = fruits.join(" "); 

</script>

</body>
</html
```

### Sorting an Array

In JavaScript, the `sort()` function arranges the elements of an array in ascending order by default, or based on a specified comparison function, while the `reverse()` function reverses the order of elements in the array.

### Joining an Array

use `concat();` to join two arrays together. In the example below we have two arrays, boys and girls, we then combine them using `concat()` and print that new array. 

```html
<html>
<body>

<p id="demo></p>

<script>

var Girls = ["Julie", "Samantha", "Jill"];
var Boys = ["Bob", "Joe", "Walt"];

var Combined = Girls.concat(Boys):

document.getElementById("demo").innerHTML = Combined; 

</script>

</body>
</html
```


## Conditional Statements

Conditional statements in JavaScript, like `if`, `else if`, and `else`, allow you to execute different blocks of code based on specified conditions. These statements evaluate conditions and execute the corresponding block of code if the condition is true, providing a way to control the flow of your program based on different scenarios.

```html
<html>
<body>

<p id="demo></p>

  <script type="text/javascript">

  var score = 65;

  if(score < 50){
    document.write("F");
  }
  else if(score < 70){
    document.write("D");
  }
  else if(score < 80){
    document.write("C");
  }  
  else if(score < 90){
    document.write("B");
  }
  else if(score < 100){
    document.write("A");
  }
  else {
    document.write("Score must be less than 100.");
  }
  
  </script>

</body>
</html
```

## Comparison Operators 

These operators are used in conditional statements, comparisons, and other contexts to evaluate expressions and control the flow of the program.

1. **Equality (==)**: Compares two values for equality, allowing type coercion.
2. **Strict Equality (===)**: Compares two values for equality without type coercion; both value and type must be the same.
3. **Inequality (!=)**: Compares two values for inequality, allowing type coercion.
4. **Strict Inequality (!==)**: Compares two values for inequality without type coercion; both value and type must be different.
5. **Greater Than (>)**: Checks if the left operand is greater than the right operand.
6. **Greater Than or Equal To (>=)**: Checks if the left operand is greater than or equal to the right operand.
7. **Less Than (<)**: Checks if the left operand is less than the right operand.
8. **Less Than or Equal To (<=)**: Checks if the left operand is less than or equal to the right operand.

Below is an example of checking if a value is equal. This will return True or False. In this example we print false. 

```html
<html>
<body>

<p id="demo></p>

<script>

var x=6;
documnet.getElementById("demo").innerHTML = (x==8); 

</script>

</body>
</html
```

## Boolean

Anything that is a real number is true anything else is false. So, all of these will return true besides b7.  

```html
<html>
<body>

<p id="demo></p>

<script>

var b1 = Boolean(80);
var b2 = Boolean(2.86);
var b3 = Boolean(-10);
var b4 = Boolean("Hi");
var b5 = Boolean("false");
var b6 = Boolean(1+8+10.14);
var b7 = Boolean(0);


documnet.getElementById("demo").innerHTML = 
"80 is " + b1 + "<br>" +
"2.86 is " + b2 + "<br>" +
"-10 is " + b3 + "<br>" +
"Any (not empty) string is " + b4 + "<br>" +
"The string 'false' is " + b5 + "<br>" +
"Any expression (except zero) is " + b6 + "<br>" +
"Zero is " + b7 ; 

</script>

</body>
</html
```

## For Loop

A for loop in JavaScript is a control flow statement that iterates over a block of code multiple times, executing the same code with different values until a specified condition is met.

```html
<html>
<body>

  <script type = "text/javascript">
    var count;

    for(count=0; count <= 10; count++){
      document.write(count);
      document.write("<br />");
    }
  
  </script>

</body>
</html
```

## For-in Loop

A for-in loop in JavaScript iterates over the enumerable properties of an object, executing a specified block of code for each property until all properties have been processed.

```html
<html>
<body>

<p id="demo></p>

<script>

  var txt = "";
  var person = {fname:"Josh", lname:"Smith", age:30};
  var x;
  
  for (x in person) {
    txt += person[x] + " ";
  }
  document.getElementById("demo").innerHTML = txt;

</script>

</body>
</html
```

## While Loop

A while loop in JavaScript repeatedly executes a block of code as long as a specified condition evaluates to true, providing a flexible way to repeat tasks until the condition becomes false.

```html
<html>
<body>

<script>

  var i = 0;
  while(i<20){
    document.write(i);
    document.write("<br />");
    i++;
  }

</script>

</body>
</html
```
