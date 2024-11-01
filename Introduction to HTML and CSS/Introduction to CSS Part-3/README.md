In CSS, **font** properties allow us to style text by adjusting its font type, size, weight, and more. Here’s a guide to common font properties:

### 1. Font Family (`font-family`)

The `font-family` property specifies the font type for an element. You can set one or multiple fonts as a "font stack" (a list of fonts) to ensure compatibility across different browsers and devices.

- Font families can include generic names like `serif`, `sans-serif`, or specific font names like `Arial` or `Times New Roman`.
- When specifying multiple fonts, separate them with commas. The browser will use the first available font.

```css
p {
  font-family: Arial, Helvetica, sans-serif;
}
```

In this example, the text will use **Arial** first. If Arial isn’t available, it will fall back to **Helvetica**, and finally to a **generic sans-serif** font.

### 2. Font Size (`font-size`)

The `font-size` property controls the size of the font. Font sizes can be specified in units like:

- **Pixels (`px`)**: Fixed size, such as `16px`.
- **Ems (`em`)**: Relative to the parent element’s font size, e.g., `1.5em`.
- **Percentages (`%`)**: Relative to the parent element, e.g., `120%`.
- **Rems (`rem`)**: Relative to the root element’s font size.

```css
h1 {
  font-size: 2em; /* 2 times the base font size */
}

p {
  font-size: 16px;
}
```

### 3. Font Style (`font-style`)

The `font-style` property specifies the style of the font, with the following values:

- **Normal**: Default, no emphasis.
- **Italic**: Slants the text.
- **Oblique**: Similar to italic but with a slightly different slant.

```css
em {
  font-style: italic;
}
```

This example makes `<em>` (emphasized) text italic.

### 4. Font Weight (`font-weight`)

The `font-weight` property controls the thickness (boldness) of the font. It can take numeric values (`100` to `900`) or keywords:

- **Normal**: Default weight.
- **Bold**: Bold weight.
- **Bolder** or **Lighter**: Relative to the parent’s font weight.

```css
strong {
  font-weight: bold;
}

h2 {
  font-weight: 600; /* Semi-bold */
}
```

### 5. Text Decoration (`text-decoration`)

The `text-decoration` property applies additional styling to text, such as:

- **Underline**: Adds a line under the text.
- **Overline**: Adds a line above the text.
- **Line-through**: Strikes a line through the text.
- **None**: Removes any decoration (e.g., removes the underline on links).

```css
a {
  text-decoration: none; /* Removes underline from links */
}

.strikethrough {
  text-decoration: line-through; /* Adds a line through text */
}
```

### Example Combining Font Properties

Here’s an example of using multiple font properties together in HTML and CSS:

**HTML:**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Font Properties Example</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <div class="content">
      <h1 class="title">Styling Fonts with CSS</h1>
      <p class="text">This paragraph demonstrates various font properties.</p>
      <p class="highlight">This text is bold, italic, and underlined.</p>
    </div>
  </body>
</html>
```

**CSS (`styles.css`):**

```css
/* Setting font family, size, and color for titles */
.title {
  font-family: "Georgia", serif;
  font-size: 2rem;
  font-weight: bold;
}

/* Setting font size and font-style for text */
.text {
  font-family: Arial, sans-serif;
  font-size: 1rem;
  color: #333;
  font-style: normal;
}

/* Styling for emphasized text */
.highlight {
  font-weight: bold;
  font-style: italic;
  text-decoration: underline;
  font-size: 1.2rem;
}
```

In this example:

- The **`.title`** class applies a serif font, increases font size, and makes the text bold.
- The **`.text`** class uses a sans-serif font, a base font size, and a darker color.
- The **`.highlight`** class combines bold, italic, and underlined styling, along with a slightly larger font size.

These properties allow for flexible control over text, making it easy to create a readable and aesthetically pleasing design.
