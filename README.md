# Introduction to React JS

- MERN Stack
  - Introduction to React JS
- React
  - React.createElement
  - ReactDOM.render
- JSX
  - Embedding Expressions
  - Nesting elements

### Why React JS?

React JS is a **JavaScript library** used for building user interfaces, particularly for **single-page applications** where you need a smooth and dynamic experience. Here’s why it’s popular:

1. **Component-Based Architecture**: React encourages breaking down your UI into **reusable components**. This makes it easier to maintain and update the code.
2. **Virtual DOM**: React uses a **virtual DOM** (Document Object Model) that optimizes performance. Rather than updating the entire webpage when something changes, it only updates the part that needs to be changed.
3. **Declarative UI**: You can create **UI components declaratively**, meaning you tell React what you want, and it handles the changes for you.
4. **Ecosystem and Community**: React has a large community, so you have access to a wide range of **tools, libraries, and tutorials**.
5. **Learn Once, Write Anywhere**: React can be used for **web** and **mobile** development (via **React Native**), so the knowledge you gain is portable.

### Advantages of React JS

1. **Performance**: The virtual DOM and efficient diffing algorithms make React fast and responsive.
2. **Reusable Components**: React allows you to break down your UI into **modular, reusable components**, which speeds up development.
3. **SEO Friendly**: React can render on the server using **Server-Side Rendering (SSR)**, improving your website's **SEO** performance.
4. **Strong Community**: The large community provides many resources, including **libraries, support, and development tools**.
5. **Unidirectional Data Flow**: React has a **one-way data flow** that helps with debugging and maintaining state within applications.
6. **Rich Toolset**: Tools like **React Developer Tools**, **Redux**, and **React Router** make development faster and easier.

---

### Running JavaScript in HTML with React

To run React JS in HTML, you can load React through a **Content Delivery Network (CDN)**. A CDN is a server that hosts React libraries that you can easily include in your HTML file.

Here’s a basic setup for including React in an HTML file:

#### Example:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React JS Example</title>
    <!-- React and ReactDOM from CDN -->
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <!-- Babel for JSX support -->
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
  </head>
  <body>
    <div id="root"></div>

    <script type="text/babel">
      // React code will go here
    </script>
  </body>
</html>
```

### Creating Elements Using React JS

In React, instead of manually creating and inserting DOM elements, you can use React’s `React.createElement()` method to create elements.

#### Example of `React.createElement`:

```javascript
const element = React.createElement(
  "h1",
  { className: "greeting" },
  "Hello, World!"
);
```

This creates an `<h1>` element with the text "Hello, World!" and a class of "greeting".

### ReactDOM.render()

Once you’ve created an element with `React.createElement()`, you can render it to the DOM using `ReactDOM.render()`. This method is used to display your React element on the page.

#### Example:

```javascript
ReactDOM.render(element, document.getElementById("root"));
```

This renders the `element` into the `<div id="root"></div>` element.

---

### JSX

JSX (JavaScript XML) is a syntax extension for JavaScript that looks similar to HTML and is used to describe what the UI should look like in React. JSX allows you to write HTML elements directly in JavaScript.

#### Example of JSX:

```javascript
const element = <h1>Hello, World!</h1>;
```

This is much simpler than using `React.createElement()` and looks more like HTML, which developers are familiar with.

---

### Babel

**Babel** is a JavaScript compiler that converts JSX into plain JavaScript that browsers can understand. JSX code isn’t valid JavaScript, so it needs to be compiled into `React.createElement()` calls behind the scenes.

#### Example:

JSX:

```jsx
const element = <h1>Hello, World!</h1>;
```

Compiled JavaScript (by Babel):

```javascript
const element = React.createElement("h1", null, "Hello, World!");
```

### Embedding Variables and Expressions in JSX

You can embed JavaScript expressions inside JSX by wrapping them in curly braces `{}`. This is useful when you want to dynamically display variables or call functions inside JSX.

#### Example:

```javascript
const name = "John Doe";
const element = <h1>Hello, {name}!</h1>;
```

Here, `{name}` will be replaced by the value of the `name` variable, so the rendered output will be:

```html
<h1>Hello, John Doe!</h1>
```

You can also use expressions, like calling a function:

```javascript
const getGreeting = (name) => `Hello, ${name}`;
const element = <h1>{getGreeting("John")}</h1>;
```

### Nesting JSX Elements

JSX elements can be nested inside one another, just like HTML. If you have multiple elements, you need to wrap them in a parent element like a `<div>`, or use a **React Fragment** (`<>` and `</>`).

#### Example of Nesting:

```javascript
const element = (
  <div>
    <h1>Hello, World!</h1>
    <p>Welcome to React JS</p>
  </div>
);
```

This JSX represents a structure with an `<h1>` and a `<p>` tag nested inside a `<div>`.

#### Using React Fragment:

```javascript
const element = (
  <>
    <h1>Hello, World!</h1>
    <p>Welcome to React JS</p>
  </>
);
```

### Summary of Steps

1. **React CDN**: Use the CDN to include React in your HTML page.
2. **React.createElement()**: Create React elements using `React.createElement()`.
3. **ReactDOM.render()**: Render the created elements into the DOM using `ReactDOM.render()`.
4. **JSX**: Use JSX for a simpler and more intuitive way to create UI elements.
5. **Babel**: Use Babel to compile JSX into plain JavaScript.
6. **Embedding Variables**: Embed JavaScript variables and expressions in JSX.
7. **Nesting JSX**: You can nest JSX elements like you nest HTML elements.

Would you like to dive deeper into any specific part or have further examples?
