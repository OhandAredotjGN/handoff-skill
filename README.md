# Handoff

A portable agent skill for handing unfinished work to a fresh session without
losing verified progress, settled decisions, or permission boundaries.

It produces one entry document and a copyable pickup prompt. The next agent can
see what is proven, what remains, what must be preserved, and where to start.

## Install

Clone into the skill directory for your agent. Choose the command that matches
your setup and use a new destination directory.

Claude Code:

```sh
git clone https://github.com/OhandAredotjGN/handoff-skill.git ~/.claude/skills/handoff
```

Codex ([local skill locations](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)):

```sh
git clone https://github.com/OhandAredotjGN/handoff-skill.git ~/.agents/skills/handoff
```

For another agent that supports `SKILL.md`, put this repository in its configured
skill directory. You can also read [SKILL.md](SKILL.md) directly and use the
document template without installing anything. No scripts, services, credentials,
or task-board integration are required.

## Use

Ask your agent:

> Use the handoff skill to prepare a clean handoff for the settings-popover task.

The default output is `docs/handoffs/<slug>.md` in the working project. An
existing project convention or an explicit destination takes precedence.

The packet records:

- The accepted objective and remaining acceptance criteria.
- Completed work with evidence and artifact pointers.
- Decisions the user approved and constraints that still apply.
- Relevant source state, ownership, and unrelated work to preserve.
- Ordered next steps, pending decisions, and blockers.
- Actual delivery and monitoring status.

See [a fictional handoff](examples/handoff.md). Preparing the packet does not
start another agent or complete the underlying task.

## Monitoring

Handoffs are manual and unmonitored by default. This repository does not include
a watcher or notification service.

If your environment already has an authorized, durable monitoring facility, the
skill explains what to verify before promising a notification. It requires
honest reporting of stalled work, failure, and expiry as well as success.

## Public edition

This edition uses neutral examples and portable paths. It has no dependency on
private project boards, local machine names, internal policies, or personal
notification channels. It preserves evidence and authorization boundaries while
letting each project supply its own tools and conventions.

Generated handoffs can still contain sensitive project context. Review their
audience and contents before sharing them publicly; installing this skill is
not an automated redaction guarantee.

## License

[MIT](LICENSE).
