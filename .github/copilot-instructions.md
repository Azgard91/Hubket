# Copilot instructions for this repository

This project is a static incident management app for TIC tickets. It uses plain HTML, CSS, and JavaScript only.

## Goals
- Keep the app running directly from the browser without a backend or install step.
- Maintain simple and readable vanilla JavaScript.
- Preserve localStorage-based persistence and time tracking behavior.

## File responsibilities
- `index.html`: overall layout, form controls, filters, and table structure.
- `styles.css`: layout, color coding, and status/priority visual states.
- `app.js`: incident lifecycle, localStorage logic, summary calculations, and event handling.

## Constraints
- Do not introduce frameworks, build tools, or dependencies.
- Keep changes compatible with existing stored incident data.
- Maintain the state logic for open/resolved/closed incidents and the summary metrics.

## Validation
Open `index.html` in a browser and manually verify that the main flows still work: create incident, edit status, filter records, and check summary/time calculations.
