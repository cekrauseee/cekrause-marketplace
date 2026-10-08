# cekrause marketplace

Personal plugin marketplace for Codex and Claude Code, maintained by Henrique Krause. Each plugin points at its public Git repository over HTTPS, which both hosts can clone without an SSH setup.

## Plugins

- `harness`: external project context and focused engineering workflows for agents. Source: https://github.com/cekrauseee/harness

## Manifests

- `.claude-plugin/marketplace.json` for Claude Code
- `.agents/plugins/marketplace.json` for Codex

## Register

Claude Code:

```bash
claude plugin marketplace add https://github.com/cekrauseee/cekrause-marketplace.git
claude plugin install harness@cekrause
```

Codex: add this repository as a Git marketplace with `codex plugin marketplace add`, then run `codex plugin add harness@cekrause`.

A machine that keeps a local checkout of this repository can register that directory instead; edits then take effect after `claude plugin marketplace update cekrause` or a Codex restart, and are published by pushing.
