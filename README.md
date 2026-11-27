# Canvasly Studio

A lightweight, browser-based canvas editor for building visual compositions. Add text, images, gradients and shapes, then fine-tune them with filters, blend modes and layer controls.

[![Live Demo](https://img.shields.io/badge/demo-live-6c3fff?style=flat-square)](https://canvalystudio.vercel.app)
![HTML](https://img.shields.io/badge/HTML-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572b6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/license-MIT-brightgreen?style=flat-square)

## Features

- **Add elements**: text, gradients, stock images, shapes, or your own images (Upload button, or drag a file onto the canvas)
- **Edit text in place**: double-click a text element (or select it and press `Enter`), type, then click away or press `Esc`
- **Filters**: blur, grayscale, brightness, contrast, saturation, sepia, hue rotation
- **Border controls**: width, radius, colour and style (solid / dashed / dotted / double)
- **Opacity and blend modes**: 12 CSS blend modes for creative layering
- **Transform**: rotation and scale per element
- **Layers**: live layer list (top layer first), select, delete, bring forward and send backward
- **Undo / redo**: full history for adds, moves, resizes, text edits, style changes, reordering and deletions
- **Duplicate**: clone the selected element
- **Autosave**: your canvas is saved in the browser and restored when you come back
- **Export to PNG**: renders the canvas (without selection outlines or handles) and downloads it
- **Works on touch screens**: drag and resize use pointer events; the sidebar stacks under the canvas on phones

### Keyboard shortcuts

| Keys | Action |
| --- | --- |
| `Ctrl+Z` | Undo |
| `Ctrl+Shift+Z` or `Ctrl+Y` | Redo |
| `Ctrl+D` | Duplicate selected element |
| `Delete` or `Backspace` | Remove selected element |
| `]` / `[` | Bring forward / send backward |
| Arrow keys | Nudge 1px (hold `Shift` for 10px) |
| `Enter` | Edit the selected text |
| `Esc` | Stop editing text, or deselect |

On macOS use `Cmd` instead of `Ctrl`.

## Run it locally

Canvasly Studio is a single `index.html` file with no build step. You can open the file directly, but a small local server is better because autosave and image export behave more reliably over `http://`.

**1. Clone the repository**

```
git clone https://github.com/abednegoingplaces/Canvaly-Studio.git
```

**2. Go into the folder**

```
cd Canvaly-Studio
```

**3. Start a local server** (pick one; you only need Python *or* Node.js)

With Python:

```
python -m http.server 5173
```

With Node.js:

```
npx serve -l 5173
```

**4. Open the editor**

Go to <http://localhost:5173> in your browser. Stop the server with `Ctrl+C` in the terminal.

## Deploying

The live demo is on Vercel and redeploys automatically when `main` changes. Any static host works: upload `index.html` as-is.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| Toolbar icons are missing | The icon font loads from the jsDelivr CDN. Check your internet connection or ad-blocker. |
| "Export library failed to load" | html2canvas loads from cdnjs. Check your connection, then reload the page. |
| Exported PNG ignores filters or blend modes | html2canvas does not support CSS `filter` or `mix-blend-mode`, so those effects are skipped in the export. Everything else (position, size, rotation, borders, opacity) is kept. |
| Stock image does not appear | Stock photos come from Unsplash. If one fails, a random Picsum photo is used instead. Uploaded images always work offline. |
| "Autosave is full" message | Browsers allow about 5 MB of saved data. Large uploaded photos can fill it; the canvas still works, but it will not be restored after a reload. Use **Clear**, or upload smaller images. |
| I want a fresh canvas | Click **Clear** (you can undo it with `Ctrl+Z`). |
| `python` is not recognised | Install Python from python.org, or use the Node.js command instead. |

## Tech

Plain HTML, CSS and vanilla JavaScript: no framework, no build step. PNG export uses [html2canvas](https://html2canvas.hertzen.com/) and icons come from [Tabler Icons](https://tabler.io/icons).

## License

MIT © Abednego Ndimu
