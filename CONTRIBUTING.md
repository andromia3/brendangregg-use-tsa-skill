# Contributing

Thanks for helping make performance analysis less guessy. This project is a
documentation-only repository — no build, no tests, no dependencies.

## Ground rules

1. **Fidelity to the primary sources.** This repo distills Brendan Gregg's
   published methodologies. If you quote or paraphrase, check against the
   original (brendangregg.com, the books, the ACM articles) and cite the
   source in the file's header blockquote. Do not redistribute his pages,
   images, or book excerpts — original text with attribution only.
2. **Honesty markers stay honest.** Content that is reconstructed rather than
   published (e.g. `references/tsa-linux.md`) must keep its provenance label.
   If you add similar material, label it the same way.
3. **Vendor-agnostic stays vendor-agnostic.** OS-specific detail belongs in
   the matching `references/*-<os>.md` file, not in `SKILL.md`. The skill body
   must stay usable on any machine with a shell.
4. **Command accuracy.** Every command in a checklist should be real and
   current. If a tool is deprecated or kernel-version-gated, say so inline.
5. **Match the house style.** GitHub-flavored markdown, tables for checklists,
   blockquoted provenance header at the top of each reference file, absolute
   dates in examples, 2-space indentation (see `.editorconfig`). Keep
   `SKILL.md` terse — depth belongs in `references/`.

## How to contribute

- **Fixes** (wrong command, stale metric, broken link): open a PR directly.
- **New OS checklist**: copy the structure of
  `references/use-linux-checklist.md`, fill the resource ×
  utilization/saturation/errors matrix for your OS, note what cannot be
  measured, and link it from `SKILL.md`'s reference table and the README.
- **New worked example**: follow `examples/example-postmortem.md` — realistic
  or clearly-labeled fictional, every claim tied to a command and output.
- **Template improvements**: keep placeholders generic; a template must work
  for a laptop, a VM, and a fleet.

## Commit & PR style

- Imperative commit messages (`add freebsd use checklist`, `fix runqlat
  package name`).
- One logical change per PR. Describe *what source* a factual change is based
  on — "I measured it on kernel 6.9" is a fine source.
- Update `CHANGELOG.md` (Unreleased section) with user-visible changes.

## Reporting issues

Open an issue with: what you were doing, what the skill told the agent to do,
and what was wrong or missing. Reproduction with a real machine's redacted
output beats prose.
