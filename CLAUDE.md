# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Single-file vanilla HTML/CSS/JS task manager app ("Mi Lista de Tareas"). No build tools, no dependencies, no package manager. Open `index.html` directly in any modern browser.

## Running the app

```bash
open index.html        # macOS: opens in default browser
python3 -m http.server # optional: serve via local HTTP server on :8000
```

## Architecture

Everything lives in `index.html`:

| Section | Lines | Description |
|---|---|---|
| `<style>` | 7–164 | All CSS — Flexbox layouts, green (#2d6a4f) color scheme |
| `<body>` | 166–204 | HTML structure: header, form input, task list (`<ul id="task-list">`), stats panel |
| `<script>` | 205–253 | Four functions: `addTask`, `toggleDone`, `deleteTask`, `updateStats` |

## Known intentional bugs (educational exercise)

The file has three bugs marked with comments:

| # | Location | Bug | Fix |
|---|---|---|---|
| 1 | CSS `header` (line 20–30) | Nav links stack vertically instead of flowing in a row | `nav` needs `display: flex` or `header` needs `justify-content: space-between` |
| 2 | `addTask()` (line 209) | `getElementById('task-inputs')` — ID doesn't exist in the DOM | Change to `'task-input'` |
| 3 | `updateStats()` (line 242) | `pending = done - total` produces negative numbers | Change to `total - done` |
