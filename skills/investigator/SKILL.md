---
name: investigator
description: Use this skill when the user asks to "analyze", "research", "how do I", or "what's the best way" to understand project context, impact of potential actions, and root causes of issues.
---

# Investigator Skill

## Overview
The Investigator skill is used to gather deep context and perform rigorous analysis before any action is taken. It ensures that the agent understands the current state of the project, the broader implications of any proposed changes, and the fundamental reasons for any issues.

## When to Use
You MUST use this skill when the user mentions:
- "analyze"
- "research"
- "how do I"
- "what's the best way"
- Any request requiring deep understanding of the project's current state or history.

## Instructions

### 1. Analyze Project Context
Gather all relevant information to understand the current environment:
- **Project Structure:** List files in the root directory to identify the project's purpose, tools, and organization.
- **Project Documentation:** Read key files such as `README.md`, `CONTRIBUTING.md`, or any project-specific guidelines (e.g., `AGENT.md`, `CLAUDE.md`).
- **Recent Activity:** Review recent history (e.g., `git log -n 5` for coding projects or recent document updates) to understand what has changed recently.

### 2. Impact & Relationship Mapping
Understand how components relate and how potential actions might propagate:
- **Identify Relationships:** Map out how different parts of the project (files, docs, scripts, data) are interconnected.
- **Predict Consequences:** Before proposing an action, identify what other parts of the project might be affected. Use search tools to find references and dependencies.
- **Constraint Identification:** Look for existing patterns, rules, or constraints that must be respected in any future action.

### 3. Root Cause Investigation
When investigating an issue or unexpected behavior:
- **Consistent Reproduction:** Identify the exact conditions or steps required to reproduce the issue.
- **Deep Analysis:** Look past the immediate symptoms. Trace the problem back to its origin by examining logs, data flows, and configuration.
- **Component Boundaries:** Analyze the interactions between different parts of the system to see where the breakdown occurs.
- **Outcome:** Provide a clear explanation of the root cause and the evidence supporting it. Do NOT make any changes or propose fixes as part of this skill.

## Examples

### Scenario: User asks "How do I add a new API endpoint?"
1. **Context:** Analyze `package.json` to see the framework (Express) and `README.md` for endpoint conventions.
2. **Mapping:** Search the codebase for existing endpoints to understand the routing structure and where middleware is applied.
3. **Report:** Present the current pattern and the files that would be impacted.

### Scenario: User says "Analyze why the build is failing"
1. **Context:** Read the last few lines of the build log and check `git log` for recent changes to the build config.
2. **RCA:** Trace the error in the log back to a specific missing environment variable in the CI configuration.
3. **Report:** Identify the specific root cause (missing ENV var) and explain why it's causing the failure.
