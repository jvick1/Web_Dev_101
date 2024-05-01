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
