# Further use cases

This folder contains six examples to explore after the main workshop use case.
Each example includes its source files, the instructions or code used to process
them, and sample results.

## How each example is organized

```text
<use-case>/
  inputs/        source material
  operations/    prompts, skills, and scripts
  outputs/       completed examples
  summary.md     purpose, workflow, and limitations
  index.md       file-by-file guide
  CLAUDE.md      instructions loaded by Claude Code in that folder
```

Read `summary.md` first. Use `index.md` when you need to find a specific file.
The outputs are examples, not guaranteed results for new source material.

## Choose an example

| Use case | Input | Output | Main method |
|---|---|---|---|
| [`class-summarizer`](class-summarizer/) | Workshop transcripts | Ten key takeaways in Markdown and HTML | Reusable prompt followed by an HTML-formatting skill |
| [`research-helper`](research-helper/) | Research papers | One HTML summary per paper and an index | Batch prompt with separate summary and interpretation sections |
| [`exam-makeup-generator`](exam-makeup-generator/) | An existing exam | Candidate questions and an assembled make-up exam | Multi-step skill with instructor review |
| [`interview-coding`](interview-coding/) | Synthetic interview transcripts and a protocol | Indexed transcripts, negative-case memos, and a methods paragraph | Three skills aligned with flexible coding (Deterding & Waters 2018) |
| [`handout-formatting`](handout-formatting/) | Word and PDF course materials | Consistent student and answer-key PDFs | LaTeX templates and a reusable conversion skill |
| [`physics-interactives`](physics-interactives/) | A teaching brief | Standalone HTML simulations and supporting materials | Project-specific skills, templates, and review checklists |

For a shorter example, begin with `class-summarizer` or `research-helper`. For
an example of a reusable skill, use `exam-makeup-generator` or
`handout-formatting`. For qualitative research, use `interview-coding`, which
runs on synthetic transcripts. The `physics-interactives` example has the most supporting
files and is best read after the simpler examples.

## Privacy note

The class-summarizer inputs contain transcripts from real workshop sessions and
include participants' names. Read
[`class-summarizer/inputs/README.md`](class-summarizer/inputs/README.md) before
using the workflow with a class recording. Follow your institution's rules for
recording, storing, and sharing student speech.
