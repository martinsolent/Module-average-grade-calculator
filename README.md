# Module Grade Calculator

A simple single-page web app that helps you calculate your overall **module mark** from individual assessment grades and their weightings.

The UI and logic are contained entirely in [`index.html`](index.html) (HTML + CSS + vanilla JavaScript).

## Features

- **2 or 3 assessments**: switch between modes (e.g. Coursework/Practical or Coursework/Practical/Final Exam).
- **Module name field**: label your calculation and show it in the results card.
- **Automatic weighting check**: shows the total weighting and highlights it until it equals **100%**.
- **Input validation**:
  - Weightings must add up to **100%**.
  - Grades must be between **0 and 100**.
- **Weighted average calculation**: calculates a final score (rounded to 1 decimal place).
- **UK-style grade banding** (based on the calculated score):
  - **A (First Class)**: 70+
  - **B (Upper Second / 2:1)**: 60–69.9
  - **C (Lower Second / 2:2)**: 50–59.9
  - **D (Third Class)**: 40–49.9
  - **F (Fail)**: < 40
- **Results breakdown**: shows each assessment’s contribution to the final score.
- **Light/Dark theme toggle**.

## How it works

1. Enter (or keep) the assessment names.
2. Enter the **weight (%)** for each assessment so the total equals **100%**.
3. Enter the **grade (%)** for each assessment.
4. Click **Calculate Module Grade**.

The app computes:

\[
\text{Module Score} = \sum (\text{grade}_i \times \text{weight}_i / 100)
\]

It then maps the score to a letter grade + label using the thresholds in the `GRADES` array inside `index.html`.

## Run locally

No build step is required.

- Download / clone the repository
- Open `index.html` in your browser

## Project structure

- `index.html` — the entire app (layout, styling, and logic)
- `README.md` — project documentation
