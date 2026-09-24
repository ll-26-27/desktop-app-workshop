# Interactive simulations

This example contains project-specific Claude Code skills for building small
browser-based teaching simulations. Each simulation is a single HTML file that
can be opened locally without a server or build process.

The project uses design ideas associated with PhET simulations, but the included
files are independent workshop examples. They have not gone through PhET's
development or research process.

## What is included

The main skills are stored under [`.claude/skills/`](.claude/skills/):

- `phet-sim`: creates a simulation after asking about the learning goal,
  learners, likely misconceptions, controls, and model limits
- `phet-activity`: creates a classroom activity around an existing simulation
- `phet-accessibility-audit`: checks a simulation against a defined
  accessibility checklist
- `phet-rationale`: drafts a short explanation of the teaching approach

The skills include templates and rubrics so the output can be reviewed against
explicit requirements rather than appearance alone.

Three completed simulations are in
[`outputs/sims/`](outputs/sims/):

- enzyme kinetics
- Hardy–Weinberg equilibrium
- predator–prey dynamics

See [`outputs/sims/README.md`](outputs/sims/README.md) for their learning goals
and technical checks.

## Workflow

1. Write a brief that identifies the concept, learner group, learning goal, and
   common misconception.
2. Run `/phet-sim` and answer its design questions.
3. Review the scientific or disciplinary model and test every control.
4. Run `/phet-activity` to draft a lesson using prediction, observation,
   explanation, and synthesis.
5. Run `/phet-accessibility-audit`, then fix and retest reported problems.
6. Ask a subject-matter expert and representative learners to review the result.

The sample input is
[`inputs/heat-pumps-teaching-brief.md`](inputs/heat-pumps-teaching-brief.md).

## Technical requirements

The simulation skill requires each output to:

- use one self-contained HTML file;
- work when opened from a local `file://` path;
- avoid external libraries and network requests by default;
- include keyboard-accessible controls and visible labels;
- provide a reset control;
- state the model's limits; and
- document the learning goal and design decisions.

SVG is the default rendering method. Canvas is available for large numbers of
moving objects, and a linked-graph template supports a model view beside a live
graph.

## Limitations

An interactive page can be visually polished while using an incorrect model or
supporting no clear learning goal. The rubrics reduce this risk but do not
replace expert review or testing with students. The examples do not demonstrate
measured learning gains, full accessibility conformance, or suitability for a
particular course.

The same workflow can be adapted to other fields when a concept can be expressed
through a small model with meaningful user-controlled variables.
