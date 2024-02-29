# CSS (Cascading Style Sheets)

 CSS is a fundamental technology in web development, crucial in creating visually appealing and functional websites and web applications. Make sure to set up our web dev environment outlined in the parent folder of this repo. In this ReadMe.md file, we'll outline some of the fundamentals for CSS and how they look in the project we just set up. 

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
3. **RGB Codes:** `color: rgb(255,0,255`
