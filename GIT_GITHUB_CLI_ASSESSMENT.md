# Git & GitHub CLI Practical Assessment

**For:** AWS-SBG Tech Team  
**Goal:** Prove you can use Git from the terminal to manage history, recover from mistakes, collaborate through GitHub, and contribute to open source.

## Rules

- Use the **Git CLI in a terminal**. Do not use GitHub Desktop.
- Do not commit directly to `main`; use branches and Pull Requests.
- Perform history-rewriting and reset exercises on your own practice branch, never on shared `main`.
- Do not commit passwords, tokens, API keys, or other real secrets.
- Use clear commit messages and keep each change focused.

## Practical tasks

### 1. Inspect the repository and its history
Clone the repository and inspect the remotes, current branch, working tree, upstream tracking branch, recent commits, and branch graph. Identify which branch is safe to work on and explain the difference between `fetch` and `pull`.

### 2. Complete a feature through a Pull Request
Create a feature branch, make a small useful change, commit it, and push it with upstream tracking. Open a PR with a clear summary and test notes. Review a teammate's PR, respond to feedback, update your own PR, and keep `main` unchanged until approval.

### 3. Cherry-pick one specific commit
Create a small commit on a separate branch and apply **only that commit** to another branch with `git cherry-pick`. Show the resulting history and explain why cherry-picking differs from merging the source branch.

### 4. Move to a specific repository state
Check out a supplied commit SHA or tag and identify whether HEAD is detached. Create a branch from that historical point, make a change, then return to the latest branch without losing the work. Demonstrate how you verified the final state.

### 5. Rewrite local work safely
On a disposable branch, create two small commits and combine them into one clean commit using `git reset --soft` or interactive rebase. Explain what `--soft`, `--mixed`, and `--hard` preserve or discard. Do not run a destructive reset on shared history.

### 6. Resolve a real merge/rebase conflict
Make overlapping edits on two branches. Integrate the changes, resolve the conflict without blindly accepting one side, run a check or test, and complete the merge or rebase. Include the final diff in your PR.

### 7. Diagnose common push and tracking errors
Reproduce or diagnose a non-fast-forward rejection and a missing-upstream / incorrect-branch push error. Fix them using the appropriate remote and tracking commands. Do not force-push over another contributor's work.

### 8. Undo and recover mistakes
- Undo a committed change that has already been shared using `git revert`.
- Use `git reflog` to locate and recover a commit after a local reset or rebase.
- Restore a staged file without discarding unrelated changes, and restore one file from a known commit.
Show the commands used and verify the recovered files or commits.

### 9. Stop generated files from being tracked
Add an appropriate pattern to `.gitignore`. If a generated file is already tracked, remove it from Git's index while keeping the local file. Verify the change with `git status` and a diff.

### 10. Make an open-source contribution
Choose a genuine, suitable issue in an active open-source project. Read its contribution guidelines and relevant code before editing. Fork the repository, clone your fork, create a focused branch, make a useful fix or documentation/test improvement, run the relevant checks, and open a PR against the original project. Link the issue where appropriate and describe what you tested. Do not submit meaningless changes or duplicate an existing PR.

## Submission

Send your **repository URL** and the links to your feature PR and open-source PR. Include a short note listing the key commands used for cherry-pick, history recovery, and conflict resolution. If an open-source maintainer has not reviewed the PR yet, submit the open PR link; acceptance is not required for the assessment.

## What will be evaluated

Correctness, safe handling of history, ability to diagnose errors, readable commits, quality of conflict resolution, PR communication, and the usefulness of the open-source contribution.
