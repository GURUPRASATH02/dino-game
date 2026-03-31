# 🦖 Dino Runner Game – Simple Jump & Run

A classic **endless runner** inspired by the Chrome Dino Game.  
Control a little dinosaur, jump over cacti, and survive as long as you can.  
Built with **plain HTML, CSS, and JavaScript** – perfect for beginners who want to learn game development basics.

![Game Screenshot](screenshot.png)  
*(Add a screenshot of your game here)*

## 🎮 Play Online
👉 **[Live Demo on GitHub Pages](https://your-username.github.io/your-repo-name/)**  
*(Replace with your actual GitHub Pages URL after deployment)*

---

## ✨ Features

- **Simple one‑button gameplay** – press `Space`, `ArrowUp`, or click/tap the canvas to jump.
- **Progressive difficulty** – speed and spawn rate increase as your score grows.
- **Score system** – earn points the longer you survive.
- **Restart functionality** – press `R` or click the RESTART button.
- **Mobile friendly** – tap the canvas to jump.
- **Smooth animations** – clouds, ground details, and cactus obstacles.

---

## 🕹️ How to Play

1. Open the game in your browser.
2. **Jump** over the green cacti.
3. Avoid collision – if you hit a cactus, it's **Game Over**.
4. Press **RESTART** or hit the **R** key to start again.
5. Your score increases automatically over time. The longer you survive, the faster the game becomes!

---

## 🛠️ Technologies Used

- **HTML5** – page structure and canvas element.
- **CSS3** – styling, layout (Flexbox), and responsive design.
- **JavaScript (ES6)** – game loop, physics, collision detection, and DOM manipulation.

No external libraries – 100% vanilla code.

---

## 📁 File Structure
dino-game/
├── index.html # Main HTML file (includes CSS & JS)
├── README.md # This file
└── screenshot.png # Optional: preview image for your repo


> **Note:** The entire game is contained in a single `index.html` file. You can copy the code from below and paste it into your own `index.html`.

---

## 💻 Local Development

Follow these steps to run the game on your own computer:

1. **Clone or download** this repository.
2. **Open the folder** in your code editor (VS Code, Sublime, etc.).
3. **Launch the game** by opening `index.html` in any modern web browser (Chrome, Firefox, Edge).
   - Or use a local development server (e.g., with VS Code Live Server extension).

That's it – no build steps, no dependencies!

---

## 🚀 Deploy to GitHub Pages

Host your game online for free using **GitHub Pages**:

1. **Create a GitHub repository** (public).
2. **Upload your files** – at least `index.html` and optionally `README.md` and a screenshot.
3. Go to your repository **Settings** → **Pages** (left sidebar).
4. Under **Branch**, select `main` (or `master`) and the `/ (root)` folder.
5. Click **Save**.
6. After a minute, your game will be live at:  
   `https://<your-username>.github.io/<repository-name>/`

> 💡 **Tip:** Rename your main file to `index.html` – GitHub Pages automatically serves it as the entry point.

---

## 🎛️ Customization – Adjust Game Speed & Difficulty

You can easily make the game easier or harder by changing a few numbers inside the JavaScript.

### 1. Obstacle Movement Speed
Find this part in the `updateGame()` function (inside `<script>`):
```javascript
obstacles[i].x -= 5;   // ← change this number

2. Score‑Based Speed Boost
The game gets faster when your score exceeds 400 and 800. Remove or change these lines:

javascript
if (score > 800) obstacles[i].x -= 1.2;
else if (score > 400) obstacles[i].x -= 0.8;
Delete them to keep constant speed.

Or reduce the extra values (e.g., 0.5 instead of 1.2).

3. Obstacle Spawn Delay
Look for:

javascript
let dynamicSpawnDelay = Math.max(35, baseSpawnDelay - Math.floor(score / 400));
Increase baseSpawnDelay (currently 80 at the top of the script) to make cacti appear less often.

Increase the minimum delay (Math.max(50, ...)) to prevent very fast spawning.

4. Jump Power / Gravity
Adjust these constants near the top:

javascript
const GRAVITY = 0.8;      // lower = floatier jump
const JUMP_POWER = -11;    // more negative = higher jump

---

### How to Use This

1. **Create a new repository** on GitHub (name it e.g., `dino-game`).
2. **Copy the full code** from the `index.html` section above into a file named `index.html`.
3. **Add this README.md** (the content I just provided) to the same repository.
4. **Push both files** to GitHub.
5. **Enable GitHub Pages** in your repository settings (Branch: `main`, folder: `/root`).
6. Your game will be live at `https://your-username.github.io/dino-runner-game/`.

Enjoy your game! 🦖
