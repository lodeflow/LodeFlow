# LodeFlow

**Build with the agent CLIs you already run.**

LodeFlow is a free, terminal-first workspace for coding agents. It hosts the
real agent CLIs — Claude Code, Codex, Antigravity and Kimi — faithfully, in real
terminals, and never rebuilds their interfaces. Run several at once across all
your projects, keep your Markdown plans and project files beside them, and bring
your own subscriptions.

> The editor should learn the project, not just open it.

Native Rust, Windows-first, macOS shipped and notarized. For developers who
direct agents instead of hand-editing files.

- **[Download for Windows or Apple Silicon](https://lodeflow.com/download/)** —
  free, no account, nothing metered
- **[Read the devlog](https://lodeflow.com/log/)** — the architecture calls and
  the dead ends
- **[Join the Discord](https://discord.gg/zBWsKJJBDS)** — questions, and the
  fastest way to reach me
- **[Discussions](../../discussions)** — bugs and feature requests, where they
  stay findable
- **[The roadmap](https://lodeflow.com/roadmap)** — what's being built, in
  order, including the cut list

## What it does today

- **Hosts the real CLIs.** A true PTY, not a re-rendered chat window. Plan mode,
  slash commands and the interface the agent's own developers built all work,
  because it is their program running.
- **Runs a fleet.** Parallel sessions across many projects, status you can read
  at a glance, sessions that survive a restart with one-keystroke resume, and
  worktree isolation so two agents on one project don't collide.
- **Sorts your accounts.** A registry, per-project binding, per-session identity
  that survives a restart, and a real Codex quota readout — used percentage,
  reset window, plan, and which account has the most left.
- **Shows you the work.** A change summary at the end of each turn, a
  per-session diff viewer, and a proof bundle whose claims are labelled
  *inferred*, *corroborated* or *exact* rather than asserted flat.
- **Opens your files.** Any text file opens, saves and is syntax-highlighted,
  and a Markdown plan sits in a pane beside the terminal rather than in another
  window.

Claude Code and Codex carry the production mileage. Antigravity and Kimi are
newer and have less of it — they run, they're hosted the same way, and they've
had fewer hours against them.

## What it isn't

**It isn't a text editor**, and it isn't trying to become one. Code is a
second-class citizen here, not absent — you can fix a typo without leaving, but
there's no LSP, no autocomplete, no refactoring, no debugger, no minimap. If you
want to type code, you already have somewhere better.

It also doesn't have a command palette, and it won't: the agent's own CLI is the
command surface.

## Status, said plainly

Hosting and the workspace are built and daily-driven. Account handling is in
progress and used every day, but **Claude spend trends and the side-by-side
usage panel don't exist yet** — the half of that feature most people picture
when they hear "usage." Review is at v1: **per-hunk accept/reject and
checkpoint/restore are deliberately not built.**

The memory work is the honest one. The mechanisms are built — project stores,
automatic admission with individual undo, delivery into both Claude and Codex —
but an audit in September did not establish that it measurably helps a later
task or saves quota. It's the differentiator and it is not proved. The
[roadmap](https://lodeflow.com/roadmap) says which of these is being walked now
and which is only planned.

One structural hole worth naming: nothing runs `git fetch`, so the
behind-remote count sits at zero whatever the remote is doing.

Sessions are local and tied to the app. There is no detach, reattach, or
connecting to a session over SSH — that's a different product's territory, and
the difference is on purpose.

## About this repository

**LodeFlow's source is not published here.** Active development happens in a
private repository, and this repo is LodeFlow's public home:

- **[Issues](../../issues)** — bug reports and feature requests. Please use the
  templates; they ask for the things that make a report actionable.
- **[Discussions](../../discussions)** — questions, ideas, and anything that
  isn't a concrete bug.
- **[Releases](../../releases)** — release notes per platform. The downloads
  themselves live on the [download page](https://lodeflow.com/download/), which
  carries a SHA-256 and a verify command for each build.

Opening the source is a decision still ahead of us, not off the table. If and
when it happens, it happens here — issue history and all.

## Reporting a bug well

Because you can't read the code, your report is the only window I have into what
happened. **Help → About** has a **Copy build details** button; paste that. Then
say which agent you were running, what you did, what happened, and what you
expected. A screenshot or a short recording is worth more than a paragraph.

If you'd rather just ask whether it's you or the app, that's what the
[Discord](https://discord.gg/zBWsKJJBDS) is for.

## Who's building this

Built by **[nhillen](https://github.com/nhillen)**. The
[Discord](https://discord.gg/zBWsKJJBDS) is the fastest way to reach me; an
[issue](../../issues) or a [discussion](../../discussions) both get read.
