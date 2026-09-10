# CS 450 Git Practice

This is a simple public practice repository for the Week 1 Thursday Git workshop.

## Goal

Practice the core Git workflow:

- clone a repository
- create a feature branch
- make a small change
- commit the change
- push the branch
- create a second branch from `main`
- create a merge conflict
- resolve the conflict
- explain what happened

## Branch naming convention

Use this naming pattern for your branch:

```bash
student-name-feature-branch
```

Example:

```bash
alex-feature-branch
```

## Exercise

Open `index.html` and update the project goals list.

The class will create two separate branches from `main` and make different edits to the same lines. This will intentionally create a merge conflict that must be resolved.

## Suggested workflow

```bash
git clone <repo-url>
cd cs-450-git-practice
git checkout -b student-name-feature-branch
# edit index.html
# save changes
git add index.html
git commit -m "Update project goals"
git push -u origin student-name-feature-branch
```

Then:

```bash
git checkout main
git checkout -b student-name-conflict-branch
# edit the same lines in index.html differently
git add index.html
git commit -m "Adjust project goal wording"
git push -u origin student-name-conflict-branch
```

Then merge into `main` and resolve the conflict.

## Notes

- This repository is intentionally simple.
- It is not the course project app.
- It exists only to practice Git collaboration.
- The goal is to understand conflict resolution, not to build a production application.
