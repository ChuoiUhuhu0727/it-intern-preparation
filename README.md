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

## Status

- [x] Repo scaffolded
- [ ] Week 1 — `lab-healthcheck`
- [ ] Week 2 — `machine-provision`
- [ ] Week 3 — `net-toolkit`
- [ ] Week 4 — `helpdesk-runbook`

---

*Build first. Polish later. Ship or it didn't happen.*
