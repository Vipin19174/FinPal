# Phase 0: Foundations (weeks 1–3)

Write your answers in `Solutions/`, in your own words.

## Week 1, session 1: terminal, environments, Git

### Check questions

1. What does "working directory" mean?
2. Why do we not commit the virtual environment folder to Git?
3. What is the difference between `git commit` and `git push`?
4. In `git log --oneline`, what do `HEAD`, `main` and `origin/main` each point to?
5. If you make two commits without pushing, which line of `git log --oneline` will `origin/main` appear on?
6. You added `Solutions/` to `.gitignore`. Why did `git status` then show `.gitignore` as modified but not show `Solutions/`?
7. What does `-u` do in `git push -u origin <branch-name>`, and why is it only needed the first time?

### Hands-on tasks

- [ ] Run `test.py` from the terminal and explain what happens for an empty file.
- [ ] Say how the `finpal` environment was created, and show how to tell from the prompt that it is active.
- [ ] Commit the pending `.gitignore` change on `feature/phase1` and push it.
- [ ] Run `git log --oneline` before and after the push and note where `origin/feature/phase1` sits each time.
