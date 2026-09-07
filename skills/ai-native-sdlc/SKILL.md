---
name: ai-native-sdlc
description: Apply an artifact-based AI-native software delivery workflow. Use when asked to adopt the AI-native SDLC playbook, turn an idea into a delivery plan, resume a documented change, assess release readiness, or turn incident evidence into follow-up work. Ordinary coding questions do not require this workflow.
metadata:
  version: "0.1.0"
---

# AI-native SDLC

## Foundation

Inspired by [Anthropic's playbook](https://claude.com/blog/the-ai-native-sdlc-playbook): connect Plan, Design, Build, Test, Deploy, and Maintain through reviewable artifacts. Capture intent, specify behavior, plan implementation, verify the change, review release evidence, and return operational findings to planning. Keep institutional knowledge versioned and distinguish advisory skills from enforced controls. Preserve human accountability at the organization's decision gates.

The procedures and templates below are an independent implementation, not an Anthropic product or an exhaustive reproduction of its plays.

## Start from the current task

1. Identify the requested outcome and stopping point: adoption assessment, planning only, implementation, release preparation, or incident investigation. Read applicable repository instructions and existing work records before choosing a format.
2. State consequential assumptions. Resolve ambiguity that changes behavior or authorization; continue independent work while answers are pending.
3. Reuse the team's authoritative record. If absent, use `docs/changes/<work-id>/change.md` from [the change template](assets/change.md). Create only sections needed now. A tiny fix may need only a short plan and proof in the task response. Do not generate empty lifecycle documents.
4. For teams using separate documents, map Outcome to `intent.md`, Behavior to `spec.md`, Execution to `plan.md`, and Evidence/Release to their existing PR or release record. Preserve record IDs and source links instead of creating conflicting copies.

## Execute and leave usable evidence

- **Planning:** Make each acceptance criterion observable. Separate supplied facts, inspected evidence, assumptions, and unresolved decisions. Do not invent stakeholders, business baselines, policies, or approvals.
- **Implementation:** Inspect actual files before naming edit locations or commands. Work within the agreed scope. Explain material departures and update the work record. Existing authorization remains valid; this skill does not impose a new approval ceremony.
- **Verification:** Associate each criterion with a result and the revision tested. Use `passed`, `failed`, `not run`, or `blocked`; never turn a planned check into a pass. For a bug, preserve a reproduction and show the behavior before and after where feasible. Explain necessary test changes rather than weakening assertions to hide a failure.
- **Release preparation:** Distinguish implementation completion, verification, release readiness, and actual deployment. Identify unresolved findings and required decisions. Complete authorized preparation before requesting any missing authorization for an external action. Never infer deployment authority from this skill.
- **Incident work:** Use [the incident template](assets/incident.md). Separate symptoms from causal hypotheses. Record the corrective change and the observation needed to establish recovery; a successful command alone does not prove recovery.

If a check fails, investigate and correct within scope. If the same failure persists without new evidence or requires unavailable access, report the specific blocker and completed work; do not retry indefinitely.

## Adoption and automation

For an adoption assessment, inspect one recent change and identify its largest evidenced delay. Propose the smallest intervention, an owner or `unassigned`, a baseline or `unknown`, and a measurable trial. Do not install a full process on the strength of missing documentation alone.

Read [automation guidance](references/automation.md) only when asked about integrations, enforcement, recurring execution, or evaluating agent configuration. This skill contains no running monitor, MCP server, hooks, or CI jobs.

Finish with the outcome, artifact links, verification actually performed, and the next required decision or action. Do not claim commits, approvals, messages, or deployments that tools did not confirm.
