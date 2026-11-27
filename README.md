# Folio PDF Studio

A PDF editor that runs entirely in the browser. Files are processed on your device and never uploaded.

**Live site:** https://amit33-design.github.io/github-slideshow/

## Features

- **Edit PDF** — edit existing text, add text, highlight, white-out, redact (content is permanently removed), shapes, freehand drawing, images and signatures; fill PDF forms; reorder, rotate, delete and insert pages; merge PDFs; extract or split pages; undo/redo.
- **Word to PDF** — `.docx` to PDF with selectable text (headings, bold/italic, lists, tables, images).
- **PDF to Word** — PDF to editable `.docx`; scanned pages are inserted as images.
- **Images to PDF** — combine JPG/PNG/WebP images into one PDF.

## Mobile

Works on phones and tablets: pinch with two fingers to zoom, swipe with one finger to scroll, tap a line in Edit text mode to retype it, and tap selected text again to edit it. On a computer, Ctrl (or Cmd) + scroll zooms.

## How it works

A single static `index.html`. Libraries load from cdnjs: pdf.js 3.11.174 (rendering), pdf-lib 1.17.1 (writing PDFs), mammoth 1.6.0 (reading .docx) and JSZip 3.10.1 (writing .docx).

## Known limits

- Edited and added text uses the standard PDF fonts (Helvetica, Times, Courier); characters outside Western European alphabets become "?".
- PDF to Word rebuilds paragraphs, not exact layout; tables and columns become plain lines. No OCR for scanned pages.
- Legacy `.doc` files are not supported; save as `.docx` first.
- Encrypted PDFs are saved with pages as images.

## Run locally

Open `index.html` in a browser, or serve the folder: `python3 -m http.server`.
