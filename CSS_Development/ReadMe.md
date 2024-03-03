# CSS (Cascading Style Sheets)

 CSS is a fundamental technology in web development, crucial in creating visually appealing and functional websites and web applications. Make sure to set up our web dev environment outlined in the parent folder of this repo. 
 
 In this ReadMe.md file, we'll outline some of the fundamentals for CSS and how they look in the project we just set up. 

## CSS Rules: 
Rules contain 3 parts `Selector {Property: Value}`

In our `App.css` file, our first `Selectors` is our div class named `App`, the `property` is `text-align`, and the `value` is `centered`:

```css
.App {
  text-align: center;
}
```

## CSS Styles: 

There are 3 types of CSS Styles:
1. **Internal** – the style sheet is contained within the same HTML sheet in which the styles are used
2. **External** – reference the styles in an external CSS file we do this with `<link rel=”stylesheet” href=”mystyles.css”>`
3. **Inline** – style rules are added directly inside the element. **Note:** This is usually not a good practice and tends to be inefficient

In our code, we are using external CSS. In our App.js file we can see the import statement at the top of the file `import './App.css';`.

## Color Names and Codes:

There are 3 types of ways to use color in CSS:
1. **Color Names:** `color: red;`
2. **Hex Codes:** `color: #33adff;`
3. **RGB Codes:** `color: rgb(255,0,255)`

## Classes & Spans:

In our `App.css` file, we can see an example of a class called App-header. One thing to note is that each class starts with a period. We then have class definitions like background color, font size, etc. Classes are a fundamental concept in CSS that greatly enhances the flexibility, maintainability, and scalability of your stylesheets.

```css
.App-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}
```

Calling the class is easy. Back in our App.js file we simply call the class' name.

```html
<header className="App-header">
  ...
</header>
```

A `<span>` is an inline HTML element used to apply style to a specific text/content. `<span>` can be also use `className`. Below is an example to illustrate the point but this is not used in our current code. 

```html
<p>This is <span style="color: blue;">blue</span> text.</p>
```

## Divisions (DIVs)

In HTML, `<div>` is a block-level element used as a generic container to group and structure content within a web page. `<div>`s are useful for **Grouping Content** within a webpage. For example, you might use `<div>` elements to contain a header, navigation menu, main content area, sidebar, footer, etc. `<div>` elements provide a way to apply **CSS styles** and layout properties to specific sections of a webpage. You can target `<div>` elements using CSS selectors to control their appearance, positioning, size, etc.

In the code we generated our `<div>` has a className App which we call in the CSS file to customize it.

```html
<div className="App">
   ...
</div>
```

## CSS IDs

An ID is a unique identifier assigned to an HTML element. Each ID must be unique within the HTML document. IDs are defined using the `id` attribute in HTML and preceded by a hash symbol (`#`) in CSS selectors.

IDs and classes are both important tools in CSS for styling HTML elements, with IDs providing unique identification and high specificity, while classes offer flexibility, reusability, and grouping capabilities.

In our example code we can play around with this by adding in an `id` to our main text area.

```html
<p id = "main-content">
  ...
</p>
```
Then call the `id` in the CSS file and update the font size to 12. 

```css
#main-content {
  font-size: 12px;
}
```
