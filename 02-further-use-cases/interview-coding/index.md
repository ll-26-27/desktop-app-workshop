# Interview coding file guide

Read [`summary.md`](summary.md) for what the project does and why.
[`CLAUDE.md`](CLAUDE.md) contains the project instructions loaded by Claude
Code.

## Sample corpus (synthetic)

- [`inputs/README.md`](inputs/README.md): study design and why each respondent
  was written the way they were
- [`inputs/protocol.md`](inputs/protocol.md): the semistructured interview
  guide
- [`inputs/attributes.csv`](inputs/attributes.csv): respondent attributes
- [`inputs/transcripts/`](inputs/transcripts/): four transcripts, `R001` to
  `R004`

The transcripts are synthetic. They contain no real respondents.

## Skills

The skills are in `.claude/skills/`. Folders whose names begin with a period
are hidden in Finder; press ⌘⇧. (Command-Shift-period) to show them.

- [`index-transcript`](.claude/skills/index-transcript/SKILL.md): applies
  protocol-based index codes to one transcript and writes a coverage report
- [`find-negative-cases`](.claude/skills/find-negative-cases/SKILL.md): takes
  a claim and returns respondents whose evidence cuts against it
- [`methods-paragraph`](.claude/skills/methods-paragraph/SKILL.md): writes a
  methods paragraph from what the project actually contains

In Claude Code, run a skill by name, for example `/index-transcript R001`. In
Cowork, ask Claude to follow the skill file, for example: "Follow
`.claude/skills/index-transcript/SKILL.md` for R001."

## Example run

- [`outputs/indexed/`](outputs/indexed/): four indexed transcripts and four
  coverage reports
- [`outputs/negative-cases/`](outputs/negative-cases/): audit memos for two
  claims
- [`outputs/methods/methods-paragraph.md`](outputs/methods/methods-paragraph.md):
  the methods paragraph generated after indexing and the audits

## Background

- [`background/how-we-built-this.md`](background/how-we-built-this.md): the
  prompts and steps that produced the project
- [`background/claude-thoughts.md`](background/claude-thoughts.md): the
  original brainstorm of about twenty candidate skills
- [`background/PLAN.md`](background/PLAN.md): the three skill-build tasks
- [`background/tradition.md`](background/tradition.md) and
  [`background/affordance.md`](background/affordance.md): essays on flexible
  coding and what LLMs change about it
