# Claude workshop materials

This repository contains materials for a Bok Center Learning Lab workshop on
working with Claude in folders of files, using Cowork in the Claude desktop app.
It includes one workshop use case, seven further use cases, reference handouts,
and a blank project to start your own work.

You do not need to understand every file. Start with the walkthrough.

## Start here

1. [Download the ZIP file](https://github.com/ll-26-27/claude-workshop-exercise/archive/refs/heads/main.zip)
   and unzip it into a folder that contains only workshop files.
2. In the Claude desktop app, open **Cowork**, choose **Add folder**, and select
   the unzipped folder.
3. Open [`00-start-here/walkthrough.md`](00-start-here/walkthrough.md) and
   follow the steps.

## Repository guide

| Folder | Contents | Start here |
|---|---|---|
| [`00-start-here/`](00-start-here/) | The workshop walkthrough and the tokenizer page. | [`walkthrough.md`](00-start-here/walkthrough.md) |
| [`01-workshop-example-use-case/`](01-workshop-example-use-case/) | The shared workshop activity. It converts photos of table responses into a CSV file and an interactive chart. | [`README.md`](01-workshop-example-use-case/README.md) |
| [`02-further-use-cases/`](02-further-use-cases/) | Seven additional examples involving transcripts, interviews, manuscripts, research papers, exams, handouts, and interactive simulations. | [`README.md`](02-further-use-cases/README.md) |
| [`03-your-project/`](03-your-project/) | A blank project with empty `inputs/`, `operations/`, and `outputs/` folders and starter instructions. | [`README.md`](03-your-project/README.md) |
| [`resources/`](resources/) | A glossary, setup guides, and workshop handouts. | [`README.md`](resources/README.md) |

## Common folder structure

Most examples use three folders:

```text
inputs/       source files such as photos, transcripts, papers, or documents
operations/   prompts, skills, and scripts used to process the source files
outputs/      results produced from the source files
```

In a chat, the conversation is the record of your work. In this structure, the
folder is the record, and you can point several chats at it. If you run an
example with your own material, keep the original files in `inputs/` and write
new files to `outputs/`.

## Setup

For the desktop app and Cowork, see
[`resources/handouts/setup-checklists/desktop-app/`](resources/handouts/setup-checklists/desktop-app/).

## Using Claude Code

Everything here also works in Claude Code, in a terminal or in VS Code. Claude
Code shows each file change directly, reports how full the context window is,
and reads a `CLAUDE.md` file in the folder automatically. The further use cases
include `CLAUDE.md` files for this reason, and the workshop use case includes a
script for Claude Code users. Setup guides for macOS and Windows are in
[`resources/handouts/setup-checklists/code-ide/`](resources/handouts/setup-checklists/code-ide/).
