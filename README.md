# LodeFlow

**The unit of software work moved from files to sessions. LodeFlow is the agent
workspace built for that shift.**

LodeFlow is a native desktop workspace for directing coding agents. It hosts the
real agent CLIs — Claude Code, Codex — faithfully in real terminals (it never
rebuilds their UI), runs a fleet of them across all your projects, sorts your
subscriptions so you never get throttled, lets you review what they did, and
learns your project so every session starts smarter than the last.

> **The editor should learn the project, not just open it.**

Native Rust, Windows-first. For developers who direct agents instead of
hand-editing files.

## What it is / isn't

- **Is:** a workspace that *hosts* the real agents and surrounds them with
  orchestration, subscription management, review, and a learning loop.
- **Isn't an IDE.** No code editing, LSP, autocomplete, or refactoring —
  directing agents is the job, not typing code.

## About this repository

**LodeFlow's source code is not published here (yet).** Active development
happens in a private repository. This repo is LodeFlow's public home:

- **[Issues](../../issues)** — bug reports and feature requests. Please use the
  templates; they ask for the details that make a report actionable.
- **[Discussions](../../discussions)** — questions, ideas, and everything that
  isn't a concrete bug or feature request.
- **[Releases](../../releases)** — downloads, once public builds ship.

Opening the source is a decision still ahead of us, not off the table. If and
when it happens, it happens here — issue history and all.

## Status — early, and said plainly

The host + workspace (faithful terminal hosting, multi-project, parallel
sessions, markdown, themes, stable auto-update) work and are daily-driven. The
differentiators — subscription routing, agent-output review, and the
learning/memory loop — are in progress.

## Reporting a bug well

Because you can't read the code, your report is the only window we have into
what happened. The bug template asks for your LodeFlow version, OS, which agent
CLI you were running, and steps to reproduce — a screenshot or short recording
is worth more than a paragraph.

## Links

- **Site:** lodeflow.com *(soon)*
- **Devlog:** lodeflow.com/log *(soon)*

## Who's building this

Built by **[nhillen](https://github.com/nhillen)**. The best way to reach me
about LodeFlow is an [issue](../../issues) or a
[discussion](../../discussions) — both get read.
