# Class summarizer file guide

Read [`summary.md`](summary.md) for the purpose, workflow, and limitations of
this example.

## Source files

- [`inputs/README.md`](inputs/README.md): source and privacy information
- [`inputs/day_1_transcript.md`](inputs/day_1_transcript.md): Day 1 transcript
- [`inputs/day_2_transcript.md`](inputs/day_2_transcript.md): Day 2 transcript
- [`inputs/day_3_transcript.md`](inputs/day_3_transcript.md): Day 3 transcript

## Operations

- [`operations/key-takeaways-prompt.md`](operations/key-takeaways-prompt.md):
  prompt that creates ten takeaways in Markdown
- [`operations/skills/md-to-deepthoughts-html/`](operations/skills/md-to-deepthoughts-html/):
  skill that converts the reviewed Markdown result to standalone HTML

## Example outputs

- [Day 1 Markdown](outputs/day-1-key-takeaways.md) and
  [HTML](outputs/day-1-key-takeaways.html)
- [Day 2 Markdown](outputs/day-2-key-takeaways.md) and
  [HTML](outputs/day-2-key-takeaways.html)
- [Day 3 Markdown](outputs/day-3-key-takeaways.md)

To process another session, add its transcript to `inputs/`, apply the
takeaways prompt, review the result, and then run the HTML conversion skill.
