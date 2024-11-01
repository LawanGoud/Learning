In CSS, text properties control the appearance of text, such as its color, font size, and alignment, while background properties define the styling of the element's background. Here’s a guide to using **color** and **background-color** properties:

### Text Properties

1. **Color (`color`)**

   - The `color` property changes the color of text within an element.
   - It can accept various types of values:
     - **Color names**: `red`, `blue`, `green`, etc.
     - **Hexadecimal**: `#FF5733` (for more specific colors).
     - **RGB**: `rgb(255, 87, 51)`.
     - **RGBA** (with transparency): `rgba(255, 87, 51, 0.5)`.

   ```css
   p {
     color: #333333; /* dark grey */
   }
   ```

### Background Properties

1. **Background Color (`background-color`)**

   - The `background-color` property sets the background color of an element.
   - It also accepts color values in formats like color names, hex codes, RGB, and RGBA.

   ```css
   .highlight {
     background-color: yellow; /* Sets background to yellow */
   }
   ```

2. **Background Color with Transparency**

   - When using RGBA, the fourth value controls transparency (opacity), from `0` (completely transparent) to `1` (completely opaque).

   ```css
   .faded-background {
     background-color: rgba(0, 128, 0, 0.3); /* semi-transparent green */
   }
   ```

### Example Combining Color and Background-Color

Here’s an example demonstrating the use of both `color` and `background-color`:

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="styles.css" />
    <title>Color and Background Example</title>
  </head>
  <body>
    <div class="highlight">
      <h1 class="title">Welcome to Styling with CSS</h1>
      <p class="text">This text has a specific color and background.</p>
    </div>
  </body>
</html>
```

**CSS (`styles.css`):**

```css
/* Setting text color */
.title {
  color: #4a90e2; /* Blue color */
}

/* Setting text and background color */
.text {
  color: #ffffff; /* White text */
  background-color: #333333; /* Dark grey background */
  padding: 10px;
}

/* Setting background color for the div container */
.highlight {
  background-color: #f0f8ff; /* Light blue background */
  padding: 20px;
  border-radius: 8px;
}
```

In this example:

- The **`.title`** class applies a blue text color.
- The **`.text`** class makes the text white on a dark background.
- The **`.highlight`** class applies a light blue background color to the container and adds some padding and rounded corners.

Using `color` and `background-color` properties helps create contrast and highlight different areas, improving readability and visual appeal.
