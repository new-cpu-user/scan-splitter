# Scan Splitter

Turn one big scan into separate documents — one file per letter, form,
or page fed through the scanner. Runs entirely in the browser; nothing
you scan is ever uploaded anywhere.

## Try it

**[Open Scan Splitter](https://USERNAME.github.io/scan-splitter/)**
*(replace `USERNAME` above once this repo's GitHub Pages is live)*

## Why

Most scanners batch-scan a stack of paper into one long PDF. This app
takes that PDF back apart into the separate documents it actually
contains — dropping blank backsides for single-sided pages, and either
treating every physical sheet as its own document or splitting on a
blank divider sheet, whichever matches how you scanned.

## Features

- Drag-and-drop a scanned PDF, or tap to browse — works with output
  from any scanner or scanning app, not tied to one brand
- Two splitting modes: one document per physical sheet, or documents
  separated by a blank divider page
- Adjustable sensitivity for what counts as "blank," with a live
  preview of the split
- Click any page thumbnail to manually correct its classification
- Editable name for each detected document before saving
- Download everything as one ZIP, or grab a single document on its own
- Installable as a home-screen app on iOS, Android, and desktop

## Privacy

Everything happens on-device, in this browser tab. The scanned PDF is
never sent to a server — rendering, blank-page detection, and
splitting all happen locally using in-browser PDF libraries. This repo
holds only the app's code, which contains no personal data; nothing
anyone scans with it ever touches GitHub's servers or anywhere else.

## Installing it as an app

Open the live link above, then:

- **iPhone / iPad (Safari):** Share icon → *Add to Home Screen*
- **Android (Chrome):** ⋮ menu → *Add to Home screen* / *Install app*
- **Mac / Windows (Chrome or Edge):** the install icon in the address
  bar, or ⋮ menu → *Install Scan Splitter*

## How it works

A single self-contained `index.html`, using:

- [pdf.js](https://mozilla.github.io/pdf.js/) to render and inspect pages
- [pdf-lib](https://pdf-lib.js.org/) to assemble the split output PDFs
- [JSZip](https://stuk.github.io/jszip/) to bundle multiple documents into one download

Blank-page detection renders each page and measures what fraction of
it is ink versus blank paper. Pages are paired front/back the way a
duplex scanner produces them, then grouped into documents according to
whichever mode is selected.

## Running it yourself

It's a static site — no build step, no server-side code. Clone or
download this repo and open `index.html` directly, or host the folder
anywhere that serves static files (GitHub Pages, Netlify, a personal
server, etc.).
