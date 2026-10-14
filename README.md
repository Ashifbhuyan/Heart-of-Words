# Heart of Words (heart-of-words) ❤️✨

An elegant, pure HTML5 Canvas typographic heart animation written entirely in Vanilla JavaScript. The heart shape is generated through parametric mathematical curves, drawing a clean outline first and then cascading love words row-by-row from top to bottom.

Developed by **@saklin_01 ([@saklincodes](https://github.com/saklincodes))**.

---

## 🌟 Key Highlights

- **Pure Mathematical Heart Curve**: Uses the classical parametric cardioid formula:
  $$x(t) = 16 \sin^3(t)$$
  $$y(t) = -(13 \cos(t) - 5 \cos(2t) - 2 \cos(3t) - \cos(4t))$$
- **Two-Phase Sequential Animation**:
  1. **Phase 1 (Border Tracing)**: Traces the outer perimeter sequentially word-by-word around the heart curve from the top center.
  2. **Phase 2 (Top-to-Bottom Cascade)**: Once the outline closes, the interior fills gracefully row-by-row from the top lobes down to the bottom tip.
- **Strictly Horizontal & Clean Typography**: Every single *"I Love You"* text sits horizontally without distracting rotations, ensuring 100% legibility.
- **Collision-Free Spacing**: Uses structured brick offsets ($72\text{px}$ horizontal, $25\text{px}$ line height) to prevent cluttered overlaps.
- **Perfect Geometric Centering**: Corrects the parametric centroid offset ($2.5 \times \text{scale}$) so the heart sits evenly between all four viewport edges.
- **Zero Dependencies**: Pure HTML5, CSS3, and Vanilla JavaScript. No libraries, no build tools, no Node.js required.

---

## 📁 Project Structure

```text
heart-of-words/
├── index.html     # Minimalist entry point & dual canvas layers
├── style.css      # Dark romantic backdrop & responsive canvas layout
├── script.js      # Core parametric math, particle system & animation loop
└── README.md      # Documentation & developer notes
```

---

## 🚀 Getting Started

Simply open `index.html` in any modern web browser:

1. Clone or download this repository.
2. Double-click **`index.html`** (or open with Chrome, Edge, Firefox, Brave, Safari).
3. Click anywhere on the screen at any time to re-trigger the bloom animation.

---

## ⚙️ Customization Guide

You can easily customize the animation parameters in [`script.js`](script.js):

### 1. Change the Message
Update the `MESSAGE` constant:
```javascript
const MESSAGE = 'I Love You'; // Change to custom name, e.g., 'I Love You Priya'
```

### 2. Adjust Colors & Palette
Modify the `SHADES` array to your preferred color theme:
```javascript
const SHADES = ['#ff1758', '#ff2a6d', '#ff5285', '#ff789e', '#ffa8c0', '#ffd6e3', '#ffffff'];
```

### 3. Adjust Pacing & Speed
Control the animation speed inside `initHeartParticles()`:
```javascript
const outlineDelayStep = 110; // ms per word along the outline (higher = slower)
const delay = outlineEndTime + normalizedY * 4200; // total duration of interior cascade
```

---

## 👨‍💻 Author

Crafted with ❤️ by **@saklin_01 ([@saklincodes](https://github.com/saklincodes))**.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and share!
