# Hover Dropdown Menu Tutorial

This tutorial demonstrates how to create a stylish and interactive hover dropdown menu using HTML and CSS. The menu will display a submenu when hovering over the main menu items.

## Table of Contents

- [Preview](#preview)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Customization](#customization)
- [HTML Structure](#html-structure)
- [CSS Styles](#css-styles)
- [Conclusion](#conclusion)

## Preview

![Dropdown Menu Preview](/path/to/your/preview/image.png)

## Prerequisites 
- Basic understanding of HTML and CSS.
- Code editor (e.g., Visual Studio Code).

## Usage 

1. Clone or download this repository.
2. Open `index.html` in a web browser to see the dropdown menu in action.

## Customization 

You can easily customize the dropdown menu to match your website's design and style.

### HTML Structure 

The dropdown menu is structured using nested `<div>` elements within a `<nav>` element. Each menu item has a sub-menu that appears on hover.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hover Drop Down Menu Tutorial</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <nav>
      <div class="menu-item">
        <div class="menu-name"><p>My projects</p></div>
        <div class="menu-links">
          <a href="https://yelose.dev"><p>My Portfolio</p></a>
          <a href="https://mummys-littlethings.web.app/"><p>Mummy's Little Things</p></a>
          <a href="https://coloritos-enriquin.web.app/"><p>Painter in Madrid</p></a>
        </div>
      </div>
      <!-- Add more menu items here -->
    </nav>
  </header>
</body>
</html>
```

### CSS Styles

The CSS file (`style.css`) provides styling for the dropdown menu, including transitions and hover effects.

```css
/* RESET */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* BASIC CSS */
header > nav {
  display: flex;
  background-color: gray;
  gap: 40px;
  cursor: pointer;
}

p {
  padding: 10px;
}
.menu-links p,
.menu-links a {
  text-decoration: none;
  color: black;
}
.menu-links a:hover,
.menu-links a:hover p {
  background-color: rgba(128, 128, 128, 0.09);
}

.menu-item {
  position: relative;
  padding: 10px;
}
.menu-links {
  background-color: beige;
  position: absolute;
  top: 50px;
  overflow: hidden;
  max-height: 0;
  opacity: 0;
  z-index: 100;
  transition: max-height 2s ease-out, opacity 0.4s ease-out;
}

/* HOVER DROPDOWN EFFECT */
.menu-item:hover .menu-links {
  opacity: 1;
  animation: showMenu 2s forwards;
}

@keyframes showMenu {
  0% {
    max-height: 0;
  }
  100% {
    max-height: 50vh;
  }
}
```

## Conclusion 

By following this tutorial, you've created a responsive and stylish dropdown menu with hover effects. Feel free to experiment and customize the styles to fit your website's design.

For a live example, you can visit [Demo](https://coleccion-legado-de-amor.web.app).

Happy coding!

