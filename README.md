# git-init.rf

A [reframe](https://github.com/anvie/reframe) **apply-mode** template for setting up git boilerplate in any project.

## What it sets up

- **`.gitignore`** — covers node_modules, .env, build artifacts, IDE/OS files, databases, logs, coverage, caches, large data files
- **`.git/hooks/pre-commit`** — blocks commits containing:
  - Files larger than 1 MB
  - Secrets / API keys / tokens
  - `node_modules/` directory
  - `.env` files (except `.env.example`)

## Usage

```bash
# From any git-tracked project root:
reframe apply https://github.com/anvie/git-init.rf

# Or from a local clone:
reframe apply ./git-init.rf
```

You'll be prompted for your name and email (for git config).

## Apply mode

This template uses `mode = "apply"`, meaning it overlays files directly into the current directory rather than generating a new project.
