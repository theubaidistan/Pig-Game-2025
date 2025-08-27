# Pig Game – Vanilla JS

A fast, responsive remake of the classic **Pig Dice Game** built with **HTML, CSS, and JavaScript**. Roll the dice, build your round score, and **Hold** before you roll a **1**! First player to reach the target wins.

---

## 🔗 Live Demo

**Play here:** [https://pig-game-2025.vercel.app/](https://pig-game-2025.vercel.app/)

---

## 🎮 Game Rules (Quick)

- Game is for **2 players** (Player 1 starts).
- Click **Roll** to add the dice value to **Current** score.
- If you roll a **1**, your **Current** score is lost and the turn switches.
- Click **Hold** to add **Current** to your **Total** and pass the turn safely.
- First to reach the **Target Score** (default **100**) **wins**.
- **New Game** resets everything.

> Tip: The risk is real—roll again for a bigger haul or hold early to play safe.

---

## ✨ Features

- Clean, minimal UI with responsive layout (mobile/tablet/desktop).
- Visual dice roll and active player indicator.
- Target score can be configured in code.
- Zero dependencies; deploys easily on any static host.

---

## 🧱 Tech Stack

- **HTML5** for structure
- **CSS3** (Flexbox / media queries) for layout
- **Vanilla JavaScript (ES6+)** for game logic

---

## 📁 Project Structure

```text
pig-game-2025/
├─ index.html
├─ style.css
├─ script.js
├─ /assets
│   └─ dice-1.png ... dice-6.png (optional, if using images)
├─ pig-game-flowchart.png
└─ README.md (this file)
```

> Your actual structure may vary. Update this section if your files differ.

---

## 🚀 Getting Started (Local)

1. **Download or clone** the project.

   ```bash
   git clone <your-repo-url>
   cd pig-game-2025
   ```

2. **Open** `index.html` directly in your browser **or** run a tiny local server:

   ```bash
   # Python 3
   python -m http.server 5173
   # then open http://localhost:5173
   ```

---

## 🕹️ How to Play

- **Roll**: Generate a random 1–6. Adds to **Current** unless it’s **1**.
- **Hold**: Bank the **Current** into **Total**, switch turn.
- **New Game**: Reset scores and state.

Optional enhancements you may have:

- **Winning Screen** when a player reaches the target.
- **Target Score Input** (e.g., set to 50/100/150).
- **Keyboard Shortcuts** (e.g., `r`=Roll, `h`=Hold, `n`=New).

> If your build includes these features, keep this section. Otherwise, remove bullets you don’t use.

---

## 🧪 Core Logic (Concept)

```js
// Example: minimal round logic
const roll = () => {
  const die = Math.trunc(Math.random() * 6) + 1;
  if (die !== 1) {
    current += die; // keep risking!
  } else {
    current = 0; // bust
    switchPlayer();
  }
};
```

---

## 📱 Responsive Notes

- Layout adapts for phones and tablets using media queries.
- On small screens, action buttons remain visible and tappable.
- If you adjust breakpoints, test landscape vs portrait to avoid hidden controls.

---

## 🛠️ Configuration

Open `script.js` and tweak:

```js
const TARGET_SCORE = 100; // change to any number
```

If you use images for dice, ensure `/assets` paths match your HTML/CSS.

---

## 🪲 Troubleshooting

- **Buttons not visible on mobile**: Check z-index and flex-direction in mobile breakpoints.
- **Dice not updating**: Ensure you’re updating the `src`/`textContent` and calling `render()` after state changes.
- **State not resetting**: Verify all state variables are cleared in New Game handler.

---

## 🗺️ Roadmap (Ideas)

- Single‑player mode vs AI
- Sound effects & animations
- Custom themes / dark mode
- Persistent high scores (localStorage)

---

## 🤝 Contributing

PRs and suggestions welcome. If this is a personal project, remove this section.

---

## 📜 License

MIT — use, modify, and share freely. Replace with your preferred license if needed.

---

```md

```

## 📷 Screenshots & Flowchart

<p align="center">
  <img src="./pig-game-flowchart.png" alt="Pig Game Flowchart" width="600">
</p>

---

## 🙌 Acknowledgements

- Inspired by the classic Pig dice game often used in JS courses.
- Thanks to open web docs and MDN.

---

**Enjoy the game and may your rolls avoid the 1!**
