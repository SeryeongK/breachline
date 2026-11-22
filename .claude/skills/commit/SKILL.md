---
name: commit
description: Write git commit messages for breachline following Conventional Commits in English. Use whenever creating a commit, splitting changes into commits, or writing a commit message.
---

# Commit convention

Based on [Conventional Commits 1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) and the [Angular commit message guidelines](https://github.com/angular/angular/blob/main/contributing-docs/commit-message-guidelines.md). Types follow `@commitlint/config-conventional`.

## Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

- `type` and `subject` are required. `scope` is optional but preferred.
- Write everything in English.

## Type

| type | use for |
| --- | --- |
| `feat` | a new feature (including a new lab) |
| `fix` | a bug fix |
| `docs` | documentation only (README, ADR, lab guides) |
| `style` | formatting only, no behavior change |
| `refactor` | code change that neither fixes a bug nor adds a feature |
| `perf` | performance improvement |
| `test` | adding or fixing tests |
| `build` | build system or dependencies (Gradle, pip, npm, Dockerfile) |
| `ci` | CI configuration (GitHub Actions) |
| `chore` | maintenance that fits nothing above (repo config, .gitignore) |
| `revert` | revert a previous commit |

## Scope

Use the top-level folder name:

`gateway`, `agent`, `simulator`, `attacker`, `console`, `labs`, `docs`, `infra`

- For a specific lab, use `lab-<n>`, e.g. `feat(lab-2): add command replay attack`.
- Omit the scope when the change spans many modules.

## Subject

- Imperative, present tense: "add", not "added" or "adds"
- Lowercase first letter
- No period at the end
- Header (whole first line) is 72 characters or fewer

## Body

- Explain **why** the change was made and how it differs from before. The diff already shows what changed.
- Wrap lines at 100 characters.
- Skip the body only for trivial changes (typos, formatting).
- When a commit adds **intentionally vulnerable code** for a lab, say so in the body:
  `Intentionally vulnerable. Active only in lab mode.`

## Footer

- Breaking change: `BREAKING CHANGE: <description>` (or `!` after the type/scope, e.g. `feat(gateway)!: ...`)
- Issue reference: `Refs #12`, `Closes #12`
- Do **not** add `Co-Authored-By`, `Claude-Session`, or "Generated with" lines.

## Rules

- One logical change per commit. Split unrelated changes into separate commits.
- Never commit secrets (`.env`, keys, tokens). Check `git diff --staged` before committing.
- Do not commit or push unless the user asks.

## Examples

```
feat(gateway): add role-based access check for device commands

Viewer accounts could call the stop API directly. Commands now require
the operator role, and hazardous commands require two approvals.

Refs #4
```

```
feat(lab-1): add unauthorized control lab

Intentionally vulnerable. Active only in lab mode.
```

```
fix(console): resync missed telemetry after websocket reconnect
```

```
docs(docs): add ADR 0001 for lab mode structure
```

```
chore: add .gitignore and repository skeleton
```
