# Prompt: build a side-by-side reader

Use this prompt after `01-transcribe-page.md` has produced files in
`outputs/transcriptions/`.

---

## The task

Build a single HTML page, `outputs/reader.html`, that shows each manuscript page
next to its transcription.

- One section per page, in filename order. On the left, the image from
  `inputs/`, linked by relative path (`../inputs/<name>.jpg`) so the page works
  when opened from the folder. Clicking the image opens it full size.
- On the right, the transcription, with buttons to switch between
  **Diplomatic**, **Reading text**, **Translation** (only where one exists),
  **Marginalia**, and **Uncertainties**.
- Show deletions as struck-through text and insertions in a different color,
  with their location visible on hover.
- Keep the diplomatic transcription in a monospace font with line numbers, so a
  reader can match lines to the image.
- A contents list at the top links to each page.
- Everything except the images is inline in the one HTML file. No external
  scripts, fonts, or stylesheets.
- Say in a short note at the top that the transcriptions were made by a model
  and have not been checked against an edition.
