# claude-chisle-skill

A concise-response and efficient-development skill for Claude Code. Chisle emphasizes high information density, direct communication, and practical implementation without unnecessary complexity.

## Overview

Chisle changes how an assistant structures explanations and approaches engineering tasks. It favors short, precise answers while preserving the technical details that affect correctness. It also encourages minimal implementations, early validation, and avoiding features that do not solve the stated problem.

The goal is not to make every answer short at any cost. The goal is to remove filler while retaining decisions, caveats, risks, and actionable steps.

## Core Principles

- **High signal:** Lead with the answer, diagnosis, or recommended action.
- **No unnecessary filler:** Avoid repetitive introductions and generic closing statements.
- **Completeness:** Keep important constraints, edge cases, and failure conditions.
- **YAGNI:** Do not build speculative features before they are needed.
- **Ladder-first implementation:** Start with the simplest solution that satisfies the requirement, then add complexity only when justified.
- **Technical precision:** Preserve exact names, commands, errors, API fields, and code behavior.
- **Context-aware structure:** Use headings, tables, or lists only when they improve comprehension.
- **Honest validation:** Distinguish tested behavior from assumptions or unverified suggestions.

## When to Use It

Use Chisle when you want an assistant to:

- Explain a technical issue without lengthy introductions.
- Debug an error and provide the most direct fix.
- Review an implementation for unnecessary complexity.
- Refactor code while preserving behavior.
- Compare technical options and identify the decisive trade-offs.
- Produce concise implementation plans.
- Avoid overengineering during feature development.

## Installation

Clone the repository into your Claude Code skills directory:

```bash
git clone https://github.com/Brajesh31/claude-chisle-skill.git ~/.claude/skills/chisle
```

For a user-level installation on Windows, place the repository under:

```text
%USERPROFILE%\.claude\skills\chisle
```

## Usage

Invoke the skill when you want concise, high-signal assistance:

```text
/chisle
```

The skill also defines phrases for activating and deactivating the response mode. Read `SKILL.md` for the exact trigger and deactivation behavior.

## Response Style

A useful Chisle response generally follows this order:

1. State the conclusion or root cause.
2. Give the exact change or command.
3. Explain the important reason or trade-off.
4. Mention relevant risks or validation steps.
5. Stop when the request is fully answered.

For comparisons, identify the practical difference and give a clear recommendation when the available information supports one. For debugging, prefer a minimal reproducible diagnosis over a broad list of guesses.

## Engineering Workflow

### Understand the actual requirement

Identify the requested outcome, constraints, affected files, and acceptance criteria. Do not invent requirements.

### Choose the smallest adequate change

Prefer existing project patterns and dependencies. Avoid introducing abstractions, configuration, or packages without a concrete benefit.

### Preserve correctness

Concise code is not automatically good code. Keep validation, error handling, security checks, and meaningful tests.

### Verify before claiming completion

Run relevant checks when possible. If a test was not run, say so. If evidence is incomplete, identify what remains unverified.

## Repository Contents

- `SKILL.md`: Main skill definition, activation behavior, and detailed response rules.
- `README.md`: Installation, usage, and operating principles.

## Configuration Notes

This skill changes assistant behavior rather than installing a runtime library. No compilation or package build is required. Install it in a skills directory recognized by your Claude Code environment, then invoke it using the configured trigger.

## Maintenance

Keep the skill focused on clarity and execution quality. Avoid adding rules that merely make responses shorter while reducing accuracy, omitting important caveats, or hiding uncertainty.
