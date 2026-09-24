# Run Doc — Helen Obiageli Oshikoya site

Static single-page website (no build tools, no framework, no dependencies).

Project files live in the parent directory (this workspace's root is `.lowisa`, which only
contains Freebuff's own data). The site is `index.html` plus `logo2.png` and
`Mrs. Helen Oshikoya.jpeg` (and `DSC_4698.jpg`).

## How to reproduce the preview artifact

A copy of the site must be present inside this thread's workspace because the Preview tab's
`htmlPath` mode only serves files inside the workspace.

1. Copy `index.html` from the parent directory into the workspace root (`.lowisa/index.html`).
   - The copy must rewrite the asset references from `./logo2.png` → `../logo2.png` and
     `./Mrs. Helen Oshikoya.jpeg` → `../Mrs. Helen Oshikoya.jpeg` (favicon, nav logo, and
     portrait), since the images live in the parent directory.
2. No dependency installation is required (vanilla HTML/CSS/JS).

## How to run the server

No server is required. Register the preview with `register_preview` using:

- Mode: `htmlPath`
- Path: `C:\Users\adcon\Downloads\Helen Obiageli Oshikoya\.lowisa\index.html`

The app serves the file on a loopback address (e.g. `http://127.0.0.1:58984/index.html`)
without spawning a separate process.

Note: bash is not installed on this Windows machine, so dev-server approaches
(`python -m http.server`, `npx serve`, etc.) are not viable in this environment.
