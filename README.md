# ExamCoach 🎓

A personal AI exam study agent powered by [Agency](https://aka.ms/agency). ExamCoach teaches Microsoft certification content from MS Learn modules conversationally, runs mock tests, and tracks your progress locally.

---

## Features

- 📖 **Study Mode** — Learn module by module with conversational teaching, then take a 10-question mock test per module
- 🏋️ **Practice Mode** — Skip teaching and jump straight to a full 60-question mock exam
- 🔁 **Unlimited retakes** — Retake any module test or the full mock exam; best score is always preserved
- 💾 **Progress tracking** — Saves your position, scores, and weak areas to `~/.copilot/examcoach-progress.json`
- ⏸️ **Quit & resume** — Stop at any point (mid-module, mid-test) and pick up exactly where you left off
- 🌐 **Any MS exam** — Works with any exam that has an MS Learn learning path

---

## How to Run

```bash
cd "path/to/ExamCoach"
agency copilot --agent ExamCoach --source repo
```

On first run, ExamCoach will ask which exam you want to study for.  
On subsequent runs, it will detect your saved progress and offer to continue.

---

## Supported Exams

| Exam | Title |
|------|-------|
| AB-730 | AI Business Professional — Transform business workflows with generative AI |

> To add any other exam, just provide the exam code and its MS Learn learning path URL when prompted.

---

## Progress File

Progress is saved locally at:

```
~/.copilot/examcoach-progress.json
```

This file is **personal and not stored in the repo**. It tracks:
- Current module and position within a module
- Test attempts and best scores per module
- Weak areas identified from incorrect answers
- Full mock exam attempts and best score

---

## Requirements

- [Agency CLI](https://aka.ms/agency) installed
- `msft-learn` MCP configured in your Agency environment
