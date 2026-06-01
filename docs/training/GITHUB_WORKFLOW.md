# GitHub Workflow Training

## Why We Use GitHub

GitHub helps the team track work, review changes, avoid overwriting each other, and keep a history of project decisions.

## Core Terms

- Repository: the project folder stored in GitHub.
- Clone: a copy of the repository on your computer.
- Branch: a separate workspace for your task.
- Commit: a saved change with a message.
- Push: send your commits to GitHub.
- Pull Request: ask for your changes to be reviewed.
- Review: feedback before changes are merged.

## Standard Workflow

1. Read your GitHub issue.
2. Create a branch from the latest main branch.
3. Make focused changes.
4. Test or review your changes.
5. Commit with a clear message.
6. Push your branch.
7. Open a pull request.
8. Respond to review feedback.
9. Wait for mentor approval.

## Basic Commands

```bash
git clone <repo-url>
git status
git checkout -b student/your-name/task-name
git add .
git commit -m "Add clear message"
git push origin student/your-name/task-name
```

## Pull Request Rules

- One pull request should focus on one task.
- Do not mix unrelated work.
- Do not commit secrets.
- Explain what you changed.
- Add screenshots where useful.
- Ask questions in the pull request if needed.
