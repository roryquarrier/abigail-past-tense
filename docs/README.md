# Site build

GitHub Pages serves this folder (Settings → Pages → `main` / `/docs`).

- `index.html` · `styles.css` (past-tense gold-on-navy theme) · `app.js` (nav, search, quiz, progress)
- `timer.js` — the **25-minute pace timer** (five 5-minute units; edit `STEPS` in `timer.js`)
- `assets/` — the 6 illustrations
- `content.js` — **generated** by `build.py` from `../course/*.md` + `../course/quizzes.json`

```bash
cd docs && python3 build.py     # needs the markdown package
```

## Units covered

Unit 10 was/were · Unit 11 past simple · **Unit 12 negatives & questions (extra
depth: dedicated step, cheat-sheet page, 8-question quiz)** · Unit 13 past
continuous · Unit 14 past continuous + past simple.

Source of the unit list: `../assets/units-extract.txt` (OCR of the contents page
supplied 2026-11-17).

## Progress store

`localStorage` key `abigail-past.progress.v2` — validated and normalised on import.

## Audit test

```bash
node tests/progress-audit.mjs                                    # live site
node tests/progress-audit.mjs http://127.0.0.1:8977/index.html   # local
```
