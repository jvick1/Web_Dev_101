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
