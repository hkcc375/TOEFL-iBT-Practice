# TOEFL iBT — Build a Sentence Practice

An interactive, browser-based practice tool for the **Build a Sentence** (Complete a Sentence) task from the TOEFL iBT Writing section. Drag and drop jumbled words to form grammatically correct conversational responses — all under a timed countdown.

**Live App:** [https://hkcc375.github.io/TOEFL-iBT-Practice/](https://hkcc375.github.io/TOEFL-iBT-Practice/)

## Features

- **411 conversational questions** — all capped at 14 words, covering everyday campus and daily-life topics
- **6-minute countdown timer** — practice under timed pressure; the test auto-stops when time runs out
- **Drag-and-drop or click** — drag words into the answer zone and reorder them, or simply click to move words between the word bank and answer bar
- **Auto-advance on correct answers** — no need to click "Next" when you get it right
- **Cross-session deduplication** — tracks which questions you've already seen (via localStorage) and always serves fresh ones first; resets automatically once the entire pool is exhausted
- **Detailed practice report** — shown when time expires, including:
  - Total questions attempted and accuracy percentage
  - Average time per question
  - Per-question breakdown with your answer, the correct answer, and time spent

## How to Use

### Option 1: Live Website (recommended)
Visit [https://hkcc375.github.io/TOEFL-iBT-Practice/](https://hkcc375.github.io/TOEFL-iBT-Practice/) — works on any device with a modern browser.

### Option 2: Open Locally
Download `index.html` and open it directly in your browser:
```bash
open index.html
```

### Option 3: Serve via localhost
```bash
cd TOEFL-iBT-Practice
python3 -m http.server 8080
# then visit http://localhost:8080
```

## How It Works

1. A **Person 1** prompt is displayed (a conversational question).
2. **Person 2's response** is shown as jumbled words in the **Word Bank**.
3. Drag (or click) the words into the **Your Answer** zone in the correct order.
4. Click **Submit** to check your answer.
   - Correct answers auto-advance after a brief flash.
   - Wrong answers show the correct sentence; click **Next** to continue.
5. When the 6-minute timer hits zero, the session ends and a **Practice Report** is generated.

## Tech Stack

- **Single HTML file** — zero dependencies, no build step, no framework
- **Vanilla JavaScript** — drag-and-drop API with click fallback
- **localStorage** — for cross-session question deduplication
- **CSS animations** — timer pulses red in the final 30 seconds

## License

This project is for personal TOEFL practice. Feel free to fork and add your own questions.
