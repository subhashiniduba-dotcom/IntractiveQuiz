# IntractiveQuiz[README.md](https://github.com/user-attachments/files/26165358/README.md)
# Interactive Quiz App

A dynamic, client-side quiz platform built with vanilla JavaScript, HTML5, and CSS3.

## Features

- **3 Topics** — JavaScript, Web Development, General Tech
- **3 Difficulty levels** — Easy, Medium, Hard (25 unique questions each)
- **Countdown timer** — 25s / 20s / 15s based on difficulty
- **Instant feedback** — correct/wrong highlighting with explanations
- **Score tracking** — live score, streak counter, best streak
- **Client-side validation** — prevents re-answering, handles time-outs
- **Answer review** — full breakdown of every question after quiz
- **Keyboard support** — press 1–4 or A–D to answer, Enter for next
- **Fully responsive** — works on mobile, tablet, and desktop
- **No dependencies** — pure HTML, CSS, JavaScript

## Project Structure

```
InteractiveQuizApp/
├── index.html          # Main HTML entry point
├── css/
│   ├── style.css       # All component styles + responsive design
│   └── animations.css  # Transitions, keyframes, micro-interactions
├── js/
│   ├── questions.js    # All quiz questions (63 total)
│   ├── quiz.js         # Quiz engine — state, scoring, timer, validation
│   ├── ui.js           # DOM rendering — all UI update functions
│   └── app.js          # Main controller — event wiring + quiz flow
└── README.md
```

## Architecture

The project follows a clean separation of concerns:

| File | Responsibility |
|---|---|
| `questions.js` | Pure data — no logic |
| `quiz.js` | Business logic — state machine, scoring, timer |
| `ui.js` | DOM manipulation — renders state to the screen |
| `app.js` | Controller — connects quiz engine to UI and handles events |

## How to Run

Just open `index.html` in any modern browser — no build step, no server needed.

```bash
# Option 1: open directly
open index.html

# Option 2: serve locally
npx serve .
# or
python3 -m http.server 3000
```

## Adding Questions

Open `js/questions.js` and add to any topic/difficulty array:

```js
{
  q: "Your question text here?",
  opts: ["Option A", "Option B", "Option C", "Option D"],
  ans: 0,          // index of correct option (0-based)
  exp: "Explanation shown after the user answers."
}
```

## Tech Stack

- HTML5 (semantic markup)
- CSS3 (custom properties, flexbox, grid, keyframe animations)
- JavaScript ES6+ (modules pattern, arrow functions, destructuring)
- Google Fonts (Syne + DM Sans)

## Screenshots

| Start Screen | Quiz | Results |
|---|---|---|
| Topic + difficulty selection | Timed question with options | Score breakdown + review |

## License

MIT — free to use and modify.
