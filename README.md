# AI-native SDLC skill

A reusable skill for turning work into inspectable decisions and evidence. It supports an adoption assessment, a planned change, release preparation, and incident follow-up.

Anthropic argues that faster code generation shifts attention toward the surrounding delivery process. Its playbook connects the lifecycle with artifacts and explicit controls. This package implements that idea with a compact workflow and original templates. [Read the source article](https://claude.com/blog/the-ai-native-sdlc-playbook), by Louis Claxton, published August 21, 2026; accessed September 7, 2026.

## Why a skill

The immediate need is reusable instructions. The package uses the standard [Agent Skills format](https://agentskills.io/specification): a `SKILL.md` entry point with supporting resources loaded as needed. An MCP server would make sense for a missing live integration, such as accessing your delivery system. No particular system was specified, so this package has no server, credentials, background process, or runtime dependency.

## Contents

- [Skill instructions](skills/ai-native-sdlc/SKILL.md)
- [Change template](skills/ai-native-sdlc/assets/change.md)
- [Incident template](skills/ai-native-sdlc/assets/incident.md)
- [Automation extension guidance](skills/ai-native-sdlc/references/automation.md)

## Install

Download or clone this repository, then copy the entire `skills/ai-native-sdlc` directory into your agent's personal skills folder:

| Agent | Destination | Invocation |
| --- | --- | --- |
| Codex | `~/.codex/skills/ai-native-sdlc/` | `$ai-native-sdlc` |
| Claude Code | `~/.claude/skills/ai-native-sdlc/` | `/ai-native-sdlc` |

Keep the templates and references alongside `SKILL.md`. Start a new session after installation. The instructions and templates are portable; Codex UI metadata is in `agents/openai.yaml`. Installation does not activate integrations or modify another project's instructions. Claude Code's discovery locations and invocation format are documented in its [skills guide](https://code.claude.com/docs/en/skills).

## Use

Example requests for Codex follow. In Claude Code, start with `/ai-native-sdlc` followed by the same task description.

```text
Use $ai-native-sdlc to assess our delivery workflow. Inspect the repository
and recommend the smallest useful improvement with a measurable trial.
```

```text
Use $ai-native-sdlc to turn this feature idea into a change record and
implementation plan. Stop before changing application code: [idea].
```

```text
Use $ai-native-sdlc to implement the accepted change in [record path]
and record which acceptance criteria you verified.
```

```text
Use $ai-native-sdlc to investigate these incident logs in read-only mode
and write a follow-up record. Mark untested hypotheses: [logs].
```

## Adaptation choices

This is an independent implementation, not an official Anthropic skill. It uses a combined change record by default, supports existing separate artifacts, scales paperwork to the task, and preserves previously granted authorization. These choices are ours. It deliberately leaves operational enforcement to actual systems; written instructions cannot supply it.

No performance improvements or production readiness are claimed. The package needs evaluation against your repositories and policies before organizational rollout.

The format checks and two isolated behavioral trials are recorded in [VALIDATION.md](VALIDATION.md).
