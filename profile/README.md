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

### Learn

| Repo | Description |
|------|-------------|
| [rust-for-pythonistas](https://github.com/Gilamonster-Foundation/rust-for-pythonistas) | Learn Rust through Python analogies — from ownership to content-addressable data |
| [agents](https://github.com/Gilamonster-Foundation/agents) | Rules templates and skills for Centaur Developers (human / agent contributors) |

### Agent Stack

| Repo | Description |
|------|-------------|
| [newt-agent](https://github.com/Gilamonster-Foundation/newt-agent) | Small, fast, local-first agentic coder — vi to Hermes-Agent's emacs |
| [agent-bridle](https://github.com/Gilamonster-Foundation/agent-bridle) | The capability leash for agent tools — a capability-governed tool registry for the Gilamonster agent line |
| [agent-mesh](https://github.com/Gilamonster-Foundation/agent-mesh) | Cryptographic peer-to-peer agent coordination — vi-minimal mesh, no broker |
| [hermes-thoon](https://github.com/Gilamonster-Foundation/hermes-thoon) | A fork of hermes-agent made for SPEED |
| [monitor-agent](https://github.com/Gilamonster-Foundation/monitor-agent) | A lightweight systems monitoring agent for operations |

Each repo's README carries the longer story — what it is, why it exists,
and how it fits the PyO3 style.

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
