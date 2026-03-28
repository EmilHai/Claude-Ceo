# Cyber-CEO Agent Roster

The full stack of autonomous agents required to run this company. Each agent has a defined role, inputs, outputs, and trigger conditions.

---

## Executive Layer

### `ceo-agent`
**Role:** Strategic decision-maker and company orchestrator
**Triggers:** Daily briefing, major decisions, escalations from other agents
**Inputs:** Company metrics, market signals, agent reports
**Outputs:** Strategic directives, priority shifts, resource allocation
**Tools:** All agents, financial dashboards, email

---

## Operations

### `ops-agent`
**Role:** Day-to-day operations and process management
**Triggers:** New tasks, blockers, SLA breaches
**Inputs:** Task queue, agent status, deadlines
**Outputs:** Task assignments, escalations, status reports
**Tools:** Task manager, calendar, Slack/comms

### `scheduler-agent`
**Role:** Manages cron jobs, recurring tasks, and time-based triggers
**Triggers:** Clock events, schedule change requests
**Inputs:** Cron schedules, agent availability
**Outputs:** Triggered agent runs, schedule manifests
**Tools:** CronCreate, CronDelete, CronList

### `monitor-agent`
**Role:** Watches system health, uptime, and agent performance
**Triggers:** Every 5 minutes, on failure events
**Inputs:** Logs, error rates, response times
**Outputs:** Alerts, incident reports, auto-remediation commands
**Tools:** Logs, Bash, notification system

---

## Engineering

### `dev-agent`
**Role:** Writes, reviews, and ships code
**Triggers:** Feature requests, bug reports, tech debt tasks
**Inputs:** Tickets, specs, existing codebase
**Outputs:** Pull requests, code diffs, test results
**Tools:** Read, Write, Edit, Bash, Glob, Grep

### `architect-agent`
**Role:** Designs system architecture and reviews technical decisions
**Triggers:** New projects, major refactors, scaling events
**Inputs:** Requirements, current architecture, performance data
**Outputs:** Architecture plans, ADRs, migration guides
**Tools:** software-architect skill, Read, WebSearch

### `qa-agent`
**Role:** Tests code, finds bugs, enforces quality gates
**Triggers:** PR opened, deploy requested
**Inputs:** Code diffs, test suites, acceptance criteria
**Outputs:** Test reports, bug tickets, pass/fail signals
**Tools:** Bash, Read, Grep

### `security-agent`
**Role:** Audits code and infrastructure for vulnerabilities
**Triggers:** PR opened, weekly scan, new dependencies added
**Inputs:** Code, dependency manifests, configs
**Outputs:** CVE reports, remediation PRs, risk scores
**Tools:** Grep, Bash, WebSearch

### `devops-agent`
**Role:** Manages CI/CD pipelines, deployments, and infrastructure
**Triggers:** Merge to main, deploy command, infra drift detected
**Inputs:** Build configs, environment specs, deployment targets
**Outputs:** Deploy logs, rollback commands, infra diffs
**Tools:** Bash, cloud CLI tools

---

## Product

### `pm-agent`
**Role:** Manages product backlog, writes specs, tracks milestones
**Triggers:** New ideas, sprint planning, stakeholder requests
**Inputs:** User feedback, business goals, engineering capacity
**Outputs:** PRDs, tickets, roadmap updates
**Tools:** pm-doc-driver skill, TaskCreate, TaskUpdate

### `research-agent`
**Role:** Investigates markets, technologies, competitors, and trends
**Triggers:** Strategy sessions, new project kickoffs, on-demand
**Inputs:** Research questions, target domains
**Outputs:** Research reports, summaries, recommendations
**Tools:** WebSearch, WebFetch, Read

### `ux-agent`
**Role:** Designs user flows, reviews interfaces, advocates for users
**Triggers:** New feature design, usability complaints, design reviews
**Inputs:** User stories, mockups, feedback data
**Outputs:** UX recommendations, annotated wireframes, copy suggestions
**Tools:** WebFetch, Read, Write

---

## Finance & Legal

### `finance-agent`
**Role:** Tracks revenue, expenses, burn rate, and financial health
**Triggers:** Daily close, invoice received, anomaly detected
**Inputs:** Transaction data, budgets, projections
**Outputs:** P&L summaries, budget alerts, financial reports
**Tools:** business-accountant-mentor skill, spreadsheet tools

### `legal-agent`
**Role:** Reviews contracts, flags compliance issues, monitors regulations
**Triggers:** Contract submitted, new market entered, policy changes
**Inputs:** Contracts, regulatory updates, company policies
**Outputs:** Redlines, compliance memos, risk flags
**Tools:** WebSearch, Read, Write

---

## Growth & Marketing

### `marketing-agent`
**Role:** Creates content, manages campaigns, tracks brand presence
**Triggers:** Product launch, content calendar, campaign deadlines
**Inputs:** Product updates, target audience, campaign briefs
**Outputs:** Blog posts, ad copy, social content, campaign reports
**Tools:** Write, WebSearch, WebFetch

### `bizdev-agent`
**Role:** Identifies partnerships, revenue opportunities, and go-to-market strategies
**Triggers:** Expansion goals, partner inquiries, quarterly planning
**Inputs:** Market data, company strengths, target verticals
**Outputs:** GTM plans, partnership proposals, revenue models
**Tools:** bizdev-idea-generator skill, WebSearch

### `sales-agent`
**Role:** Qualifies leads, drafts outreach, tracks pipeline
**Triggers:** New lead, follow-up due, deal stage change
**Inputs:** Lead data, CRM state, product positioning
**Outputs:** Outreach emails, call summaries, deal updates
**Tools:** Gmail MCP, WebSearch, Write

---

## Communications

### `comms-agent`
**Role:** Handles external communications, drafts emails, manages inbox
**Triggers:** Incoming email, scheduled send, announcement needed
**Inputs:** Email threads, communication briefs
**Outputs:** Drafted emails, sent confirmations, response summaries
**Tools:** gmail_create_draft, gmail_read_message, gmail_search_messages

### `hr-agent`
**Role:** Manages hiring, onboarding, performance, and culture
**Triggers:** Open role, applicant received, review cycle
**Inputs:** Job specs, candidate profiles, team feedback
**Outputs:** Job posts, interview questions, offer letters, review reports
**Tools:** Write, WebSearch, comms-agent

---

## Memory & Intelligence

### `memory-agent`
**Role:** Maintains persistent company knowledge — decisions, context, lessons learned
**Triggers:** After major decisions, project close, incident resolved
**Inputs:** Conversation summaries, agent outputs, key decisions
**Outputs:** Memory files, indexed knowledge base
**Tools:** Write, Read, Glob

### `reporting-agent`
**Role:** Aggregates cross-agent data into executive summaries
**Triggers:** Daily at 08:00, on-demand
**Inputs:** Agent logs, metrics, task status
**Outputs:** Daily briefing doc, weekly digest, KPI dashboard
**Tools:** TaskList, TaskGet, Read, Write

---

## Agent Count Summary

| Layer | Agents |
|---|---|
| Executive | 1 |
| Operations | 3 |
| Engineering | 5 |
| Product | 3 |
| Finance & Legal | 2 |
| Growth & Marketing | 3 |
| Communications | 2 |
| Memory & Intelligence | 2 |
| **Total** | **21** |
