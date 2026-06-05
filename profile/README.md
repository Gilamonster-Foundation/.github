# Gilamonster Foundation

**Open Source Software — Designed for Agentic Workflows**

We build tools and educational resources at the intersection of developer
tooling, data provenance, and agentic systems. Our specific domain is
**Python ↔ Rust interop**: reaching for Rust *from* Python — bindings,
real threads beyond the GIL, and type-system rigor — without giving up
what makes Python productive.

## How We Build: Centaur Development

We practice **Agentic Engineering, not Vibe Coding**. A Centaur Developer is
a human / agent pair working as one contributor: the human owns judgment —
architecture, review, and the merge button — while agents carry throughput.
The discipline is the point:

- **Every change rides the same rails:** branch → test-driven development →
  all checks green → pull request → CI → human merge. No exceptions for
  agent-authored code.
- **Every bug fix ships a regression test** that failed before the fix.
- **Zero-warnings policy** at merge — lint noise is where real issues hide.
- **Agents work on a leash:** tool authority is capability-governed and
  deny-by-default (see [agent-bridle](https://github.com/Gilamonster-Foundation/agent-bridle)),
  not entrusted to prompt hygiene.
- **Agents are credited, not hidden:** agent contributions are attributed as
  `model@harness` (e.g. `nemotron3:33b@newt-agent`) so provenance survives
  in the history.

The canonical rules, templates, and skills live in the
[agents](https://github.com/Gilamonster-Foundation/agents) repo.

## The PyO3 Style

Our house pattern for shipping software: **a Rust core with Python reach.**
The engine is a Rust workspace — correctness, speed, and real threads beyond
the GIL — exposed to Python through [PyO3](https://pyo3.rs) and built with
[maturin](https://github.com/PyO3/maturin), so `pip install` delivers
prebuilt wheels and Python users never need a Rust toolchain. The Rust
crates stay independently usable from crates.io; the Python package is a
first-class surface, not a wrapper afterthought. One source of truth, two
ecosystems served.

## Projects

### Build with agents

| Repo | What it is |
|------|------------|
| [newt-agent](https://github.com/Gilamonster-Foundation/newt-agent) | **Small, fast, local-first agentic coder** — vi to Hermes-Agent's emacs. A single Rust binary with a sharp, minimal tool set that runs against your local hardware by default: no cloud bytes leave your machine unless you deliberately install a provider plugin. Ships its core as the `newt-agent-py` PyO3 wheel. We build it because an agentic coder should be an instrument you own, not a subscription you rent. |
| [hermes-thoon](https://github.com/Gilamonster-Foundation/hermes-thoon) | **A fork of [hermes-agent](https://github.com/NousResearch/hermes-agent) made for SPEED.** Takes a feature-rich Python agent and moves its hot paths onto the shared Rust crates that power newt-agent — the PyO3 style proven on a real, living codebase rather than a toy benchmark. |
| [monitor-agent](https://github.com/Gilamonster-Foundation/monitor-agent) | **A lightweight systems-monitoring agent for operations.** Rust, small footprint, built to give a fleet of machines (and the agents running on them) operational eyes without dragging in a heavyweight observability stack. |

### Keep agents honest

| Repo | What it is |
|------|------------|
| [agent-bridle](https://github.com/Gilamonster-Foundation/agent-bridle) | **The capability leash for agent tools.** A capability-governed tool registry: every tool declares the authority it needs, dispatch refuses unless required ⊑ granted, and tools receive only the meet of the two — least authority by construction, backstopped by Landlock on Linux. We build it because the confused-deputy problem is an *architecture* problem; hardening the prompt does not fix it. |
| [agent-mesh](https://github.com/Gilamonster-Foundation/agent-mesh) | **Cryptographic peer-to-peer agent coordination** — vi-minimal mesh, no broker. Agents coordinate directly with signed messages instead of trusting a central service. We build it because a coordination layer should not be a single point of failure, compromise, or rent. |

### Learn and contribute

| Repo | What it is |
|------|------------|
| [agents](https://github.com/Gilamonster-Foundation/agents) | **The Centaur Developer base.** Canonical rules, templates, skills, and soul files for human / agent contributors across the org — including the crediting rules that put `model@harness` attribution into git history. Start here if you (or your agent) want to contribute. |
| [rust-for-pythonistas](https://github.com/Gilamonster-Foundation/rust-for-pythonistas) | **Learn Rust through Python analogies** — from ownership to content-addressable data. The on-ramp for Python developers joining the PyO3 style. |
| [.github](https://github.com/Gilamonster-Foundation/.github) | Organization-level defaults, templates, and safety workflows — secret scanning, push protection, and CI gates shared across the org. |

### In the hangar

Beyond the public repos, we are developing multi-agent orchestration —
flights of local-model workers coordinated over agent-mesh, each on an
agent-bridle leash — privately. Those projects go public once they pass
our go-public scrub, the same provenance discipline we apply to everything
else.

## Philosophy

> "Computer Science has as much to do with Computers as Astronomy does with
> Telescopes." — Edsger W. Dijkstra

Every project here is a telescope, not the sky. The code, the tools, the
frameworks — they exist to serve something beyond themselves. User data is
sovereign. Tools are replaceable. Formats should be plain text. Don't build
lock-in.

## Contributing

Centaur Developers welcome — human, agent, or both. The contribution rules
live in [agents](https://github.com/Gilamonster-Foundation/agents); this
org's [CONTRIBUTING.md](https://github.com/Gilamonster-Foundation/.github/blob/main/CONTRIBUTING.md)
and `AGENTS.md` point there. All repositories in this org enforce safety
gates: secret scanning, push protection, and CI checks that reject leaked
credentials or private infrastructure details.
