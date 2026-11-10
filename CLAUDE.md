# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

FinPal is a personal finance agent. The repository is at its initial commit, which tracks only `README.md` and a Python `.gitignore`. `test.py` is an empty, untracked placeholder, not a test suite. There is no application code, dependency manifest, build, lint, or test setup yet.

## Environment

- Python project. VS Code is configured (`.vscode/settings.json`, currently untracked) to use **conda** as both the environment manager and the package manager, so create environments and install packages with conda rather than venv/pip unless told otherwise.
- Development happens on Windows (PowerShell).

## Keeping this file current

No commands or architecture are documented here because none exist yet. Once a dependency manifest (e.g. `environment.yml`), a test runner, a linter, or the agent's module structure is added, record the commands (including how to run a single test) and the high-level architecture in this file.

## How to work with me
- I am a beginner learning agentic AI engineering by building this project.
- Explain concepts before writing code. Prefer hints over full solutions.
- Let me write the code; review it and point out mistakes.
- Never use real bank data; synthetic data only.