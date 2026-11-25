
# Rescue Lite v1.0

**Lightweight Adaptive AI Conversation Memory and Recovery**

Rescue Lite helps AI assistants maintain project focus, preserve important decisions, manage memory, and recover conversations.

It uses two Markdown files: `SKILL.md` and `MEMORY.md`.

- No database or backend.
- No external AI API.
- No additional AI model.
- No software dependencies.

## Features

| Command | Purpose |
|---|---|
| `Rescue Align` | Restore the latest confirmed objective and identify conversation drift. |
| `Rescue Optimize` | Remove redundant memory while preserving important decisions. |
| `Rescue Recover` | Identify contradictions and prepare continuation prompts. |

### Key Principles

- Confirmed user decisions take priority.
- Suggestions are not treated as confirmed requirements.
- Important constraints must be preserved.
- Memory changes require user approval.
- Recovery must not invent missing information.

## Project Structure

```text
rescue-ai/
├── SKILL.md
├── MEMORY.md
├── README.md
└── LICENSE
```

## Installation

1. Download `SKILL.md` and `MEMORY.md`.
2. Add `SKILL.md` to an AI assistant that supports custom instructions or Skills.
3. Provide `MEMORY.md` as project context.
4. Keep both files available when starting new conversations.
5. Start using Rescue commands.

Installation methods vary between AI platforms.

## Usage

Initialize Rescue:

```text
Initialize Rescue for my project.
```

Restore project focus:

```text
Rescue Align
```

Optimize persistent memory:

```text
Rescue Optimize
```

Recover conversation context:

```text
Rescue Recover
```

## Memory Management

`MEMORY.md` is controlled by the user.

Rescue can propose updates but must obtain approval before replacing existing memory.

Keep backups before applying significant changes.


## Limitations

Rescue Lite cannot automatically access previous conversations, synchronize memory between sessions, or edit local files in every AI environment.

Users must provide the latest memory when starting a new conversation.

Factual accuracy is not guaranteed.

## Technology

- Markdown

## License

MIT License. See [LICENSE](LICENSE).

## Project Status

**Rescue Lite v1.0 — Initial release.**

Designed to remain lightweight, portable, and easy to understand.
