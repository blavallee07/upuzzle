# MathForge — UWaterloo Math Puzzle Platform

A LeetCode-style platform for math and logic puzzles, built for University of Waterloo students. Featuring number theory, combinatorics, graph theory, linear algebra, and Jane Street-style monthly challenges with prizes.

---

## What is this?

MathForge is a competitive math puzzle platform where UWaterloo students can:

- Solve puzzles across multiple math categories (number theory, combinatorics, graph theory, linear algebra, and more)
- Submit answers to numerical, multiple choice, coding, and proof-based problems
- Compete in monthly Jane Street-style puzzle challenges with prizes
- Track progress and climb the leaderboard

Think LeetCode, but for math — built by a Waterloo student, for Waterloo students.

---

## Features

- Problem library — browseable by category and difficulty
- Multiple puzzle types — numerical, MCQ, coding, written proofs
- Monthly contest — Jane Street-style puzzle of the month
- Instant answer validation — with tolerance-based checking for numerical answers
- Code execution — submit Python/Java solutions directly in the browser (via Judge0)
- AI-assisted proof grading — written answers evaluated intelligently

---

## Tech Stack

| Layer | Tool |
|---|---|
| Frontend | Next.js + TypeScript |
| Styling | Tailwind CSS |
| Backend | Flask (Python) |
| Database | Supabase (Postgres) |
| Code Execution | Judge0 |
| Math Rendering | KaTeX |
| Hosting | Vercel + Railway |

---

## Project Structure

```
mathforge/
  backend/
    app.py              # Flask entry point
    problems/           # Problem definitions (JSON)
    routes/
      problems.py       # GET /problems, GET /problems/<id>
      submit.py         # POST /submit
  frontend/
    pages/
      index.tsx         # Problem list
      problems/[id].tsx # Problem detail + submission
    components/
      ProblemCard.tsx
      AnswerInput.tsx
```

---

## Getting Started

### Prerequisites

- Python 3.10+
- Node.js 18+
- Git

### Backend (Flask)

```bash
cd backend
pip install -r requirements.txt
python app.py
```

### Frontend (Next.js)

```bash
cd frontend
npm install
npm run dev
```

The app will be running at `http://localhost:3000`.

---

## Puzzle Types

**Numerical** — Answer is a number, checked within a tolerance (e.g. ±0.01%).

**Multiple Choice** — Exact match against one of the provided options.

**Coding** — Submit a Python/Java function, executed against hidden test cases via Judge0.

**Written / Proof** — Free-form answer, graded by AI with partial credit support.

---

## Roadmap

- [x] Problem schema design
- [x] Flask API (problems + submission)
- [ ] Frontend problem list page
- [ ] Answer submission + validation
- [ ] User accounts + solve history (Supabase)
- [ ] Leaderboard
- [ ] Monthly Jane Street-style contest system
- [ ] Prize distribution workflow

---

## Contributing

This project is open to contributions from UWaterloo students. If you want to add problems, fix bugs, or build new features, open a pull request or reach out directly.

Problem submissions should follow the format in `/backend/problems/example.json`.

---

## License

MIT
