# Contributing to Gilamonster Foundation

Thank you for your interest in contributing! This guide applies to all repos
in the Gilamonster Foundation org.

## Getting Started

1. Fork the repository
2. Create a branch from `main` for your change
3. Make your changes with tests
4. Run the repo's full check suite (usually `cargo test` or `just check`)
5. Open a pull request

## Safety Requirements

All repos enforce safety gates. Your PR **will be blocked** if it contains:

- Secrets, API keys, or tokens
- Private IP addresses or internal hostnames
- Hardcoded filesystem paths
- High-entropy strings that look like credentials

This is intentional. We take supply-chain safety seriously.

### Pre-commit Hooks

Install pre-commit hooks after cloning:

```bash
pip install pre-commit
pre-commit install
```

This catches issues locally before you push.

## Code Style

- **Rust**: `cargo fmt` + `cargo clippy -- -D warnings`
- **Python**: `black` + `ruff check`
- All warnings must be resolved (zero-warnings policy)

## Pull Request Process

1. PRs require at least one review before merge
2. All CI checks must pass
3. Keep PRs focused — one logical change per PR
4. Write a clear description: what changed and why

## Centaur Developers (Human / Agent Contributors)

We welcome contributions from human/agent teams — what we call **Centaur
Developers**. If an AI agent helped produce your contribution:

- **Disclose it.** Credit the agent in commit trailers using the synthetic
  `model@harness` identity format (e.g.
  `Co-Authored-By: nemotron3:33b <nemotron3:33b@newt-agent>` — not a real
  email address).
- **Own it.** A human reviews and is accountable for everything that lands.
  Autonomous agent work always arrives through a pull request, never a
  direct push.
- **Follow the rules repo.** Templates, skills, and the full crediting
  conventions live in
  [Gilamonster-Foundation/agents](https://github.com/Gilamonster-Foundation/agents).

## License

By contributing, you agree that your contributions will be licensed under the
Apache License 2.0.
