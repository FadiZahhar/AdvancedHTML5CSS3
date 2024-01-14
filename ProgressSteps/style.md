```
@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');

:root {
  --line-border-fill: #3498db;
  --line-border-empty: #383838;

}

* {
  box-sizing: border-box;
}

body {
  background-color: #1f1f1f;
  font-family: 'Muli', sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  overflow: hidden;
  margin: 0;
}

.container {
  text-align: center;
}

.progress-container {
  display: flex;
  justify-content: space-between;
  position: relative;
  margin-bottom: 30px;
  max-width: 100%;
  width: 350px;
}

.progress-container::before {
  content: '';
  background-color: var(--line-border-empty);
  position: absolute;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  height: 4px;
  width: 100%;
  z-index: -1;
}

.progress {
  background-color: var(--line-border-fill);
  position: absolute;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  height: 4px;
  width: 0%;
  z-index: -1;
  transition: 0.4s ease;
}

.circle {
  background-color: #1f1f1f;
  color:#e2e2e2;
  border-radius: 50%;
  height: 30px;
  width: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 3px solid var(--line-border-empty);
  transition: 0.4s ease;
}

.circle.active {
  border-color: var(--line-border-fill);
}

.btn {
  background-color: var(--line-border-fill);
  color: #fff;
  border: 0;
  border-radius: 6px;
  cursor: pointer;
  font-family: inherit;
  padding: 8px 30px;
  margin: 5px;
  font-size: 14px;
}

.btn:active {
  transform: scale(0.98);
}

.btn:focus {
  outline: 0;
}

.btn:disabled {
  background-color: var(--line-border-empty);
  cursor: not-allowed;
}
```css

This CSS code is designed to style the "Progress Steps" HTML structure you shared earlier. It uses modern CSS practices, including CSS variables and Flexbox. Let's break down the key parts:

1. **Google Font Import:**
   - `@import url('https://fonts.googleapis.com/css?family=Muli&display=swap');`: Imports the "Muli" font from Google Fonts.

2. **CSS Root Variables:**
   - `:root { ... }`: Defines two CSS variables (`--line-border-fill` and `--line-border-empty`) for colors, making it easy to maintain and change the color scheme.
   - `--line-border-fill`: Color for the completed steps and the progress line.
   - `--line-border-empty`: Color for the incomplete steps and the base line.

3. **Universal Box Sizing:**
   - `* { box-sizing: border-box; }`: Ensures that padding and border widths are included in the total width and height of elements.

4. **Body Styling:**
   - Sets background color, font family, and uses Flexbox to center the content (`display: flex`, `align-items: center`, `justify-content: center`).
   - `height: 100vh` and `overflow: hidden` make the body take up the full viewport height and hide any overflow.

5. **Container Styling:**
   - `.container { text-align: center; }`: Aligns the content of the container to the center.

6. **Progress Container Styling:**
   - Uses Flexbox for layout and spaces items evenly.
   - The `::before` pseudo-element creates a line behind the circles, representing the path of the progress steps.

7. **Progress Bar Styling:**
   - `.progress`: Styles the progress bar which visualizes the progress between steps.
   - Initially, its width is `0%`, and it expands as the steps progress.
   - Uses a transition for smooth width change.

8. **Circle Styling:**
   - Styles the circles representing each step.
   - Uses Flexbox for centering content inside the circles.
   - The `active` class changes the border color to indicate the current or completed step.

9. **Button Styling:**
   - Styles for the "Prev" and "Next" buttons.
   - `:active` and `:focus` pseudo-classes are used for interactive styles.
   - Disabled state (`:disabled`) changes the button's appearance to indicate it's not clickable.

In summary, this CSS code styles the progress steps, creating a visual representation of a multi-step process. It includes interactive styles for the buttons and dynamic changes for the progress bar and active steps, providing a clear and engaging user interface. The use of CSS variables enhances maintainability, and Flexbox ensures a flexible layout.