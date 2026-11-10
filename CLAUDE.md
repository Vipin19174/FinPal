# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

FinPal is a personal finance agent, built as the capstone of a 26-week self-study roadmap in agentic AI engineering. The repository is a learning project first: the owner writes the code, and Claude acts as tutor and reviewer (see "How to work with me").

There is no application code yet. `test.py` is an empty placeholder, not a test suite, and there is no dependency manifest, build, lint, or test setup.

## Roadmap

The plan lives in a Claude doc: https://claude.ai/artifact/WoV2v85gMktDRrmHZdJPcL. Read it with the Claude Docs tools (not a web fetch) when a session starts with "Tutor: ..." or refers to a phase, week, quiz, milestone or exit test. It defines, per phase, the weekly topics, a mini-project, a capstone milestone and an exit test, plus a progress tracker.

Planned build order, each phase adding a layer to the same agent: Python and Git foundations → hand-written tool-calling loop on Bedrock (`finpal/llm.py`) → Strands agent with tools → FastAPI service and Streamlit UI in Docker → Databricks data and RAG → multi-agent with MCP and human approval → guardrails, MLflow tracing and evals → Kong, personas and AgentCore deployment.

The first capstone milestone (Phase 0) is a script that generates a synthetic `transactions.json` (date, merchant, amount, category).

## Environment

- Windows, PowerShell in the VS Code terminal.
- Conda environment `finpal` (Python 3.12) at `C:\Users\vipin\.conda\envs\finpal`; only pip and setuptools are installed so far. Activate with `conda activate finpal`. VS Code (`.vscode/settings.json`) uses conda as environment and package manager, so install packages with conda rather than venv/pip unless told otherwise.
- Conda (`C:\ProgramData\anaconda3`) is not on PATH in non-interactive shells, where plain `python` is the global 3.13. To run something in the project environment from a tool call, use `C:\Users\vipin\.conda\envs\finpal\python.exe` directly.

## Repository conventions

- Work happens on feature branches (e.g. `feature/phase1`) pushed to `origin`, not directly on `main`.
- `Questions/` holds one folder per phase (e.g. `Questions/phase0/`) with one file per session (e.g. `week1_session3.md`) containing that session's questions, the owner's answers and Claude's reviews together. Each phase folder has a `README.md` indexing its sessions and their status, and an `images/` folder for screenshots.
- `Solutions/` is gitignored, so it exists only locally. It held answers before the workbook format and is no longer the place for them.

## Keeping this file current

Once a dependency manifest (e.g. `environment.yml`), a test runner, a linter, or the agent's module structure is added, record the commands (including how to run a single test) and the high-level architecture in this file.

## How to work with me
- I am a beginner learning agentic AI engineering by building this project.
- Explain concepts before writing code. Prefer hints over full solutions.
- Let me write the code; review it and point out mistakes.
- Never use real bank data; synthetic data only.
- When asking questions, create question file inside the questions folder D:\FinPal\Questions . Maintain one folder per phase and, inside it, one file per session.
- Questions, my answers and your reviews all live in that same session file. Within the file the order is: Questions, then "Answers, attempt 1", "Review 1", "Answers, attempt 2", "Review 2", and so on. I add each new attempt below the last review; you append each review below my latest attempt and never edit my answers.
