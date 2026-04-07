# TOEFL iBT 2026 — Practice Hub

An interactive, browser-based practice tool for the new **TOEFL iBT 2026** format (effective January 21, 2026). Two practice sections covering Speaking and Writing, all running locally in your browser with no sign-up required.

**Live App:** [https://hkcc375.github.io/TOEFL-iBT-Practice/](https://hkcc375.github.io/TOEFL-iBT-Practice/)

## Practice Sections

### Listen & Repeat (Speaking)

Mirrors the new TOEFL iBT 2026 **Listen & Repeat** task. You hear a sentence and must repeat it exactly — scored on accuracy, pronunciation, and fluency.

- **36 campus/daily-life scenarios** with 7 sentences each (252 total)
- **Progressive difficulty:** 2 short (8s), 3 medium (10s), 2 long (12s) — matching the real exam
- **No preparation time** — recording starts automatically 1 second after the prompt, just like the real test
- **Live speech transcription** via Web Speech API
- **AI-powered evaluation** on a 0–5 scale across 3 rubric dimensions:
  - Repeat Accuracy (word-level edit distance)
  - Pronunciation / Intelligibility (character-level similarity)
  - Fluency & Rhythm (length ratio + word order preservation)
- **End-of-scenario report** with overall scores, sentence-by-sentence word diffs, and improvement tips

### Build a Sentence (Writing)

Practice the **Build a Sentence** (Complete a Sentence) task from the TOEFL iBT Writing section.

- **411 conversational questions** — all capped at 14 words, covering campus and daily-life topics
- **6-minute countdown timer** — practice under timed pressure; auto-stops when time runs out
- **Drag-and-drop or click** — drag words into the answer zone or click to move them
- **Auto-advance on correct answers**
- **Cross-session deduplication** — tracks questions via localStorage; resets when the pool is exhausted
- **Detailed practice report** — accuracy, average time per question, per-question breakdown

## How to Use

### Option 1: Live Website (recommended)
Visit [https://hkcc375.github.io/TOEFL-iBT-Practice/](https://hkcc375.github.io/TOEFL-iBT-Practice/) — works on any device with a modern browser.

### Option 2: Open Locally
```bash
open index.html
```

### Option 3: Serve via localhost
```bash
cd TOEFL-iBT-Practice
python3 -m http.server 8080
# then visit http://localhost:8080
```

## File Structure

```
index.html              — Landing page / section selector
listen-and-repeat.html  — Listen & Repeat speaking practice
build-a-sentence.html   — Build a Sentence writing practice
```

## Tech Stack

- **Single HTML files** — zero dependencies, no build step, no framework
- **Vanilla JavaScript** — Web Speech API, MediaRecorder, drag-and-drop
- **localStorage** — for cross-session question deduplication
- **Works best in Chrome/Edge** — for full speech recognition support

## License

This project is for personal TOEFL practice. Feel free to fork and add your own sections.
