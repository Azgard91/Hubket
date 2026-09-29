# AGENTS.md

## Project overview
This repository contains a small web app for tracking TIC incidents. It is built with plain HTML, CSS, and JavaScript and runs entirely in the browser without a build step or backend.

## Core behavior
- Manage incident records with title, description, priority, responsible person, status, creation timestamp, and resolution timestamp.
- Supported states: Abierto, En progreso, Resuelto, Cerrado.
- Supported priorities: Baja, Media, Alta, Crítica.
- Supported responsible users: Juan, Matías, Dalmiro.
- Persist data in browser localStorage using the key `incidentes`.
- Show summary cards for incident counts by status and a calculated average resolution time.
- Allow filtering by status, priority, and responsible user.

## Important files
- `index.html`: page structure and form/filter layout.
- `styles.css`: visual design and priority/status coloring.
- `app.js`: core logic for rendering, filters, localStorage persistence, status changes, and time calculations.
- `README.md`: user-facing project documentation.

## Working rules for future agents
- Keep the app dependency-free and static: no frameworks, bundlers, or package install steps.
- Prefer small DOM-based updates and maintain compatibility with the existing vanilla JavaScript style.
- When adding new incident fields, ensure they are safely initialized and saved to localStorage.
- Preserve the current behavior of time tracking:
  - if an incident is open, show elapsed time since creation;
  - if it is resolved or closed, keep the resolution timestamp and compute duration from creation to resolution;
  - if the incident is reopened, reset the resolution state cleanly.
- When changing the data model, keep backward compatibility with previously stored entries in localStorage.
- Keep the UI simple, accessible, and fully functional without a server.

## Validation
To validate changes:
1. Open `index.html` in a browser.
2. Create, update, and filter incidents.
3. Confirm the summary and time calculations still match the expected behavior.

## Preferred contribution style
- Make surgical, targeted updates.
- Keep code readable and consistent with the existing naming pattern (`ESTADOS`, `PRIORIDADES`, `RESPONSABLES`, `mostrar`, `guardar`).
- Favor explicit, simple logic over abstraction unless it significantly improves clarity.
