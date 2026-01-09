# Git Commands Plugin

Git-related automation commands for Claude Code.

## Commands

### `/commit`, `/commit+`, `/commit++`

Generate git commit messages based on your staged changes. Three variants with different model tiers for varying levels of detail.

| Command | Model | Output |
|---------|-------|--------|
| `/commit` | Haiku 4.5 | Single-line commit subject |
| `/commit+` | Sonnet 4.5 | Detailed commit message |
| `/commit++` | Opus 4.5 | Comprehensive commit message |

**What it does:**
1. Reads current git status
2. Analyzes staged changes diff
3. Reviews current branch and recent commits for context
4. Generates an appropriate commit message

**Usage:**
```bash
/commit
/commit+
/commit++
```

**Example workflow:**
```bash
# Stage your changes
git add -p

# Generate a commit message
/commit

# Claude will analyze your staged changes and output a commit message
```

### `/pr`

Generate a pull request title and description for your current branch.

**What it does:**
1. Identifies the correct base branch (usually `main` or `master`)
2. Analyzes the diff between your branch and the base
3. Generates a PR title and description in a copyable markdown block

**Usage:**
```bash
/pr
```

**Example workflow:**
```bash
# After committing your changes
/pr

# Claude will output a markdown block with PR title and body ready to copy
```
