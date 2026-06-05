# Agents

Gilamonster Foundation repositories are built by **Centaur Developers** —
human/agent teams contributing as one unit.

The canonical rules, templates, and skills live in
**[Gilamonster-Foundation/agents](https://github.com/Gilamonster-Foundation/agents)**.
Do not duplicate them here; this file is a pointer so that agents (and
humans) who land in this repo know where the rules of the road are.

The short version, binding in every repo of this org:

1. **The PR is the deliverable.** All changes land through pull requests
   with CI gates. Agents never push to `main`.
2. **Credit is provenance.** Agent contributions are disclosed in commit
   trailers using the synthetic `model@harness` identity format — see the
   [crediting rules](https://github.com/Gilamonster-Foundation/agents#crediting-agents).
3. **Safety gates are non-negotiable.** No secrets, no private
   infrastructure details, no leaked credentials. CI enforces this; don't
   fight it.
4. **Every bug fix carries a regression test.**

For everything else — soul files, skills, rules templates — start at the
[agents](https://github.com/Gilamonster-Foundation/agents) repo.
