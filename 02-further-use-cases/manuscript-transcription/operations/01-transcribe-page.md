# Prompt: transcribe a manuscript page

Use this prompt once per image in `inputs/`. It produces one Markdown file per
page in `outputs/transcriptions/`, with the same base name as the image.

---

## The task

Transcribe the manuscript page in the image I name. Work from what is visible
on the page. The goal is a transcription a scholar could check line by line
against the image.

### Before you start

1. Look at the whole page. State what you think it is (language, approximate
   date, type of document) and how legible it is.
2. **Say whether you recognize the text.** Many famous texts are in your
   training data. If you recognize this one, say so, and then transcribe what
   you see rather than what you remember. Wherever a reading depends on your
   memory of the text rather than on visible letters (a burnt edge, a blot, a
   faded word), mark it with `[supplied: …]`. Never fill a gap silently.

### Conventions for the diplomatic transcription

- **One line of output per line of the manuscript**, numbered. Keep the scribe's
  line breaks, including words split across lines.
- **Keep the letters the scribe used**: þ, ð, æ, ƿ (wynn, not *w* and not *p*),
  ⁊ (Tironian *et*), ꝥ (crossed thorn, for *þæt*), ſ (long s), and superscript
  letters (write `Rob^t^`). Letter shapes that are only variant forms of
  ordinary letters (insular *g*, *r*, and *s*) are written as ordinary letters.
  Keep abbreviation marks as written (for example, `ū` for a macron over *u*).
  Do not expand abbreviations here.
- **Keep the scribe's word division and punctuation**, including the medieval
  point (·) where it is used.
- **Deletions:** `~~struck text~~`. If a deleted word cannot be read, write
  `~~[illegible]~~`.
- **Insertions:** put the inserted text where it belongs in the line, in
  `⟨angle brackets⟩`, and say where it is written: `⟨that I might⟩[interlinear]`,
  `⟨beautiful!⟩[left margin]`. Include caret marks as `^` if visible.
- **Uncertain readings:** `[?word]` for a probable reading, `[illegible]` when
  you cannot read a word, `[…]` for text lost to damage, with an estimate of how
  many letters are lost if you can judge it: `[…3…]`.

### Sections to write

Write `outputs/transcriptions/<image-name>.md` with these sections:

1. **About this page**: what it is, date, hand(s), condition, and whether you
   recognized the text.
2. **Diplomatic transcription**, following the conventions above.
3. **Marginalia and later additions**: every mark that is not part of the main
   text, such as folio numbers, stamps, glosses, corrections in another hand,
   and pen trials. Give the location, a transcription, and whether it appears
   to be in the main hand or a different one. Say how sure you are.
4. **Reading text**: the same text with abbreviations expanded, word division
   regularized, and deletions removed, so it can be read continuously. For
   verse, set out the lines as verse. Do not modernize spelling.
5. **Translation** (for languages other than modern English): a close prose
   translation.
6. **Uncertainties**: a numbered list of every uncertain, supplied, or
   illegible reading, each with its line number and what would settle it
   (a higher-resolution image, the physical manuscript, a standard edition).

### Before you call it done

- Every line of the manuscript has a line in the diplomatic transcription.
- Every `[supplied: …]`, `[?…]`, `[illegible]`, and `[…]` also appears in the
  Uncertainties list.
- Nothing in the reading text or translation depends on a reading that was not
  marked as uncertain.
- The file does not claim to have checked the transcription against an
  edition. That check is for a person to do.
