# Claude CEO

An autonomous company that runs on Claude agents. You say "go." The agents handle the rest.

## What this is

A system of AI agents — each with a defined role, a shared task queue, and a daily log — that runs your company's operations, engineering, business development, and reporting without you micromanaging every step.

## Quickstart

**Requirements:** [Claude Code](https://claude.ai/code) (free tier works)

```bash
git clone <this-repo>
cd claude-ceo
code .   # or open in your editor
```

Open Claude Code in this directory. It will read `CLAUDE.md` automatically.

**Run your first cycle:**
> go

That's it. The `ceo-agent` dispatches all active agents in order and returns a briefing.

---

## How to add work

Open `ops/tasks.md` and add a row:

```
| 005 | P1 | Your task title | dev-agent | TODO | Any notes |
```

Then say **"go"** and the loop picks it up.

**Priority levels:**
| Level | Meaning |
|-------|---------|
| P0 | Drop everything — do this now |
| P1 | Today |
| P2 | This week |
| P3 | Backlog |

---

## Agent roster

| Agent | Role |
|-------|------|
| `ceo-agent` | Orchestrates the full loop |
| `ops-agent` | Manages task queue, assigns work, flags blockers |
| `dev-agent` | Writes and ships code |
| `bizdev-agent` | Finds revenue opportunities, writes GTM plans and outreach |
| `memory-agent` | Distills decisions and lessons into persistent memory |
| `reporting-agent` | Produces the daily briefing |

Full future roster: [`AGENTS.md`](AGENTS.md)

---

## File structure

```
claude-ceo/
  CLAUDE.md                  ← operating manual (auto-loaded by Claude Code)
  README.md                  ← this file
  AGENTS.md                  ← full agent roster (active + planned)
  agents/                    ← agent definitions (prompt + rules)
  ops/
    tasks.md                 ← single source of truth for all work
    daily-log.md             ← append-only activity log
  memory/
    INDEX.md                 ← index of all memory entries
    *.md                     ← individual memory files
  bizdev/
    opportunities.md         ← index of revenue opportunities
    opportunity-*.md         ← individual opportunity briefs
    outreach-*.md            ← outreach drafts
  content/                   ← marketing content drafts
  reports/
    latest.md                ← today's briefing
    YYYY-MM-DD.md            ← archived daily briefings
```

---

## Customizing agents

Each agent lives in `agents/<name>.md`. Edit the file to change its behavior — what it reads, what it writes, its rules. The agents are just prompts.

To add a new agent:
1. Create `agents/my-agent.md` following the format of any existing agent
2. Add it to the roster table in `CLAUDE.md`
3. Assign it tasks in `ops/tasks.md`

---

## Daily rhythm

```
Say "go"
  → ops-agent assigns tasks
  → agents execute in priority order
  → memory-agent captures lessons
  → reporting-agent writes briefing
Read reports/latest.md
Add new tasks if needed
Say "go" again
```
