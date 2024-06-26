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

## Width and Height

The `width` property sets the width of an element. The `min-width` property sets the minimum width that an element can be resized to. Lastly `max-width` sets the maximum width of an element preventing it from becoming wider than the specified value. 

The same concepts apply to the `height` element and use the same syntax. 

```css
.element {
    width: 300px;
    min-width: 100px;
    max-width: 500px;
}
```

## Nested Divs

The outer <div> element that contains both the image and the text is referred to as the "Container". Within the Container <div>, you'll have two nested <div> elements: one for the image and one for the text. In the example below we place text on top of images all contained in a container div. 

```css
<div class="container">
    <div class="image">
        <img src="example.jpg" alt="Example Image">
    </div>
    <div class="text">
        <h2>Text on Top of Image</h2>
        <p>This is some text that appears on top of the image.</p>
    </div>
</div>
```

## Display Properties

The display property specifies the type of display box used for an element. It can be set to various values, such as block, inline, inline-block, flex, grid, table, etc., The visibility property determines whether an element is visible or hidden without affecting the layout of surrounding elements. The float property specifies whether an element should be floated to the left or right side of its container. The position property determines the positioning method used for an element. Values include static, relative, absolute, fixed, and sticky, each affecting how the element is positioned within its containing element. The overflow property specifies how content that overflows the element's box should be handled. It can be set to visible, hidden, scroll, or auto.

```css
.element {
    display: block; /* Element displayed as a block-level element */
    visibility: hidden; /* Element is invisible but still occupies space */
    float: left; /* Element floated to the left */
    position: absolute; /* Element positioned absolutely */
    overflow: hidden; /* Content that overflows the element is hidden */
}
```

## CSS Positioning 

The CSS position property specifies the positioning method used for an element. There are four main values for the position property: static, relative, absolute, and fixed. These positioning values allow you to precisely control the placement of elements on the page, enabling you to create complex layouts and designs in CSS. Understanding how each positioning value works is essential for effective web development.

The `static` value is the default positioning method for elements. Elements with `position: static;` are positioned according to the normal document flow. Elements with position: static; are not affected by the top, right, bottom, or left properties.

```css
.element {
    position: static;
}
```

The `relative` value positions an element relative to its normal position in the document flow. When an element is set to `position: relative;`, you can use the top, right, bottom, and left properties to offset it from its original position.

```css
.element {
    position: relative;
    top: 10px;
    left: 20px;
}
```

The `absolute` value positions an element relative to its nearest positioned ancestor (an ancestor with a position other than static).
If no positioned ancestor is found, the element is positioned relative to the initial containing block (usually the <html> element).

```css
.element {
    position: absolute;
    top: 0;
    right: 0;
}
```

The `fixed` value positions an element relative to the browser window's viewport, so it remains fixed in its position even when the page is scrolled. Fixed-positioned elements are not affected by scrolling.

```css
.element {
    position: fixed;
    top: 20px;
    right: 20px;
}
```

## Float & Clear Properties

The CSS `float` property is used to specify whether an element should be floated to the left or right side of its container, allowing content to flow around it. This property is commonly used for creating layouts where elements are positioned side by side or where text wraps around images.

The `float` property can be set to left, right, or none.

```css
.float-left{
   float: left;
}
```

The `clear` property controls the behavior of elements adjacent to floated elements. When an element is floated, other elements may wrap around it, causing layout issues. The `clear` property ensures that an element does not wrap around a floated element by specifying whether it should be placed below the floated element or not.

The `clear` property can be set to left, right, both or none.

```css
.clear-left {
    clear: left;
}
```

## Z-Index

The CSS `z-index` property controls the stacking order of positioned elements along the z-axis (depth) within a stacking context. When elements overlap on a webpage, the `z-index` property determines which element appears on top of the others.

The higher the `z-index` value, the closer the element is to the top of the stacked order and more likely to appear in front of other elements. Negative values are allowed and can be used to position elements behind others.

```css
.element1 {
    position: relative;
    z-index: 2;
}

.element2 {
    position: relative;
    z-index: 1;
}
```

In this example, `element1` will appear on top of `element2` because it has a higher `z-index` value.

## CSS Styling Links

You can style links using different pseudo-classes to specify their appearance in various states, such as unvisited, visited, hover, and active. These pseudo-classes allow you to customize the visual presentation of links based on user interaction and their browsing history.

**Unvisited** defined as `link` is the default link class. In the example below our link will be blue with no underline. 

**Visited** defined as `visited` shows that the user has already visited this link. In our example, the link will be purple.

**Hover** defined as `hover` is a pseudo-class that activates when the user's mouse cursor hovers over the link. Our code will add an underline to the link when we hover.

**Active** is defined as `active` changing the link when they are being activated or clicked by the user. Our code will make the link background yellow.

```css
/* Default link styles */
a:link {
    color: blue;
    text-decoration: none; /* Remove underline by default */
}

/* Visited link styles */
a:visited {
    color: purple;
}

/* Hover styles */
a:hover {
    text-decoration: underline; /* Underline on hover */
}

/* Active styles */
a:active {
    background-color: yellow; /* Yellow background when clicked */
}
```

## CSS Tables

First, let's look at HTML:
The `<table>` element is the container for the entire table. It contains one or more `<tr>` (table row) elements. Rows can contain one or more `<th>` (header cell) or `<td>` (table data) elements.

```html
<!--link to css folder-->
<link href="/css/table.css" rel="stylesheet">

<!-- Content -->
<div class="container">
<div>
    <div class="container">
      <table>
        <thead>
          <tr role="row" style="background-color:#4879aa">
            <th style="color:#fff">Header 1</th>
            <th style="color:#fff">Header 2</th>
            <th style="color:#fff">Header 3</th>
            <th style="color:#fff">Header 4</th>
            <th style="color:#fff">Header 5</th>
            <th style="color:#fff">Header 6</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>row 1.1</td>
            <td>row 1.2</td>
            <td>row 1.3</td>
            <td>row 1.4</td>
            <td>row 1.5</td>
            <td>row 1.6</td>
          </tr>
          <tr>
            <td>row 2.1</td>
            <td>row 2.2</td>
            <td>row 2.3</td>
            <td>row 2.4</td>
            <td>row 2.5</td>
            <td>row 2.6</td>
          </tr>
          <tr>
            <td>row 3.1</td>
            <td>row 3.2</td>
            <td>row 3.3</td>
            <td>row 3.4</td>
            <td>row 3.5</td>
            <td>row 3.6</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>
```

This CSS snippet improves a table's appearance and usability. It ensures full-width responsiveness, seamless borders, and subtle shadow effects.

```css
table {
	width:100%;
	border-collapse: collapse;
	overflow: hidden;
	box-shadow: 0 0 20px rgba(0,0,0,0.2);
}

th, td {
	padding: 15px;
	background-color: rgba(40, 40, 40, 0);
	color: #0D0D0D;
}

th {
	text-align: left;
}

thread th {
	background-color: #55608f;
}

tbody tr:hover,
td:hover::before {
	background-color: rgba(40, 40, 40, 0.1);
}

td:hover:before {
	content: "";
	position: absolute;
	left: 0;
	right: 0;
	top: -9999px;
	bottom: -9999px;
	background-color: rgba(40, 40, 40, 0.1);
	z-index: -1;
}
```

## Project

