---
name: plan
description: Plan-only feature planning and documentation. Use when the user asks to plan a feature, create a plan, or produce a planning document without implementing changes. The skill reads the repo for context, asks clarifying questions to remove ambiguity, and writes a single plan markdown file named plan-SLUG.md in the project root; no other files may be created or modified.
---

# Plan

## Overview

Create a plan document only. Do not implement. Read the repo for context, ask clarifying questions until there are no ambiguities, then write a single markdown file in the project root named `plan-SLUG.md`. This plan file is the only file that may be created or edited.

## Workflow

1. **Understand the project**
   - Read relevant files (README, docs, architecture notes, configs, and feature-adjacent code).
   - Use `rg` to locate related symbols, routes, or feature flags.
   - Do not edit any files during exploration.

2. **Ask clarifying questions**
   - Ask only what is needed to remove ambiguity before writing the plan.
   - If the user provides partial answers, follow up until requirements are clear.
   - Confirm or propose the plan file name (kebab-case) based on the feature.

3. **Write the plan**
   - Create or update a single file in the project root named `plan-SLUG.md`.
   - Do not modify or create any other files.
   - Keep the plan concrete, scoped, and free of implementation details that change code.

## Plan File Requirements

The plan must include these sections (in this order):

1. **Title** (short, descriptive)
2. **Goal**
3. **Scope** (include explicit non-goals)
4. **Assumptions / Constraints**
5. **Decisions & Rationale** (required)
6. **Proposed Approach** (high-level steps, no code changes)
7. **Risks & Mitigations**
8. **Open Questions** (required; track unresolved items)

If relevant, add optional sections such as **Data/Interfaces**, **Testing/Validation**, or **Rollout** after Proposed Approach.

## Guardrails

- Only create or edit the plan file in the project root.
- If asked to implement or modify other files, explain the constraint and offer to proceed with planning only.
- Keep the plan readable and reviewable without referring back to the terminal.
