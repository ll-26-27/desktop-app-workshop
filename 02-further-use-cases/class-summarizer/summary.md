# Class summarizer

This example converts a workshop transcript into a short document with ten key
takeaways. It produces a Markdown file for editing and a standalone HTML file
for reading, printing, or sharing.

Three reviewed examples are included:

- [Day 1 Markdown](outputs/day-1-key-takeaways.md) and
  [HTML](outputs/day-1-key-takeaways.html)
- [Day 2 Markdown](outputs/day-2-key-takeaways.md) and
  [HTML](outputs/day-2-key-takeaways.html)
- [Day 3 Markdown](outputs/day-3-key-takeaways.md)


## How it works

1. A transcript with speaker labels is placed in `inputs/`.
2. [`operations/key-takeaways-prompt.md`](operations/key-takeaways-prompt.md)
   asks the assistant to select exactly ten takeaways and write them to Markdown.
3. Each takeaway has a one-sentence heading followed by a short explanation
   based on the transcript.
4. A final section records useful points that did not fit in the top ten.
5. The
   [`md-to-deepthoughts-html` skill](operations/skills/md-to-deepthoughts-html/SKILL.md)
   converts the Markdown result to HTML.

The prompt asks for the source session, time range, and speakers at the top of
the output. It also asks the writer to use specific examples and quotations from
the session. These requirements make it easier to check the summary against the
transcript.

## Run it with another transcript

1. Add a transcript to `inputs/`. Do not overwrite the source transcript.
2. Apply
   [`operations/key-takeaways-prompt.md`](operations/key-takeaways-prompt.md)
   and specify the output filename.
3. Review names, quotations, and claims against the transcript.
4. Run the HTML skill on the reviewed Markdown file.

See [`inputs/README.md`](inputs/README.md) for the origin of the sample
transcripts and the privacy issues involved in using class recordings.

## Design choices

- The fixed count requires the model to rank the material instead of returning
  a long list.
- Separate headings make the result easy to scan.
- Source information and quotations support manual verification.
- Markdown is the editable source; HTML is the distribution format.

## Limitations

A transcript summary can omit context, misattribute speech, or reproduce
transcription errors. Review it before distribution. For recordings involving
students, confirm consent, storage, and access requirements before sending the
transcript to a model or adding it to a repository.

The same workflow can be adapted to meetings, lectures, interviews, or
conference sessions by changing the output structure and review criteria in the
prompt.
