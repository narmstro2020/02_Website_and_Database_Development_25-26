# Assignment 1: Color Palette Creator

## Objective
Create a webpage that demonstrates your understanding of CSS color formats by building a color palette showcase. You will create color swatches using different color formats and apply them to various HTML elements.

## Requirements

### HTML Structure
Create an HTML file with:
1. A main heading (h1) for the page title

### CSS Requirements
You must demonstrate ALL of the following color formats:
1. **Named Colors Section**: Use at least 5 different named colors
2. **Hexadecimal Section**: Use both full (#RRGGBB) and shorthand (#RGB) hex colors
3. **RGB Section**: Create colors using rgb() values
4. **RGBA Section**: Show transparency with at least 3 different alpha values
5. **HSL Section**: Create a color scheme using hsl()
6. **HSLA Section**: Combine HSL with transparency
   
## Starter Code

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Color Palette Showcase</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
   
    <main>
        <section>
            <h1>Named Colors</h1>
            <h2>Hex Color</h2>
            <h3>RGB Color</h3>
            <h4>RGBA Color</h4>
            <h5>HSL Color</h5>
            <h6>HSLA Color</h6>
        
    </main>
    

</body>
</html>
```

styles.css
```css
h1{

}

h2{

}

h3{

}

h4{

}

h5{

}

h6{

}


```


## Tips
- Use comments in your CSS to label each color format section
- Test transparency by overlapping elements
- Remember that HSL hue values go from 0-360 degrees
- For the rainbow, think about the color wheel
- A monochromatic scheme can use different lightness or saturation values

## Submission
Submit two files:
1. `color-palette.html` - Your complete HTML file with embedded CSS
2. A screenshot of your rendered webpage

## Bonus Challenge (Optional)
Create a "color card" design where each color swatch looks like a physical card with:
- A shadow effect using RGBA
- The color value displayed as text on the card
- Rounded corners using CSS you research yourself
