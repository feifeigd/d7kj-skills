---
name: hello-skill
description: Demonstrates Cursor Agent Skill layout for the d7kj-skills repository. Use when validating skill loading, onboarding skill authors, or copying a minimal SKILL.md template.
# 默认只在用户点名或明确关联时加载，避免无关对话占上下文
disable-model-invocation: true
---

# Hello Skill（演示）

## Purpose

Reference layout for Agent Skills in this repo: required YAML frontmatter plus concise agent instructions.

## Instructions

When this skill is loaded:

1. Briefly confirm it is the **hello-skill** demo and that skills here use directory `hello-skill/SKILL.md` (or sibling folders per skill).
2. If the user wants a **new skill**, gather: purpose, when it should trigger, output format, and whether it lives in this repo or in a project’s `.cursor/skills/`.
3. When authoring, write `name` (lowercase, hyphens, ≤64 chars) and `description` (third person; include trigger terms so the skill is discoverable). Keep `SKILL.md` body under ~500 lines; move long reference to sibling files one level deep.

## Conventions

| Item | Rule |
|------|------|
| `name` | Letters, digits, hyphens only |
| `description` | Non-empty; describe capabilities and when to use |
| `disable-model-invocation` | Default `true` so the skill loads when explicitly named; omit only if auto-invoke from context is desired |

## Maintainer

Repository: `d7kj-skills`. Contributed by feifeigd.
