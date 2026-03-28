# Twitter/X Thread: How the Agent Stack Works

**Hook:**
I built a company that runs itself.

No team. No standups. No Slack.
Just Claude agents — each with a job, a queue, and a log.

Here's the full stack 🧵

---

**1/**
The problem: I wanted to build and ship products but kept getting buried in ops, planning, and context-switching.

So I designed a system where AI agents handle execution.
I just say "go."

---

**2/**
There are 5 active agents right now:

- `ops-agent` — manages the task queue, assigns work
- `dev-agent` — writes and ships code
- `bizdev-agent` — finds revenue opportunities
- `memory-agent` — remembers decisions across sessions
- `reporting-agent` — writes the daily briefing

Each one has a job description, rules, and reads from a shared task queue.

---

**3/**
The shared data layer is dead simple:

```
ops/tasks.md       ← all work lives here
ops/daily-log.md   ← append-only activity log
memory/            ← decisions, lessons, context
reports/latest.md  ← what happened today
```

No database. No API. Just files.

---

**4/**
The task format:

| ID | Priority | Title | Agent | Status |
|----|----------|-------|-------|--------|
| 001 | P0 | Find revenue opportunities | bizdev-agent | DONE |

P0 = drop everything.
P1 = today.
P2 = this week.
P3 = backlog.

Agents pick up their tasks, execute, mark DONE. I never have to babysit.

---

**5/**
The loop runs when I type one word: "go"

ceo-agent dispatches in order:
1. ops-agent assigns work
2. Each assigned agent executes
3. memory-agent captures lessons
4. reporting-agent writes the briefing

I read the briefing. I add new tasks. I say "go" again.

---

**6/**
First real run yesterday:

bizdev-agent found 3 revenue opportunities in one shot:
- Sell the stack as a $49 template
- $500–$1,500 setup service for founders
- $1k–$3k/mo AI agency retainer for startups

Each brief had a target customer, pricing, GTM plan, and a next task.

That's the output of one "go."

---

**7/**
The whole thing is just markdown files and Claude Code.

No infra. No ops cost beyond API usage.
The agents are prompt files. The company runs in a repo.

If you want the template:
→ [link when live]

Or reply and I'll show you how to set it up for your own project.

---

**CTA tweet (standalone):**
I'm selling the full agent stack as a template.

Drop-in to any project. Customize the agents for your workflow.
$49. One-time.

Launching this week — reply "stack" and I'll send you the link first.
