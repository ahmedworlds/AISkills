---
name: rescueai
description: Adaptive AI conversation memory, alignment, optimization, and recovery workflow using MEMORY.md and rescueai align, rescueai optimize, and rescueai recover commands.
---

# RESCUEAI v1.0
## Adaptive AI Conversation Memory and Recovery Skill

Version: 1.0.0
Status: Initial release

## 1. PURPOSE

rescueai is a lightweight, adaptive AI conversation memory and recovery Skill.

Its purpose is to help an AI assistant:

- Remember the user's real objectives.
- Recognize evolving user intentions.
- Maintain alignment with the latest confirmed requirements.
- Reduce unnecessary working-memory content.
- Identify contradictions and unsupported claims.
- Recover conversations that have lost direction.
- Preserve important decisions and project progress.
- Minimize unnecessary repetition and token consumption.

rescueai provides instructions and workflows. The AI assistant performs all reasoning.

rescueai does not require a separate AI model, external API, database or backend.

## 2. OPERATING PRINCIPLES

Always follow these principles:

1. The user's latest confirmed intention takes priority.
2. Never silently change significant user requirements.
3. Distinguish confirmed decisions from suggestions.
4. Preserve important historical information.
5. Ask only when clarification is genuinely necessary.
6. Ask one question at a time.
7. Keep responses concise and practical.
8. Never claim to have modified a file unless that action actually occurred.
9. Never claim to have deleted previous conversation messages.
10. Treat MEMORY.md as user-controlled persistent memory.

## 3. MEMORY MODEL

The persistent memory file is named:

MEMORY.md

Use the following information categories:

- Original Objective
- Current Objective
- User Preferences
- Confirmed Decisions
- Constraints
- Completed Work
- Current Task
- Next Step
- Unresolved Questions
- Important History

### Memory classification

Classify information as follows:

CONFIRMED
Explicitly approved or stated by the user.

PROPOSED
Suggested by the AI but not approved.

TEMPORARY
An idea, possibility or exploratory suggestion.

REJECTED
A suggestion explicitly declined by the user.

HISTORICAL
A previous decision or requirement that remains useful for context.

SUPERSEDED
A previous requirement replaced by a newer confirmed requirement.

Never promote PROPOSED or TEMPORARY information to CONFIRMED without user approval.

### Adaptive memory rules

When objectives change:

1. Identify the new intention.
2. Determine whether it is exploratory or confirmed.
3. Compare it with the current objective.
4. If confirmed, prioritize the new objective.
5. Preserve useful historical context.
6. Mark replaced requirements as SUPERSEDED where useful.
7. If the change is ambiguous and materially important, ask one question.

Do not interpret every new suggestion as a permanent change.

## 4. COMMAND: RESCUEAI ALIGN

Trigger: rescueai align

Purpose:
Restore alignment with the latest confirmed user objective.

### Procedure

1. Retrieve the latest available MEMORY.md.
2. Identify the current confirmed objective.
3. Identify important preferences and constraints.
4. Compare the current conversation with those requirements.
5. Identify relevant drift, contradictions or outdated assumptions.
6. Distinguish confirmed requirements from temporary suggestions.
7. Restore focus without changing requirements.

### Response format

RESCUEAI ALIGN

Current objective:
[Latest confirmed objective]

Important requirements:
[Relevant constraints and decisions]

Alignment assessment:
[Aligned / Minor drift / Significant drift]

Issues identified:
[Only relevant issues]

Recommended next step:
[One practical action]

If there is no meaningful drift, say so. Do not invent problems.

Do not rewrite MEMORY.md during align unless the user explicitly requests a memory update.

## 5. COMMAND: RESCUEAI OPTIMIZE

Trigger: rescueai optimize

Purpose:
Reduce unnecessary memory while preserving useful information.

### Procedure

1. Read the available MEMORY.md.
2. Identify duplicate information.
3. Identify outdated or superseded requirements.
4. Identify settled debates and rejected suggestions.
5. Identify unnecessary historical detail.
6. Preserve objectives, decisions, constraints and progress.
7. Preserve unresolved questions.
8. Prepare a compact proposed replacement.
9. Compare the proposed replacement with the original.
10. Ask the user for approval.

### Information that must be protected

Never remove or weaken:

- The latest confirmed objective.
- Important user preferences.
- Active project requirements.
- Confirmed decisions.
- Important constraints.
- Completed milestones.
- Current task and next step.
- Unresolved important questions.
- Historical decisions needed to understand current requirements.

### Approval procedure

Present:

1. What will be preserved.
2. What will be added.
3. What will be updated.
4. What will be removed or condensed.
5. The complete proposed MEMORY.md.

Then ask:

"Do you approve replacing your current MEMORY.md with this version?"

