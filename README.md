# Canvasly Studio

A lightweight, browser-based canvas editor for building visual compositions — add text, images, gradients, and shapes, then fine-tune with filters, blend modes, and layer controls.

[![Live Demo](https://img.shields.io/badge/demo-live-6c3fff?style=flat-square)](https://canvaslystudio.vercel.app)
![HTML](https://img.shields.io/badge/HTML-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572b6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-brightgreen?style=flat-square)

## Features

- **Add elements** — text, gradients, images, and shapes onto a freeform canvas
- **Filters** — blur, grayscale, brightness, contrast, saturation, sepia, hue rotation
- **Border controls** — width, radius, color, and style (solid/dashed/dotted/double)
- **Opacity & blend modes** — 12 CSS blend modes for creative layering
- **Transform** — rotation and scale per element
- **Layer management** — reorder, select, and delete from a live layer list
- **Undo/redo** — full history stack for moves, resizes, edits, and deletions
- **Duplicate** — clone the selected element with `Ctrl+D`
- **Export to PNG** — render your composition and download it as an image
- **Keyboard shortcuts** — `Ctrl+Z` / `Ctrl+Shift+Z` (undo/redo), `Ctrl+D` (duplicate), arrow keys (nudge), `Delete` (remove), `Esc` (deselect)

## Usage

Open `index.html` in a browser, or visit the [live demo](https://canvaslystudio.vercel.app). Click an "Add elements" button to drop a new item onto the canvas, drag to reposition, use the resize handle to scale, and tune it with the sidebar controls.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no build step, no framework. PNG export uses [html2canvas](https://html2canvas.hertzen.com/).

## License

MIT © Abednego Ndimu
