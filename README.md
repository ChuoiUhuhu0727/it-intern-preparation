# it-intern-preparation

> My 4-week journey to earn a spot as an IT intern in my university's computer lab — the room I love most.

i aspire to become IT intern in my university, to become an essential part of my most favorite room in my school: computer lab. This repo is my journey of self-learning and practicing computer-system key concepts to take over this role (hopefully huhu).

## The goal

By **mid-August 2026**, have a portfolio that proves I can actually *do* the lab job — not just talk about it. The IT intern role touches three pillars, so this repo does too:

- **Helpdesk & hardware** — fixing machines, imaging the OS, supporting users
- **Sysadmin & scripting** — managing many machines, automating the boring parts
- **Networking** — lab connectivity, IP/subnet, troubleshooting

## How I build (the philosophy)

Every tool here follows the same three-beat spine of any good ops script:

```
COLLECT facts  →  JUDGE against thresholds  →  REPORT
```

The gap between amateur and pro lives in **JUDGE**. Printing `Disk: 95%` is amateur.
Printing `⚠️ Disk 95% — almost full, needs cleanup` is someone who knows the job.
Every script here doesn't just list numbers — it forms an opinion.

I also learn **context + intuition first**: before writing any code, I map each metric to a real user complaint. Example, for machine health:

| A user complains… | …the metric behind it |
|---|---|
| "Disk full, can't save / can't update" | Disk free % |
| "Everything lags" | RAM used / free |
| "Machine runs hot, shuts down" | CPU load |
| "Nobody rebooted this in ages" | Uptime |
| "Missing software / unpatched Windows" | Installed software + pending updates |

## 4-week roadmap

One runnable project per week, each mapping to a real task an IT intern does in the lab.

| Week | Pillar | Project | The real lab task it mirrors |
|------|--------|---------|------------------------------|
| **1** (Jul 19–26) | Sysadmin | `lab-healthcheck/` — PowerShell + Bash script that audits one machine (OS, disk, RAM, uptime, software, pending updates) and returns a pass/warn verdict | Spotting which of 40 lab machines is "sick" without checking each by hand |
| **2** (Jul 27–Aug 2) | Sysadmin + Helpdesk | `machine-provision/` — idempotent setup script for a fresh machine (install standard software, apply config) | Re-imaging / provisioning lab machines at the start of term |
| **3** (Aug 3–9) | Networking | `net-toolkit/` — ping sweep to find live machines in a subnet + IP/subnet calculator + connectivity troubleshooter | Finding which machine dropped off the network; diagnosing "no internet" |
| **4** (Aug 10–15) | Helpdesk | `helpdesk-runbook/` — triage playbook for common lab incidents + repo polish + demo | Structured, repeatable user support |

## Why this track — and what it costs

Long-term I want to be an **embedded systems / robotics engineer**. These projects aren't the *core* of that — firmware, real-time, and control theory live elsewhere. They're the **enabling layer**: Linux fluency, automation, systematic debugging, and the `sense → threshold → act` reflex that every robot loop shares. I'm walking this track with eyes open about the trade-offs:

- **Opportunity cost** — hours here are hours not spent deepening robotics. IT skills plateau fast; domain depth compounds. So this track is deliberately **time-boxed to 4 weeks**.
- **Breadth vs depth** — helpdesk/sysadmin work is broad and shallow; robotics needs deep vertical mastery. This is a foundation, not a destination.
- **Comfort trap** — scripting gives fast green-check dopamine; embedded gives slow, painful wins. I watch for drifting toward the easy track and avoiding the hard one.

**Guardrails I hold myself to:**

- **Build first, polish later** — working code before a pretty README.
- Before opening a new thing to read: *"does this produce something runnable in the next 60 minutes?"* If not, log it and move on.
- Each project consciously **pulls a robotics thread** — Python over shell where sensible; make `sense → threshold → act` explicit.
- **Explain the code back before shipping it** — understand the concept, not just the output.

## Status

- [x] Repo scaffolded
- [ ] Week 1 — `lab-healthcheck`
- [ ] Week 2 — `machine-provision`
- [ ] Week 3 — `net-toolkit`
- [ ] Week 4 — `helpdesk-runbook`

---

*Build first. Polish later. Ship or it didn't happen.*
