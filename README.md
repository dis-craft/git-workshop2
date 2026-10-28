# Git & GitHub CLI Practical Assessment

**For:** AWS-SBG Tech Team  
**Focus:** Real workflow, repository state, troubleshooting, recovery, collaboration, and open-source contribution.

This assessment checks whether you can use Git confidently in real projects—not just remember commands.

## Rules and setup

- Use the **Git CLI in a terminal** for all Git operations. Do not use GitHub Desktop or another Git GUI.
- Use a separate practice repository, at least two branches, and a remote repository.
- Never practise `reset --hard`, history rewriting, recovery, or force-pushing on a real project or shared `main`.
- Do not commit passwords, access tokens, API keys, or real secrets.
- Use clear commit messages and be ready to explain what each command changes.
- GitHub's website may be used for repository settings, Issues, Pull Requests, reviews, Releases, and open-source contribution.

## A. Core workflow and repository state

1. **Inspect a repository.** Clone it and identify the current branch, working-tree state, remotes, local/remote branches, recent commits, and tags. Explain the difference between `git fetch` and `git pull`.
2. **Build a clean feature workflow.** Create a feature branch, make two meaningful commits, push it, configure upstream tracking, and verify which remote branch it tracks.
3. **Move to an exact state.** Given a commit hash or tag, check out that exact state. Demonstrate detached HEAD, inspect the target, then return safely to the intended branch without losing work.
4. **Stage selectively.** Change at least two parts of a file, stage only one change, inspect staged and unstaged diffs separately, and commit only the intended change.
5. **Ignore generated files correctly.** Add suitable `.gitignore` patterns for generated output, dependencies, or local configuration. If a matching file is already tracked, stop tracking it while keeping the local copy.

## B. Undoing changes safely

6. **Choose the right undo operation.** Demonstrate the difference between discarding an uncommitted change, un-staging a file, undoing a local commit while keeping its changes, and reverting a commit that has already been shared.
7. **Recover a lost commit.** In the practice repository, create a commit, make it hard to find with a reset, then recover it using Git history/references such as `git reflog`. Verify the restored commit and file.

## C. Branch integration and advanced Git

8. **Cherry-pick a specific commit.** Create a commit on one branch and apply only that commit to another branch without merging the entire source branch. Verify the destination history and file content.
9. **Resolve a cherry-pick conflict.** Make the same lines differ on two branches, cherry-pick the conflicting commit, resolve it, and finish the operation. Explain how to abort if the wrong commit was selected.
10. **Compare merge and rebase.** Integrate a feature branch into an updated main branch. Demonstrate merge and rebase in separate practice branches or disposable copies, then compare the histories.
11. **Stash unfinished work.** Make uncommitted changes, switch tasks without committing, then restore the work. Demonstrate `git stash apply` versus `git stash pop`, including what to do if restoration conflicts.
12. **Resolve a normal merge conflict.** Merge branches that edit the same lines, preserve the intended changes, remove conflict markers, test the result, and complete the merge.
13. **Fix a commit on the wrong branch.** Move an accidental local commit to the correct branch and leave both branches sensible. Explain how the approach changes if the commit was already pushed.
14. **Use Git history tools.** Use `git log`, `git show`, `git diff`, `git blame`, and `git reflog` to identify what changed, who last changed a line, where HEAD pointed before a reset, and which commit introduced a bug.
15. **Clean up branches.** Rename a local branch, delete an obsolete local branch, remove a merged remote branch, and confirm the checked-out branch before deleting anything.

## D. Diagnose common errors

For each scenario, explain the cause, choose the least risky fix, and verify the final state. Do not blindly copy commands from online answers.

| Error or scenario | What you should demonstrate |
|---|---|
| Push rejected / non-fast-forward | Inspect remote changes, integrate them safely, then push again. |
| No upstream branch configured | Set the intended upstream and verify tracking before pushing. |
| Uncommitted changes block checkout | Protect the work by committing, stashing, or safely moving it before switching. |
| Merge or rebase already in progress | Identify the operation; finish it or deliberately abort it. |
| Detached HEAD | Explain why HEAD is detached and preserve useful work on a branch. |
| Pathspec or branch not found | Check spelling, directory, refs, and whether a remote fetch is needed. |
| Cherry-pick or revert conflict | Resolve and continue, or abort if the selected change should not be applied. |
| Ignored file still appears in Git | Check whether it is already tracked; fix the index without deleting needed local data. |
| Accidental reset or deleted commit | Inspect reflog and recover to a new branch before doing anything else. |
| Authentication / permission failure | Check account, remote URL, credentials, and repository access. Never share tokens in chat. |

## E. GitHub collaboration (using Git + GitHub)

16. **Open a useful Pull Request.** Push a feature branch, open a PR against the correct base, describe the change and testing, and link the related Issue. Do not commit directly to `main`.
17. **Review and update.** Review a teammate's PR, identify a genuine issue or improvement, leave a constructive comment, and update your own PR in response to review feedback.
18. **Use the fork workflow.** Fork a repository, clone your fork, add the original repository as an `upstream` remote, fetch its updates, and explain how to sync your branch. Show the `origin` and `upstream` remotes.
19. **Protect shared work.** Explain why force-pushing shared branches is risky. In a disposable branch only, demonstrate a lease-checked force push and explain when it should not be used.
20. **Release a working version.** Create an annotated version tag such as `v1.0.0`, push the tag, and write a short GitHub Release note describing the change.

## F. Open-source contribution

21. **Make a genuine contribution to an external project.** Find a suitable issue in an active open-source repository. Read its contribution guidelines and inspect the relevant code before editing. Fork the repository, clone your fork, create a focused branch, make a useful fix or documentation/test improvement, run the relevant checks, and open a PR against the original project. Link the issue where appropriate and explain what you tested. Do not submit meaningless changes or duplicate an existing PR. A maintainer does not need to merge the PR before the assessment is submitted.

## Submission

Submit:

- Your practice repository URL.
- Your feature Pull Request link and the related Issue.
- Your open-source Pull Request link.
- A short note with the commands/results used for cherry-picking, conflict resolution, and commit recovery.

## Scoring guide (100 points)

| Area | Points | What good looks like |
|---|---:|---|
| Core workflow and repository state | 15 | Correct branches, remotes, selective staging, and exact-state checkout. |
| Undo and recovery | 15 | Chooses safe operations and can recover lost work. |
| Cherry-pick, rebase, merge, and stash | 20 | Handles history and conflicts without losing changes. |
| Troubleshooting | 15 | Diagnoses the cause before applying a fix and verifies the result. |
| GitHub collaboration and releases | 15 | Useful PRs, reviews, Issues, tracking, and release workflow. |
| Open-source contribution | 20 | Follows project guidelines, makes a meaningful change, tests it, and communicates clearly in the PR. |

## Completion checklist

- [ ] All Git commands were run in a terminal, not GitHub Desktop.
- [ ] The final working tree is clean and the intended branch is pushed.
- [ ] No work was lost and no secrets were committed.
- [ ] You can explain each fix, verify it with `status`, `log`, or `diff`, and describe risks before destructive commands.
- [ ] Feature PR and open-source PR links are included in the submission.
