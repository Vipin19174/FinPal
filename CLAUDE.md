# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

FinPal is a personal finance agent for customers of a fictional bank. It uses synthetic data only; never use real bank data.

There is no application code yet. `test.py` is an empty placeholder, not a test suite, and there is no dependency manifest, build, lint, or test setup.

## Planned architecture

The agent is built in layers, each added to the same codebase: a script that generates a synthetic `transactions.json` (date, merchant, amount, category) → hand-written tool-calling loop on Bedrock (`finpal/llm.py`) → Strands agent with tools → FastAPI service and Streamlit UI in Docker → Databricks data and RAG → multi-agent with MCP and human approval → guardrails, MLflow tracing and evals → Kong, personas and AgentCore deployment.

## Environment

- Windows, PowerShell in the VS Code terminal.
- Conda environment `finpal` (Python 3.12) at `C:\Users\vipin\.conda\envs\finpal`; only pip and setuptools are installed so far. Activate with `conda activate finpal`. VS Code (`.vscode/settings.json`) uses conda as environment and package manager, so install packages with conda rather than venv/pip unless told otherwise.
- Conda (`C:\ProgramData\anaconda3`) is not on PATH in non-interactive shells, where plain `python` is the global 3.13. To run something in the project environment from a tool call, use `C:\Users\vipin\.conda\envs\finpal\python.exe` directly.

## Repository conventions

- Work happens on feature branches (e.g. `feature/phase1`) pushed to `origin`, not directly on `main`.
- Git tracks project code only. Several local-only folders and files are gitignored on purpose (see the end of `.gitignore`); never stage or commit them.

## Keeping this file current

Once a dependency manifest (e.g. `environment.yml`), a test runner, a linter, or the agent's module structure is added, record the commands (including how to run a single test) and the high-level architecture in this file.
