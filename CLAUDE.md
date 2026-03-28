# Cyber-CEO — Operating Manual

## What this is
An autonomous company run by AI agents. You are the CEO. Agents handle execution.

## How to run
Say **"go"** to run the full autonomous loop. The ceo-agent will dispatch all agents in order without you needing to trigger each one manually. It will only stop to ask you if a decision requires human judgment.

## Agent roster (active)
| Agent | File | Does what |
|-------|------|-----------|
| ceo-agent | agents/ceo-agent.md | Orchestrates the full loop — dispatches all agents automatically |
| ops-agent | agents/ops-agent.md | Manages task queue, assigns work, flags blockers |
| dev-agent | agents/dev-agent.md | Writes and ships code |
| memory-agent | agents/memory-agent.md | Distills decisions and lessons into persistent memory |
| reporting-agent | agents/reporting-agent.md | Daily briefing — status, blockers, metrics |
| bizdev-agent | agents/bizdev-agent.md | Revenue opportunities, GTM plans, outreach |

Full roster (including inactive agents): `AGENTS.md`

## Shared data layer
| Path | Purpose |
|------|---------|
| `ops/tasks.md` | Single source of truth for all work |
| `ops/daily-log.md` | Append-only activity log |
| `memory/INDEX.md` | Index of all memory files |
| `memory/*.md` | Individual memory entries |
| `reports/latest.md` | Most recent daily briefing |
| `reports/YYYY-MM-DD.md` | Archived daily briefings |

## How to run an agent
Invoke any agent by saying: **"run ops-agent"** (or dev/memory/reporting).
The agent will read its definition from `agents/<name>.md` and execute its responsibilities.

## How to add work
Add a row to `ops/tasks.md`, then run ops-agent to assign it.

Priority levels: `P0` (now), `P1` (today), `P2` (this week), `P3` (backlog)

## Daily rhythm
1. `run reporting-agent` → read `reports/latest.md`
2. Add any new tasks to `ops/tasks.md`
3. `run ops-agent` → assigns/prioritizes work
4. `run dev-agent` → executes engineering tasks
5. End of day: `run memory-agent` → captures lessons
