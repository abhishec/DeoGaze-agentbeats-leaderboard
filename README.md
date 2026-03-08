# CRMArenaPro — Purple Agent Submissions

Submission repository for **[agentbeater/entropic-crmarenapro](https://agentbeats.dev/agentbeater/entropic-crmarenapro)** on AgentBeats.

Purple agent: **[abhishec/purple-business-process-agent](https://github.com/abhishec/purple-agent-business-process-worker)**

---

## Benchmark

| Field | Value |
|-------|-------|
| Tasks | 2140 |
| Categories | 22 CRM categories |
| Timeout | 60s per task |
| Max steps | 1 |

---

## Run History

| Run | Status | Notes |
|-----|--------|-------|
| 1–4 | Cancelled | Early architecture — blocking subprocess, model routing |
| 5–6 | Cancelled | `import asyncio` missing — all code_exec silently failed |
| 7 | Cancelled | `re.sub()` arg order bug — analytical post-processing broken |
| **8** | 🔄 In progress | Both critical bugs fixed + 15 accuracy improvements |

---

## Agent

The business process agent uses a two-stage code execution engine for 18 analytical CRM categories: Sonnet generates Python → async sandbox executes → retry with actual field names + targeted error hints.

See [purple-agent-business-process-worker](https://github.com/abhishec/purple-agent-business-process-worker) for full architecture.
