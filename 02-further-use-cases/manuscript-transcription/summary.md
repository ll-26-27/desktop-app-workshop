# Manuscript transcription

This example transcribes five manuscript pages, from Old English to the
nineteenth century, and builds a reader that shows each page beside its
transcription. It is written for humanists who work with archival images.

The pages:

- *Beowulf*, opening page (c. 975–1025), Old English
- *The Seafarer*, opening page, Exeter Book (10th century), Old English
- Robert Burns, preface to the Glenriddell Manuscript (1791)
- Mary Shelley, draft of *Frankenstein* with revisions between the lines and in
  the margin (1816–17)
- John Keats, "Ode to a Nightingale," holograph with deletions (1819)

Open [`outputs/reader.html`](outputs/reader.html) to see the result.

## How it works

1. The page images are in `inputs/`, with sources, licenses, and standard
   editions listed in [`inputs/README.md`](inputs/README.md).
2. [`operations/01-transcribe-page.md`](operations/01-transcribe-page.md) is run
   once per page. It asks for a diplomatic transcription (the scribe's line
   breaks, letters, abbreviations, deletions, and insertions), a separate
   record of marginalia and later hands, a reading text, a translation where
   needed, and a numbered list of every uncertain reading.
3. [`operations/02-build-reader.md`](operations/02-build-reader.md) turns the
   transcriptions into a single HTML page, with the image on the left and
   switchable views on the right.

## The move worth noticing: what it saw versus what it remembers

*Beowulf* and *The Seafarer* are in the model's training data. A model asked to
transcribe them can produce a fluent text from memory, including letters that
burned away in 1731. The prompt requires it to say whether it recognizes the
text and to mark every reading that comes from memory rather than from the
page as `[supplied: …]`. Open the *Beowulf* transcription and compare the
supplied letters with the burnt right edge of the image.

The same issue appears in the draft pages: the published *Frankenstein* and
Keats's final text are also in the training data, and a model can quietly
"correct" a draft toward the version it knows. The transcriptions keep the
draft's own words ("my man compleated," "a painful numbness falls") and list
what they could not read.

## What to check

The transcriptions have not been checked against an edition. That is the
exercise:

1. Choose a page and open its standard edition (listed in
   [`inputs/README.md`](inputs/README.md)).
2. Compare it line by line with the diplomatic transcription.
3. For each difference, decide whether the model misread the page, the
   edition emends it, or the image is not good enough to tell.

Expect particular trouble with the letter wynn (ƿ), which looks like *p*, with
struck words in the drafts, and with the two small images (Frankenstein and
Keats, about 500 pixels wide).

## Run it on your own pages

1. Put your images in `inputs/`, with a line for each in `inputs/README.md`
   saying where it came from and whether you may share it.
2. Run [`operations/01-transcribe-page.md`](operations/01-transcribe-page.md)
   on each image. Adjust the conventions to your field's (for example, Leiden
   conventions for epigraphy).
3. Check a sample against the original before you rely on the rest.
4. Run [`operations/02-build-reader.md`](operations/02-build-reader.md).

Do not use this with images you do not have the right to share, or with
unpublished archival material whose terms of use prohibit uploading.
