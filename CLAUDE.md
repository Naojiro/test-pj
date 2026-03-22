# CLAUDE.md

This file provides guidance for AI assistants (Claude and others) working in this repository.

## Repository Overview

> **Note:** This repository is in its initial state. Update this section as the project evolves.

- **Project name:** test-pj
- **Owner:** Naojiro
- **Remote:** `http://local_proxy@127.0.0.1:35685/git/Naojiro/test-pj`

## Git Workflow

### Branch Naming

- Feature branches for Claude sessions: `claude/<description>-<session-id>`
- Always develop on the branch specified at the start of each session.
- Never push to `main` or `master` without explicit permission.

### Commit and Push

```bash
# Stage specific files (never use git add -A blindly)
git add <file1> <file2>

# Commit with a descriptive message
git commit -m "Short imperative summary

Optional longer explanation if needed."

# Push and set upstream tracking
git push -u origin <branch-name>
```

- Write commit messages in the imperative mood ("Add feature" not "Added feature").
- Keep the subject line under 72 characters.
- Reference issue/PR numbers where relevant (e.g., `Closes #42`).

### Pull Requests

- Keep PRs focused on a single concern.
- Fill out the PR description with a summary and test plan.
- Do not force-push to shared branches.

## Development Setup

> **TODO:** Fill in once the project stack is established.

```bash
# Install dependencies (update with actual package manager)
# npm install | yarn install | pip install -r requirements.txt | ...

# Run the project
# npm run dev | python main.py | ...
```

## Testing

> **TODO:** Fill in once a test framework is chosen.

```bash
# Run all tests
# npm test | pytest | go test ./... | ...

# Run a single test file
# npm test -- <file> | pytest <file> | ...
```

- Always run the full test suite before pushing.
- Do not commit code that breaks existing tests.
- Write tests for new functionality.

## Linting and Formatting

> **TODO:** Fill in once linting tools are configured.

```bash
# Lint
# npm run lint | flake8 . | golangci-lint run | ...

# Format
# npm run format | black . | gofmt -w . | ...
```

- Resolve all lint errors before committing.
- Do not disable lint rules without a comment explaining why.

## Code Conventions

### General

- Prefer clarity over cleverness.
- Keep functions small and focused on a single responsibility.
- Avoid over-engineering: build only what is needed now.
- Delete dead code rather than commenting it out.
- Do not add docstrings, comments, or type annotations to code you did not change.

### Security

- Never commit secrets, API keys, or credentials.
- Validate input at system boundaries (user input, external APIs); trust internal code.
- Avoid introducing OWASP Top 10 vulnerabilities (SQLi, XSS, command injection, etc.).

### Dependencies

- Prefer well-maintained, minimal dependencies.
- Pin versions for reproducible builds.
- Review transitive dependencies before adding new packages.

## File Structure

> **TODO:** Document the directory layout once source code is added.

```
test-pj/
├── CLAUDE.md          # This file
└── ...                # Add project structure here
```

## CI/CD

> **TODO:** Document CI/CD pipelines once configured (GitHub Actions, GitLab CI, etc.).

## Environment Variables

> **TODO:** List required environment variables and their purpose here.

| Variable | Required | Description |
|----------|----------|-------------|
| _(none yet)_ | — | — |

## Common Tasks

> **TODO:** Add frequently used commands and workflows as the project grows.

## Updating This File

Keep this file up to date as the project evolves:
- Add the tech stack and directory structure once established.
- Fill in test, lint, and format commands when tooling is configured.
- Document any non-obvious conventions or architectural decisions.
