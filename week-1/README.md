# Week 1 – Node.js Crash Course  
**Day 1** | **Duration:** 3 hrs | **Live 1-on-1**

---

## LEARNING OBJECTIVES  
1. Install Node.js, npm, and set up VS Code with GitHub  
2. Run your first Node.js script and understand the difference from browser JS  
3. Use `npm` to manage packages and create `package.json`

---

## SLIDE DECK OUTLINE (Google Slides / Markdown)  
| Slide | Title | Content (bullet points) |
|-------|-------|-------------------------|
| 1 | Welcome to Backend! | • From HTML/CSS/JS → Server-side JS <br> • Why Node.js? (speed, full-stack JS) |
| 2 | Node.js Architecture | • Diagram: **Event Loop** + **Non-blocking I/O** <br> • Browser JS vs Node.js (no `window`, has `process`) |
| 3 | Install Node.js + npm | • Use **nvm** (macOS/Linux) or **Node.js installer** (Windows) <br> • Run: `node -v`, `npm -v` |
| 4 | VS Code Setup | • Extensions: **ESLint**, **Prettier**, **GitLens** <br> • Terminal: `code .` |
| 5 | First Script | • `index.js` → `console.log("Hello, Node!")` <br> • Run: `node index.js` |
| 6 | npm init & package.json | • `npm init -y` <br> • Explain: `name`, `version`, `main`, `scripts` |
| 7 | Mini-Exercise | • Build a **personalized greeting CLI** |
| 8 | Homework Preview | • CLI Calculator (add/subtract) with input validation |

*YouTube Video (free):*  
→ [Node.js Tutorial for Beginners – Dave Gray (Part 1)](https://www.youtube.com/watch?v=Oe421EPjeBE) – **watch 0:00–22:00**  
*(Covers installation, first script, npm, and `process.argv`)*

---

## LIVE-CODING SCRIPT (VS Code → GitHub)

```bash
# 1. Clone starter repo
git clone https://github.com/yourname/sofe-backend-week1-day1.git
cd sofe-backend-week1-day1
code .
```

```js
// index.js
console.log("Hello, Node.js from SOFE Backend!");
console.log("Runtime:", process.version);
console.log("Platform:", process.platform);

// Bonus: Greet user from CLI
const name = process.argv[2] || "Student";
console.log(`Welcome to Node.js, ${name}!`);
```

**Step-by-step narration (copy-paste into Zoom chat):**
```
1. Open index.js
2. Run: npm init -y
3. node index.js → see output
4. Explain process.argv: "How to pass name from CLI"
5. Break → student types same code + adds their name
6. git add . && git commit -m "Day 1: First Node script"
7. Push to GitHub → create PR
```

---

## MINI-EXERCISE (15 min in-session)

**Task:** Create `greet.js` that prints `"Hello, {name}!"` using `process.argv[2]`  
**Starter:** `exercises/greet.js`  
```js
// exercises/greet.js
const name = process.argv[2] || "Student";
console.log(`Hello, ${name}!`);
```

**Success criteria:**  
- [x] `node exercises/greet.js Alice` → `Hello, Alice!`  
- [x] No ESLint errors (`npx eslint .`)  
- [x] Passes `npm test` (Jest)

---

## HOMEWORK (due before Day 2)

| Deliverable | Format | Rubric |
|-------------|--------|--------|
| CLI Calculator (Add & Subtract) | GitHub PR | • Accepts 3 args: `num1`, `operator`, `num2` (40%) <br> • Validates input (30%) <br> • Jest tests pass (20%) <br> • README with usage (10%) |

**Repo link:** `https://github.com/studentname/sofe-project`  
**Branch:** `week1-day1`

---

## JEST TEST SNIPPET (auto-run with `npm test`)

```js
// tests/calculator.test.js
const { add, subtract } = require('../calculator');

test('adds 2 + 3 = 5', () => {
  expect(add(2, 3)).toBe(5);
});

test('subtracts 5 - 3 = 2', () => {
  expect(subtract(5, 3)).toBe(2);
});
```

*Run: `npm test` → all green*

---

## RESOURCES (100% FREE)
- **Docs:** [https://nodejs.org/en/docs](https://nodejs.org/en/docs)  
- **YouTube:** [Dave Gray – Node.js Full Course (Part 1)](https://www.youtube.com/watch?v=Oe421EPjeBE)  
- **Reading:** [Node.js Official Guide – Getting Started](https://nodejs.org/en/docs/guides/getting-started-guide)  
- **Cheat Sheet:** [Node.js Cheat Sheet – Devhints](https://devhints.io/nodejs)

---

## PROGRESS TRACKER (Notion / Google Sheet)
| Week | Day | Done? | Notes |
|------|-----|-------|-------|
| 1 | 1 | [ ] | First commit + PR merged |

*Share link with student → they tick when PR merged.*

---

**Session Flow (3 hrs):**  
- **0:00–0:05** – Warm-up: “What’s the difference between browser and server?”  
- **0:05–0:45** – Slides 1–4 (install + setup)  
- **0:45–1:30** – Live coding + student replication  
- **1:30–1:45** – Mini-exercise (greet.js)  
- **1:45–2:00** – Break  
- **2:00–2:45** – `npm`, `package.json`, GitHub PR demo  
- **2:45–3:00** – Homework walkthrough + Q&A

---
