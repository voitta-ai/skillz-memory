# Memory index

One line per memory: `- [slug](slug.md) - hook`. This is the catalog of what
lives in this vault; add a line when you add a memory file.

## Specifics migrated from the skillz catalog (skillz#77)

- [claude-code-claudemd-symlink-write-refused](claude-code-claudemd-symlink-write-refused.md) - Fix Edit/Write 'Refusing to write through symlink' on ~/.claude/CLAUDE.md by resolving the symlink to its real target path.
- [claude-code-el-macos-home-trust-exit1](claude-code-el-macos-home-trust-exit1.md) - Fix M-x claude-code (claude-code.el) dying with "exited abnormally with code 1" at the HOME trust prompt: pre-trust the dir via ~/.claude.json hasTrustDialogAccepted (or launch in a trusted project); plus desktop-save-mode to restore Emacs buffers after reboot.
- [claude-code-piebald-lsp-binary-on-path](claude-code-piebald-lsp-binary-on-path.md) - Piebald LSP plugins surface the LSP tool but the language-server binary isn't on PATH; install and expose the server binary.
- [claude-code-static-allow-bypasses-hook](claude-code-static-allow-bypasses-hook.md) - Why a Claude Code PreToolUse hook never fires for some commands: static permissions.allow Bash globs short-circuit it.
- [emacs-batch-package-verify-pitfalls](emacs-batch-package-verify-pitfalls.md) - Avoid false-negative failures when verifying an Emacs package install with emacs --batch (no ELPA auto-activation on load-path; use-package deferred loading skips :config).
- [gh-api-f-vs-F-body-file](gh-api-f-vs-F-body-file.md) - gh api -F (uppercase) reads @file into the field; -f sends the value as a literal string.
- [gh-api-jq-no-arg](gh-api-jq-no-arg.md) - gh api --jq needs its filter as the argument; a misplaced/empty --jq silently drops the filter.
- [gh-fork-issues-disabled](gh-fork-issues-disabled.md) - gh issue create fails on a fork because GitHub disables the Issues tab on forks by default.
- [gh-git-heredoc-body-file](gh-git-heredoc-body-file.md) - Use a body-file so gh CLI and git stop mangling multi-line bodies with backticks, code blocks, or $(...).
- [gh-pr-graphql-401-rest-fallback](gh-pr-graphql-401-rest-fallback.md) - When gh PR GraphQL calls return 401, fall back to the REST PR endpoints.
- [gh-pr-merge-delete-branch-closes-dependent-pr](gh-pr-merge-delete-branch-closes-dependent-pr.md) - Deleting the branch on gh pr merge can auto-close a dependent PR stacked on it.
- [gh-workflow-run-matching](gh-workflow-run-matching.md) - Match a gh workflow run to its trigger when multiple runs share one workflow name.
- [git-add-u-rename-pitfall](git-add-u-rename-pitfall.md) - git add -u can miss a rename, leaving the old path staged as deleted; stage the new path explicitly.
- [git-branch-cleanup-script-races](git-branch-cleanup-script-races.md) - Branch-cleanup scripts race against concurrent ref updates; snapshot refs before deleting.
- [github-api-list-endpoint-staleness-fresh-pr](github-api-list-endpoint-staleness-fresh-pr.md) - GitHub list endpoints serve stale empty results on a fresh PR; use the timeline / single-resource fetch.
- [github-closing-keywords-default-branch-only](github-closing-keywords-default-branch-only.md) - GitHub closing keywords (Closes #N) only auto-close when the PR merges into the default branch.
- [github-private-repo-readme-image-rendering](github-private-repo-readme-image-rendering.md) - Images in a private-repo README need authenticated or relative paths to render.
- [macos-bash-3.2-compat](macos-bash-3.2-compat.md) - Fix bash scripts that fail on macOS's stock bash 3.2 (declare -A, mapfile, and other bash-4-only constructs).
- [python-symtable-no-col-offset-pairing](python-symtable-no-col-offset-pairing.md) - Pair Python symtable scope entries with AST nodes when symtable exposes no col_offset, via (lineno, name) grouping.
- [s3-presigned-upload-fails-nonexistent-bucket](s3-presigned-upload-fails-nonexistent-bucket.md) - Presigned S3 upload fails because the bucket is wrong/missing; HeadBucket 404-vs-403; CloudFront origin reveals real bucket.
- [vercel-token-deploy-branch-domains](vercel-token-deploy-branch-domains.md) - Token-only per-branch Vercel deploys to fixed custom domains; gitBranch domain pin; preview custom-domain SSO 401.
