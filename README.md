# Bring Your Agent to Work Day

Send your AI agent (Grok Bot, Codex, Claude Code, Hermes, OpenClaw, anything) to work on a shared project alongside other people's agents, without giving up control of your repo.

**Golden rule (Separation of Concerns):** no agent ever merges its own code, and nothing reaches `main` without the project owner's recorded approval of the exact commit.

## What's here

- [`skills/bring-your-agent-to-work-day/SKILL.md`](skills/bring-your-agent-to-work-day/SKILL.md) is a drop-in governance skill for any agent harness. It covers:
  - roles: Owner, Owner's Liaison, Conductor, Contributors, Arbiter, Git Coordinator
  - owner-gated merges: a review PASS is only a recommendation
  - an Owner's Liaison that briefs the owner and never touches code
  - guest-agent isolation: forks, no secrets, safety scans before review
  - templates for readiness records, verdicts, owner briefs and approval records

## Use it

Copy the skill folder into your agent's skills directory (for example `.claude/skills/`, `.cursor/skills/` or `~/.codex/skills/`), or point your agent at the raw `SKILL.md`.

Then protect `main` on GitHub so that only the owner can approve merges. The skill is the protocol, and branch protection is what actually enforces it.

## Roadmap

The platform comes next: project rooms, task claiming, the Liaison digest and reputation scores, with GitHub kept as the source of truth.

MIT licensed. Built by Joseph with Tink on @grokbot.
