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

In our example HTML code, we can play around with this by adding in an `id` to our main text blob.

```html
<p id = "main-content">
  ...
</p>
```

Then call the `id` in the CSS file with a `#` and update the font size to 12px. 

```css
#main-content {
  font-size: 12px;
}
```

## CSS Margins

Margins can be applied to all four sides of an element (top, right, bottom, and left), or individually. Margins are defined using the `margin` property in CSS. The syntax allows you to specify the margin for all sides at once (`margin: value;`), or individually for each side (`margin-top`, `margin-right`, `margin-bottom`, `margin-left`).

Margins can be specified using various units, such as pixels (`px`), percentages (`%`), ems (`em`), rems (`rem`), and more. Percentages are often used for responsive design to create margins relative to the size of the containing element.

```css
/* Apply the same margin to all sides */
margin: 10px;

/* Apply different margins to each side */
margin-top: 10px;
margin-right: 20px;
margin-bottom: 10px;
margin-left: 20px;

/* SHORTHAND */
/* One value applies to all sides */
margin: 10px;

/* Two values: top/bottom, left/right */
margin: 10px 20px;

/* Three values: top, left/right, bottom */
margin: 10px 20px 15px;

/* Four values: top, right, bottom, left */
margin: 10px 20px 15px 25px;
```

## Padding

Padding refers to the space between the content of an element and its border. Padding has the same syntax as margin for example, `padding: 10px;`.

![image](https://github.com/jvick1/Web_Dev_101/assets/32043066/b2b36da9-6d98-4580-b727-f13b38bd7eb2)

## Borders

In CSS, borders are used to create lines or outlines around elements, separating them visually from surrounding content. They can be applied to any block-level or inline element, such as `<div>`, `<p>`, `<span>`, etc. Borders can be dashed, dotted, double, groove, hidden, inset, outset, ridge, solid, none. 

```css
border: 4px;
border-color: #333;
border-style: dashed;
```

or if you want some cleaner code try the following:

```css
border: 4px dashed #333;
```

## Text Properties

Text properties are used to control the appearance and behavior of text content within HTML elements. These properties allow developers to specify various aspects of text styling, such as font size, font family, font weight, text color, alignment, decoration, spacing, and more. Here are some commonly used text properties in CSS:

1. **font-family**: Set the font family or typeface to be used for the text content. Multiple fonts can be listed as fallback options if the primary font is not available. 

```css
font-family: Arial, sans-serif;
```

2. **font-size**: Sets the size of the text. It can be specified in various units such as pixels, ems, rems, percentages, etc.

```css
font-size: 16px;
```

3. **font-weight**: Sets the thickness or boldness of text. Can be keywords like `normal` or `bold`, or numeric values like `100`, `400`, etc.

```css
font-weight: bold;
```

4. **font-style**: Sets the style of the font, such as italic or normal.

```css
font-style: italic;
```

5. **text-align**: Sets alignments of text within its containing element. Common values include `left`, `right`, `center`, and `justify`.

```css
text-align: center;
```

6. **text-decoration**: Sets decorations added to text, such as underline, overline, line-through, or none.

```css
text-decoration: underline;
```

7. **color**: Sets the color of the text content.

```css
color: #333;
```

8. **line-height**: Controls the height of each line of text. It can be set as a unitless number, percentage, or specific length value.

```css
line-height: 1.5;
```

9. **letter-spacing**: Specifies the spacing between characters in the text.

```css
letter-spacing: 1px;
```

10. **word-spacing**: Controls the spacing between words in the text.

```css
word-spacing: 2px;
```
11. **text-transform**: Sets text to lowercase, uppercase, capitalize, etc.

```css
text-transform: capitalize; 
```
## Backgrounds

The `background` property in CSS allows you to set various background-related properties, such as background color, image, position, repeat behavior, and more. Here's an overview of CSS background properties:

1. **background-color**: Sets the background color of an element.
```css
background-color: #fff;
```

2. **background-image**: Sets an image to be used as the background of an element.
```css
background-image: url('path/to/image.jpg');
```

3. **background-repeat**: Sets how a background image should be repeated if it doesn't fill the entire background area.
```css
background-repeat: repeat-x;
```

4. **background-position**: Sets the starting position of a background image within its container.
```css
background-position: center top;
```

5. **background-size**: Sets the size of the background image.
```css
background-size: cover;
```

6. **background-attachment**: Sets whether the background image scrolls with the content or remains fixed in place as the user scrolls the page
```css
background-attachment: fixed;
```
## Transparency

Opacity values range from 0 (completely transparent) to 1 (completely opaque). Here's how you can control transparency in CSS:

Let's do an example with our existing code. I want to make `.App-logo` fade 40% when I hover over the icon. How can I do this? Hint remove `pointer-events: none;` from the `App.css` file.

**Solution:** in our `App.css` remove `pointer-events: none;`, we'll add a starting `opacity` set to 1, add a `transition` on opacity, and set the hover `opacity` to `0.6`.

```css
.App-logo {
  height: 40vmin;
  opacity: 1;
  transition: opacity 0.3s ease;
}

.App-logo:hover {
  opacity: 0.6;
}
```
