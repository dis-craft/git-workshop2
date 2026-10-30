# Git & GitHub Practical Assessment

**For:** AWS-SBG Tech Team  
**Format:** Hands-on tasks using Git CLI and GitHub  
**Goal:** Demonstrate that you can work safely in a real collaborative repository, diagnose problems, recover work, and contribute to open source.

This is a practical assessment, not a command-memorisation test. Complete the tasks by performing the operations yourself and be prepared to explain the result.

## Rules and setup

- Use **Git CLI in a terminal** for all Git operations. Do not use GitHub Desktop or another Git GUI for the Git tasks.
- Use a dedicated practice repository, disposable branches, and a remote repository you control.
- Do not experiment with destructive commands, history rewriting, or force-pushing on a real project or a shared \`main\` branch.
- Use dummy data only. Never commit passwords, API keys, access tokens, private keys, or real credentials.
- Before changing repository history, inspect \`git status\` and \`git log\`. After each task, verify the result.
- Use clear branch names, meaningful commit messages, and focused Pull Requests.
- GitHub's website may be used for repository settings, Issues, Pull Requests, reviews, Releases, Actions, and security settings.
- Tasks marked **Advanced** or **Rare** are stretch tasks. Complete the Core and Team Workflow tasks first.

## Part 1 — Git foundations

**Objective:** Be comfortable creating repositories, tracking changes, and understanding the state of a working tree.

1. **Create a repository — Core**  
   Create a new local repository with \`git init\`. Add a README, make the first commit, and verify the branch and commit history.

2. **Clone an existing repository — Core**  
   Clone the practice repository into a new directory. Check that the remote is configured and identify the checked-out branch.

3. **Configure your Git identity — Core**  
   Set your name and email locally for the practice repository. Inspect the local and global configuration and explain which value takes precedence.

4. **Inspect repository state — Core**  
   Create, modify, and delete sample files. Use \`git status\` to identify untracked, modified, staged, and deleted files.

5. **Manage remotes — Core**  
   Add a remote named \`origin\`, verify it with \`git remote -v\`, rename a test remote, and remove the test remote. Do not remove the actual \`origin\`.

6. **Stage and commit changes — Core**  
   Make at least two logically separate changes. Stage and commit them separately with descriptive commit messages.

7. **Stage only part of a file — Intermediate**  
   Change two different sections of one file. Use interactive staging (for example, \`git add -p\`) to commit only one section, then commit the remaining section separately.

8. **Inspect differences — Core**  
   Make both staged and unstaged changes. Show the difference between \`git diff\` and \`git diff --staged\`, then explain what each output represents.

9. **Move and remove tracked files — Core**  
   Rename or move a tracked file with Git, remove another tracked file, and verify the changes before committing.

10. **Use .gitignore correctly — Core**  
    Ignore a generated folder and a local configuration file. Then take a file that is already tracked, add a matching ignore rule, and stop tracking it without deleting your local copy.

11. **Manage branches — Core**  
    Create a branch, switch between branches, create-and-switch in one command, rename a branch, and safely delete an obsolete local branch.

12. **Read commit history — Core**  
    Use \`git log\`, \`git log --oneline --graph --all\`, \`git show\`, and \`git blame\` to inspect commits and identify who last changed a particular line.

13. **Create and inspect tags — Core**  
    Create a lightweight tag and an annotated version tag. List the tags, inspect the annotated tag, and push a tag to the remote.

14. **Inspect an exact repository state — Intermediate**  
    Check out a known commit or tag and identify the detached-HEAD state. Return to the intended branch without losing any work.

## Part 2 — Everyday collaboration with Git and GitHub

**Objective:** Work with branches, remotes, Pull Requests, Issues, and teammates.

15. **Publish a feature branch — Core**  
    Create a feature branch, make a commit, push it using \`git push -u origin <branch>\`, and verify its upstream tracking information.

16. **Compare fetch, pull, and pull --rebase — Intermediate**  
    Make a remote change from another clone or through GitHub. Use \`git fetch\` first and inspect what changed. Then demonstrate a normal pull and a pull with rebase in a disposable branch or clone.

17. **Merge a feature branch — Core**  
    Create a feature branch with at least one commit, update the base branch, merge the feature branch, and inspect the resulting commit graph.

18. **Temporarily put work aside — Intermediate**  
    Make uncommitted changes, use \`git stash\`, switch to another task, and restore the changes. Demonstrate the difference between \`git stash apply\` and \`git stash pop\`.

19. **Open a useful Pull Request — Core**  
    Push a feature branch and open a PR against the correct base branch. Include the purpose, summary of changes, testing performed, and a link to the related Issue.

20. **Create a Draft Pull Request — Intermediate**  
    Open a draft PR for work that is not ready for review. Add a clear checklist of what remains, then mark it ready for review when complete.

21. **Review and update a Pull Request — Core**  
    Review a teammate's PR. Leave a specific, constructive comment or request a change. Update your own PR in response to review feedback and explain what changed.

22. **Use Issues and labels — Core**  
    Create a bug or feature Issue with reproduction steps or acceptance criteria. Add suitable labels, assign an owner, and close it only after the work is verified.

23. **Create contribution templates — Intermediate**  
    Add an Issue template and a Pull Request template under \`.github/\`. Verify that GitHub offers the templates when creating a new Issue or PR.

24. **Organise work with Projects and milestones — Intermediate**  
    Create a small GitHub Project board, add a few Issues, move them across status columns, and group related work under a milestone.

25. **Contribute through a fork — Core**  
    Fork a repository, clone your fork, add the original repository as \`upstream\`, fetch from it, and explain the difference between \`origin\` and \`upstream\`.

26. **Resolve a normal merge conflict — Intermediate**  
    Make two branches change the same lines. Merge them, resolve the conflict, remove all conflict markers, test the result, and complete the merge.

27. **Apply one commit with cherry-pick — Intermediate**  
    Create two commits on one branch. Apply only the chosen commit to another branch with \`git cherry-pick\`, then verify that unrelated changes were not brought over.

28. **Undo a shared change with revert — Intermediate**  
    Revert a commit that has already been pushed to the practice remote. Verify that the undo is recorded as a new commit rather than silently rewriting shared history.

29. **Publish a Release — Intermediate**  
    Create and push an annotated version tag such as \`v1.0.0\`. Create a GitHub Release using that tag and write concise release notes.

30. **Clean up local and remote branches — Core**  
    Delete a merged local branch and a merged remote branch. Confirm the current branch and remote branch name before deleting anything.

## Part 3 — Troubleshooting and safe recovery

**Objective:** Diagnose the cause of a problem before choosing a fix. Use disposable repositories or branches for tasks involving history changes.

For each task, record the symptom, the cause, the command or procedure used, and how you verified the final state.

31. **Fix a non-fast-forward push — Intermediate**  
    Create a remote commit that your local branch does not contain. Attempt a push, inspect the rejection, integrate the remote change safely, and push again.

32. **Configure a missing upstream — Core**  
    Create a local branch without tracking information. Set the correct upstream and verify it using \`git branch -vv\`.

33. **Handle an operation already in progress — Intermediate**  
    Start a merge or rebase that produces a conflict. Identify which operation is in progress, then either finish it or deliberately abort it.

34. **Recover from detached HEAD — Intermediate**  
    Make a useful commit while in detached HEAD. Preserve it on a new branch and verify that the commit remains accessible.

35. **Move a commit made on the wrong branch — Intermediate**  
    Make a local commit on the wrong feature branch. Move or apply it to the intended branch and leave both branches in a sensible state. Explain how the approach changes if the commit was already shared.

36. **Recover a commit with reflog — Advanced**  
    In a disposable repository, create a commit and make it unreachable from the current branch using a reset. Use \`git reflog\` to locate it and restore it on a recovery branch.

37. **Find a bug-introducing commit with bisect — Advanced**  
    Create a short sequence of commits where one introduces a known failure. Use \`git bisect\` with good and bad points to identify the first bad commit, then reset the bisect session.

38. **Choose the correct reset mode — Advanced**  
    In a disposable branch, demonstrate \`git reset --soft\`, \`--mixed\`, and \`--hard\`. Before and after each operation, inspect the commit, staging area, and working tree. Never run this exercise on shared work.

39. **Rewrite local commits with interactive rebase — Advanced**  
    Create several local commits. Use \`git rebase -i\` to reorder, reword, squash, or drop commits. Explain why rewriting commits that others already use can disrupt collaboration.

40. **Move a range of commits with rebase --onto — Rare**  
    Create a branch with a base and a few commits. Use \`git rebase --onto\` to move only the intended commit range to a different base. Verify the resulting graph.

41. **Compare two versions of a commit series — Rare**  
    Create one version of a feature branch, amend or reorganise it, and use \`git range-diff\` to compare the old and new commit series.

42. **Use force-with-lease safely — Advanced**  
    In a disposable remote branch, rewrite local history and demonstrate \`git push --force-with-lease\`. Explain what it checks and why it is safer than \`git push --force\`. Never force-push shared \`main\`.

43. **Reuse conflict resolutions with rerere — Rare**  
    Enable \`rerere\` in a practice repository, resolve a conflict, recreate the same conflict, and show how Git can reuse the recorded resolution.

44. **Work on multiple branches with worktrees — Rare**  
    Create a second working tree for another branch using \`git worktree\`. Make separate changes in each working directory and list and remove the extra worktree safely.

45. **Use a submodule — Rare**  
    Add a small repository as a submodule. Clone the parent repository elsewhere, initialise and update the submodule, and explain what the parent repository records.

46. **Use a subtree — Rare**  
    Add a small external repository using \`git subtree\`. Demonstrate how its content is integrated and explain one difference between a subtree and a submodule.

47. **Check out only selected directories — Rare**  
    Use sparse checkout to work with only selected paths in a larger practice repository. Show how to change the selected paths.

48. **Use a partial clone — Rare**  
    Clone a suitable practice repository with \`--filter=blob:none\`. Inspect the clone and explain why Git may download file contents later when they are needed.

49. **Transfer a repository without a server — Rare**  
    Create a Git bundle, clone from the bundle into another directory, and verify that the expected history and refs are present.

50. **Check repository integrity — Rare**  
    Run \`git fsck\` on a practice repository and explain the output. Inspect what \`git gc\` does; do not manually delete Git object files.

51. **Export a tracked snapshot — Rare**  
    Use \`git archive\` to export a commit or tag without the repository's Git history. Inspect the exported files.

52. **Understand replace references — Rare**  
    In a disposable repository, use \`git replace\` to substitute an object for inspection, then remove the replace reference and verify the original history is unchanged.

53. **Rewrite repository history safely — Rare**  
    Use \`git filter-repo\` on a disposable clone to remove a dummy file or dummy secret from history. Explain why history rewriting requires coordination and why rotating a real leaked credential is still necessary.

54. **Create and run a Git hook — Advanced**  
    Add a local pre-commit hook that checks a simple rule, trigger it, and then correct the failure. Explain why local hooks are not a substitute for server-side checks.

55. **Configure file-specific Git behaviour — Rare**  
    Add a \`.gitattributes\` rule for line endings or a sample file type. Inspect how Git treats the file and explain when custom diff or merge behaviour is useful.

## Part 4 — GitHub administration, automation, and deployment

**Objective:** Configure a repository for a team and understand the platform features used to maintain it.

56. **Manage repository access — Core**  
    Add a test collaborator or inspect an existing collaborator's permission. Explain the difference between read, triage, write, maintain, and admin access.

57. **Protect the default branch — Intermediate**  
    Configure a branch protection rule or repository ruleset for the practice repository. Require a Pull Request and prevent ordinary direct pushes to the protected branch.

58. **Require reviews and checks — Intermediate**  
    Configure the protected branch to require at least one approval and a status check. Demonstrate that an unapproved or failing PR cannot be merged.

59. **Assign code ownership — Intermediate**  
    Add a \`CODEOWNERS\` file with sample paths and reviewers. Open a PR touching one of those paths and verify the review request behaviour.

60. **Understand merge strategies — Intermediate**  
    Use a practice PR to compare merge commit, squash merge, and rebase merge. Explain how each affects the branch history.

61. **Use a merge queue — Rare**  
    If the repository plan and settings support it, enable a merge queue and submit a practice PR. Explain how it validates changes against the latest target branch. If unavailable, document the limitation and explain the purpose.

62. **Create a GitHub Actions workflow — Intermediate**  
    Add a workflow under \`.github/workflows/\` that checks out the repository and runs a simple validation command. Confirm that it runs successfully.

63. **Configure workflow triggers — Intermediate**  
    Configure separate or combined triggers for \`push\`, \`pull_request\`, and \`workflow_dispatch\`. Trigger each one and inspect the run history.

64. **Use jobs, steps, and runners — Intermediate**  
    Create a workflow with multiple steps and at least two dependent jobs. Inspect the job and step logs and explain the runner environment.

65. **Store workflow artifacts and cache dependencies — Advanced**  
    Make a workflow generate a small build artifact and upload it. Add dependency caching to a suitable sample workflow and explain the difference between an artifact and a cache.

66. **Use Actions secrets and variables — Intermediate**  
    Add a harmless test value as a repository secret and another as a variable. Reference them in a workflow without printing the secret. Remove the test values after verifying the workflow.

67. **Reuse a workflow — Advanced**  
    Create a reusable workflow and call it from another workflow. Pass an input and demonstrate how reusable workflows reduce repeated configuration.

68. **Understand self-hosted runners — Rare**  
    Research the requirements and security implications of a self-hosted runner. If a safe test machine is available, register a temporary runner, run a harmless workflow, then remove the runner.

69. **Understand OIDC authentication — Rare**  
    Explain how a workflow can use OIDC to obtain short-lived credentials from a supported cloud provider instead of storing a long-lived cloud key. Do not create or expose production credentials for this task.

70. **Publish a site with GitHub Pages — Core**  
    Enable Pages for the practice repository. Deploy a simple static site from a branch or through GitHub Actions and verify the published URL.

71. **Configure a custom Pages domain — Intermediate**  
    On a domain you control, configure the required DNS records, add the custom domain in Pages settings, verify it, and enable HTTPS. Do not change DNS for a domain you do not own.

72. **Track large files with Git LFS — Intermediate**  
    Configure Git LFS for a suitable sample file type, track a dummy large file, commit and push it, then verify that the file is managed by LFS.

73. **Publish a package — Advanced**  
    Publish a small sample package to GitHub Packages, inspect its version and visibility, and document how another developer would install it.

74. **Review dependencies and Dependabot — Intermediate**  
    Inspect the dependency graph of a sample repository. Enable or review Dependabot alerts and explain how a dependency update PR should be tested.

75. **Enable secret scanning and push protection — Advanced**  
    Inspect the repository's security settings. Enable secret scanning or push protection where available. Use only a documented dummy test pattern; never create or push a real credential.

76. **Understand security advisories — Advanced**  
    Inspect how a repository security advisory is created and handled. Explain the difference between privately coordinating a vulnerability fix and publishing a public advisory.

77. **Authenticate with SSH and HTTPS — Core**  
    Configure SSH authentication for GitHub and verify the connection. Also explain HTTPS authentication using a credential manager or Personal Access Token. Never paste a token into the repository or assessment submission.

78. **Use fine-grained Personal Access Tokens — Intermediate**  
    Create a temporary fine-grained token with the minimum required repository and permission scope. Use it for a harmless task, then revoke it.

79. **Sign and verify commits — Advanced**  
    Configure SSH or GPG commit signing in a practice repository. Create a signed commit and verify its signature status on the command line and, where available, on GitHub.

80. **Understand deploy keys — Advanced**  
    Explain how a deploy key grants repository-specific SSH access. If you have a safe test server, configure a read-only deploy key and verify that it cannot push.

81. **Understand GitHub Apps and webhooks — Rare**  
    Describe how a GitHub App differs from a Personal Access Token. Inspect a sample webhook event or configure a local test receiver if available; do not expose a public endpoint containing secrets.

82. **Inspect audit logs — Rare**  
    If the account or organisation provides audit logs, locate a recent repository or access-related event. Explain what information an audit log helps an administrator investigate.

## Part 5 — Open-source contribution

83. **Make a genuine contribution to an external project — Core**  
    Find an active open-source project and a suitable issue. Read its contribution guidelines, search for existing fixes or PRs, and inspect the relevant code before editing. Fork the project, clone your fork, add the original as \`upstream\`, and create a focused branch. Make a useful bug fix, documentation improvement, or test addition. Run the relevant checks and open a PR against the original repository. Link the Issue where appropriate and explain what you tested. Do not submit meaningless changes or duplicate an existing PR. The PR does not need to be merged before submission.

## Submission

Submit the following links and evidence:

- Your practice repository URL.
- Your feature branch and Pull Request link.
- The Issue linked to your feature PR.
- Your open-source Pull Request link.
- A short terminal log or notes showing cherry-picking, conflict resolution, and commit recovery.
- The GitHub Actions run link and GitHub Pages URL, if those tasks were completed.
- A brief note describing any advanced task that was unavailable due to account, plan, or repository restrictions.

## Scoring guide

| Area | Points | What good looks like |
|---|---:|---|
| Git foundations | 15 | Correct repository state, staging, commits, branches, tags, and inspection. |
| Everyday collaboration | 20 | Clean remote workflow, useful PRs, reviews, Issues, and fork contributions. |
| Troubleshooting and recovery | 20 | Diagnoses problems first and recovers work without unnecessary data loss. |
| Advanced Git | 15 | Understands history manipulation, recovery, and specialised repository tools. |
| GitHub administration and automation | 20 | Configures permissions, protections, Actions, deployment, and security features. |
| Open-source contribution | 10 | Makes a meaningful, tested contribution and communicates it clearly. |
| **Total** | **100** | |

## Completion checklist

- [ ] Git operations were performed in a terminal, not GitHub Desktop.
- [ ] Tasks involving destructive commands were performed only in disposable repositories or branches.
- [ ] The final working tree is clean and the intended branch is pushed.
- [ ] No real secrets or credentials were committed.
- [ ] The feature PR and open-source PR links are included in the submission.
- [ ] I can explain the commands used, verify the result, and describe the risks before destructive operations.
