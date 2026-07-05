# Project 2: Character Counter

A textarea with a live character counter capped at 200 characters, built with plain HTML, CSS, and JavaScript.

## Features
- Displays "200 characters max" up front
- Counter updates on every keystroke: `"used/200 characters"`
- Turns amber when 20 or fewer characters remain
- Turns red and shows a warning once the limit is hit
- Typing (and pasting) is hard-blocked past 200 characters

## How it works
- A single `input` event listener recalculates `used` and `remaining` on every change
- If pasted text pushes the value over 200 characters, it's trimmed back down with `textarea.value.slice(0, MAX_CHARS)`
- `MAX_CHARS` (200) and `CLOSE_THRESHOLD` (20) are set as constants at the top of the script, so limits can be adjusted in one place

## Running the project
No build step or dependencies needed. Just open `character-counter.html` directly in a browser.

## Notes
This file currently bundles HTML, CSS, and JavaScript in one file for simplicity. If your assignment expects separate files, split it into:
```
index.html
style.css
script.js
```
and link them with `<link rel="stylesheet" href="style.css">` and `<script src="script.js"></script>`.
