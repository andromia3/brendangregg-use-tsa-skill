# Changelog

All notable changes to this project are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project
adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Fixed

- Explain BCC offcputime's state bitmask in both Linux/off-CPU references:
  state 3 includes interruptible and uninterruptible waits; state 2 includes
  only uninterruptible waits. Add a bounded example and pinned source.

## [1.0.0] - 2026-07-28

Initial release.

### Added

- `SKILL.md`: golden rules, 7-phase master procedure (problem statement →
  triage → USE sweep → TSA sweep → drill-down → root-cause confirmation →
  fix & verify → report), anti-pattern list.
- References distilled from brendangregg.com:
  - `references/use-method.md` — the USE Method complete, incl. the Apollo
    guidance-computer worked example.
  - `references/tsa-method.md` — the TSA Method complete, six states,
    latency-states rule.
  - `references/use-linux-checklist.md` — full Linux USE checklist (physical +
    software resources) with Rosetta Stone cross-OS summary.
  - `references/tsa-linux.md` — labeled reconstruction of TSA on Linux
    (official checklist never published) + Solaris `prstat -mLc` mapping.
  - `references/linux-60s-triage.md` — the "60,000 milliseconds" checklist.
  - `references/linux-observability-tools.md` — tool map by system layer.
  - `references/offcpu-and-flame-graphs.md` — off-CPU analysis + flame graphs.
  - `references/methodology-toolbox.md` — 24 methodologies, 6
    anti-methodologies, performance mantras.
- Report templates: `templates/triage-report.md`, `templates/rca-report.md`,
  `templates/postmortem-report.md`.
- `examples/example-postmortem.md` — worked cgroup CPU-throttling postmortem.
- `README.md` with install instructions for Claude Code, Kimi Code, OpenAI
  Codex, OpenClaw, Gemini CLI, Cursor, Windsurf, Aider, and generic
  agentskills-compatible agents.
- Repo hygiene: `LICENSE` (MIT + attribution note), `CONTRIBUTING.md`,
  `CODE_OF_CONDUCT.md`, `.gitignore`, `.gitattributes`, `.editorconfig`.

[Unreleased]: https://github.com/thecsdoctor/brendangregg-use-tsa-skill/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/thecsdoctor/brendangregg-use-tsa-skill/releases/tag/v1.0.0
