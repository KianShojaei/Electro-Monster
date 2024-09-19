# Electro-Monster
𝑨𝒏 𝒆𝒍𝒆𝒄𝒕𝒓𝒊𝒄 𝒎𝒐𝒏𝒔𝒕𝒆𝒓 𝒘𝒉𝒊𝒄𝒉 𝒇𝒐𝒍𝒍𝒐𝒘𝒔 𝒕𝒉𝒆 𝒎𝒐𝒗𝒆𝒎𝒆𝒏𝒕𝒔 𝒐𝒇 𝒕𝒉𝒆 𝒎𝒐𝒖𝒔𝒆 𝒐𝒏 𝒕𝒉𝒆 𝒔𝒄𝒓𝒆𝒆𝒏





# Electric Monster - Mouse Follower


This project is a fun interactive animation where an electric monster follows the movements of your mouse on the screen. It utilizes HTML5 Canvas, CSS, and JavaScript to create a visually appealing experience.

## Demo Video

![Demo Video](./assets/demo-video.gif)

## Features
- An electric monster that reacts to mouse movements.
- Dynamic tentacle animations with colorful effects.
- Fully responsive design that adapts to screen size.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Code Overview](#code-overview)
    - CSS Styles
    - HTML Structure
    - JavaScript Logic
4. [License](#license)

---

## Installation

To get started with the project, clone the repository:

```bash
git clone https://github.com/KianShojaei/Electro-Monster.git
cd electric-monster
```

Open `index.html` in your preferred web browser to see the project in action.

---

## Usage

Simply move your mouse around the screen to see the electric monster follow your cursor. The animation will adjust dynamically based on your mouse's position.

### Controls:
- **Mouse Movement**: Move the mouse to control the monster.
- **Mouse Leave**: The monster returns to a default behavior when the mouse leaves the canvas.

---

## Code Overview

### CSS Styles

The CSS file (`style.css`) styles the canvas and the background, creating a dark environment that enhances the visual effects.

```css
body,
html {
  margin: 0px;
  padding: 0px;
  position: fixed;
  background: black;
}
```

### HTML Structure

The HTML file (`index.html`) sets up the canvas where the monster will be drawn. It includes links to the CSS and JavaScript files.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Monster Electro</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <canvas id="canvas"></canvas>
    <script src="index.js"></script>
</body>
</html>
```

### JavaScript Logic

The main functionality of the project is implemented in the JavaScript file (`index.js`). Here’s a breakdown of the key components:

1. **Initialization**: Sets up the canvas and context.

```javascript
function init(elemid) {
  let canvas = document.getElementById(elemid),
      c = canvas.getContext("2d"),
      w = (canvas.width = window.innerWidth),
      h = (canvas.height = window.innerHeight);
  c.fillStyle = "rgba(30,30,30,1)";
  c.fillRect(0, 0, w, h);
  return { c: c, canvas: canvas };
}
```

2. **Tentacle Class**: Represents the monster's tentacles, updating their position based on mouse movement.

```javascript
class tentacle {
  constructor(x, y, l, n, a) {
    // Initialization logic
  }
  move(last_target, target) {
    // Update position based on target
  }
  show(target) {
    // Render the tentacle
  }
}
```

3. **Animation Loop**: The draw function handles the rendering of the tentacle animations in response to mouse movements.

```javascript
function draw() {
  c.fillStyle = "rgba(0, 0, 0, 1)";
  c.fillRect(0, 0, w, h);
  // Additional rendering logic
}
```

4. **Event Listeners**: Capture mouse movements and update the target position accordingly.

```javascript
canvas.addEventListener("mousemove", function (e) {
  mouse.x = e.pageX - this.offsetLeft;
  mouse.y = e.pageY - this.offsetTop;
});
```

5. **Responsive Design**: The canvas resizes with the browser window.

```javascript
window.addEventListener("resize", function () {
  (w = canvas.width = window.innerWidth),
  (h = canvas.height = window.innerHeight);
  loop();
});
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Kian

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
