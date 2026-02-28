# Smart AI Skills

A collection of AI agent skills for software development workflows. It's based on the skills at https://github.com/obra/superpowers, but with some modifications and additions (eg: separate coding skill).

## Skills Overview

| Skill | Description |
|-------|-------------|
| [brainstorming](./skills/brainstorming/SKILL.md) | Explore ideas and turn them into detailed specs through collaborative dialogue |
| [coding](./skills/coding/SKILL.md) | General coding best practices (DRY, KISS, SOLID, TDD) |
| [task-breakdown](./skills/task-breakdown/SKILL.md) | Break down specs into detailed, executable tasks |
| [subagent-task-execution](./skills/subagent-task-execution/SKILL.md) | Execute task breakdowns using specialized subagents |
| [reflection](./skills/reflection/SKILL.md) | Analyze interactions to improve skills and capture user preferences |
| [skill-editor](./skills/skill-editor/SKILL.md) | Create and manage new agent skills |

## Workflow

```
User Request → Brainstorming → Task Breakdown → Execution (via Subagents)
                                        ↓
                              Reflection (periodic)
```

1. **Brainstorming**: Clarify requirements and create specs
2. **Task Breakdown**: Convert specs into bite-sized tasks
3. **Subagent Task Execution**: Execute tasks with review loops
4. **Reflection**: Continuously improve based on experience

## Usage

These skills are designed for use with the opencode CLI. They are automatically loaded when needed based on the task context.

## Directory Structure

```
skills/
├── brainstorming/SKILL.md
├── coding/SKILL.md
├── task-breakdown/SKILL.md
├── subagent-task-execution/SKILL.md
├── reflection/SKILL.md
└── skill-editor/SKILL.md
```
