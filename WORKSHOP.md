# Thursday Git Workshop Instructions

## Setup checklist

Before the workshop begins, confirm the following:

- Git is installed
- VS Code or Cursor is installed
- GitHub login works
- A terminal is available
- The repository is cloned locally

## Branch naming convention

Use this branch name pattern:

```bash
student-name-feature-branch
```

Example:

```bash
alex-feature-branch
```

## Task 1: Create your feature branch

From `main`, create a branch with your name:

```bash
git checkout main
git checkout -b student-name-feature-branch
```

Then make one small change to `index.html`.

Example change:

- update the second bullet from `Test the workflow` to `Validate the workflow with a demo`

Commit the change:

```bash
git add index.html
git commit -m "Update workflow wording"
```

Push the branch:

```bash
git push -u origin student-name-feature-branch
```

## Task 2: Create the second branch from `main`

This step is important. The second branch should be created from `main`, not from the first branch.

```bash
git checkout main
git checkout -b student-name-conflict-branch
```

Edit the same lines in `index.html` in a different way.

Example change:

- update the second bullet from `Test the workflow` to `Check the workflow in a live review`

Commit and push:

```bash
git add index.html
git commit -m "Adjust workflow language"
git push -u origin student-name-conflict-branch
```

## Task 3: Create the merge conflict

From `main`, merge the second branch:

```bash
git checkout main
git merge student-name-conflict-branch
```

This should create a merge conflict because both branches changed the same lines.

## Task 4: Resolve the conflict

Open the file and edit the conflict markers.

Use the version that preserves the best intent from both changes.

Example final result:

```html
<li>Validate the workflow with a demo and a live review</li>
```

Then:

```bash
git add index.html
git commit -m "Resolve merge conflict in project goals"
```

## Learning goals

By the end of the exercise, students should be able to explain:

- what a branch is
- what a commit is
- why a merge conflict happens
- how to read both versions of a conflict
- how to resolve the conflict into a coherent final result

## Notes

This repository is intentionally simple.

The goal is to practice Git workflows and collaboration, not to build a production application.
