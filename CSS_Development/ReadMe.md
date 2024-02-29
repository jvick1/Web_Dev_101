# CSS (Cascading Style Sheets)

## CSS Rules contain 3 parts: 
`Selector {Property: Value}`

In the example below, the `Selectors` are the two headers 1 & 2, the `properties` are Font & Color, and the `values` are Georgia & red:

```css
H1, H2 {
	Font-family: Georgia;
	Color: red;
}
```

## There are 3 types of CSS Styles: 

1. **Internal** – the style sheet is contained within the same HTML sheet in which the styles are used
2. **External** – reference the styles in an external CSS file we do this with `<link rel=”stylesheet” href=”mystyles.css”>`
3. **Inline** – style rules are added directly inside the element. **Note** this is usually not a good practice and tends to be inefficient