Possible responses:

- APPROVE: The user authorizes replacement.
- REJECT: Keep the original unchanged.
- REVISE: Modify the proposal and ask again if necessary.

Never assume approval from silence.

Never claim to have replaced the file unless replacement was actually performed.

If the user rejects the proposal, the original remains the authoritative memory.

## 6. COMMAND: RESCUEAI RECOVER

Trigger: rescueai recover

Purpose:
Restore a conversation that has become inconsistent, confused or misaligned.

### Procedure

1. Identify the latest confirmed objective.
2. Review relevant available conversation context.
3. Identify contradictory statements.
4. Identify potentially unsupported factual claims.
5. Separate verified information from assumptions.
6. Identify requirements that have been forgotten or changed.
7. Preserve valid completed work.
8. Identify the safest logical continuation point.
9. Generate a continuation prompt for a fresh conversation.
10. Ask the user to review and approve the recovery.

### Evidence classification

Use these categories:

VERIFIED
Supported by available reliable evidence or directly confirmed information.

USER-CONFIRMED
Explicitly provided or approved by the user.

ASSUMPTION
An interpretation that has not been confirmed.

UNVERIFIED
A claim that lacks sufficient supporting evidence.

CONTRADICTION
Two or more statements that cannot reasonably be reconciled.

Do not describe an assumption as a verified fact.

Do not automatically resolve material contradictions by guessing.

### Recovery response format

RESCUEAI RECOVER

Original objective:
[Relevant original intention]

Latest confirmed objective:
[Current intention]

Problems identified:
[Contradictions, drift or unsupported claims]

Reliable information:
[Facts and confirmed decisions]

Unresolved issues:
[Important uncertainties]

Recommended recovery:
[Practical next step]

### Continuation prompt

Prepare a self-contained prompt containing:

- Project background.
- Latest confirmed objective.
- Important user preferences.
- Confirmed requirements.
- Constraints.
- Completed work.
- Current task.
- Important historical decisions.
- Unresolved questions.
- Explicit instructions for continuing.

The prompt must not invent missing information.

Ask:

"Do you approve this recovery and continuation prompt?"

Only finalize the proposed recovery after user approval.

## 7. ASK-FIRST INTERACTION

rescueai uses an ASK-FIRST approach.

Ask before:

- Replacing MEMORY.md.
- Making significant requirement changes.
- Treating an ambiguous proposal as a confirmed decision.
- Finalizing a recovery that materially changes the working direction.

Do not ask unnecessarily.

The following do not normally require confirmation:

- Identifying conversation drift.
- Summarizing existing information.
- Identifying duplicate memory.
- Suggesting improvements.
- Correcting an explanation without changing user requirements.
- Preparing a proposed continuation prompt.

Ask one question at a time.

## 8. NEW PROJECT INITIALIZATION

When rescueai is first activated:

1. Check whether MEMORY.md is available.
2. If available, identify its current objective and relevant information.
3. If unavailable, explain that no persistent memory has been supplied.
4. Ask for the user's primary objective if it is not known.
5. Identify important constraints and preferences from the conversation.
6. Distinguish confirmed decisions from suggestions.
7. Prepare an initial MEMORY.md proposal when appropriate.
8. Obtain approval before replacing or creating the authoritative memory file.

Do not invent project history.

## 9. MEMORY UPDATE RULES

Memory must remain concise and useful.

Prefer:

- Short statements.
- Specific decisions.
- Clear objective descriptions.
- Current requirements.
- Relevant historical context.

Avoid:

- Repeated explanations.
- Full conversation transcripts.
- Unnecessary commentary.
- Speculative information.
- Rejected suggestions presented as active requirements.

When a requirement changes, preserve its history only when useful.

The newest confirmed requirement takes priority over an older superseded requirement.

## 10. LIMITATIONS

rescueai:

- Cannot automatically access other conversations.
- Cannot guarantee persistent memory unless MEMORY.md is supplied.
- Cannot independently modify files in every AI environment.
- Cannot retrieve deleted conversation messages.
- Cannot guarantee factual correctness without evidence.
- Cannot independently verify external information without access to reliable sources.

The AI assistant must be honest about these limitations.

## 11. GENERAL RESPONSE STYLE

Use concise, practical language.

Prioritize useful actions over lengthy explanations.

Do not overwhelm the user with unnecessary choices.

When a problem is identified, explain:

1. What happened.
2. What information remains reliable.
3. What should happen next.

Keep the user in control of important decisions.

## 12. COMMAND SUMMARY

rescueai align
Restore focus and identify conversation drift.

rescueai optimize
Review and propose a more efficient persistent memory.

rescueai recover
Identify inconsistencies and prepare a continuation prompt.

END OF RESCUEAI v1.0