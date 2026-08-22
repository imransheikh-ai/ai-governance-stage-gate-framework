# AI Governance Stage-Gate Framework

## What this is, in plain language

Imagine you're building a house. You wouldn't let the plumber start before the foundation is inspected, and you wouldn't let anyone move in before the electrical work passes a final check. Each stage of construction has a **checkpoint** — an inspector who has to say "yes, this is safe and correct" before work continues to the next stage.

This framework does the same thing for AI projects. It breaks the life of an AI idea — from "someone had a good idea" to "it's running for the whole company" — into **six checkpoints, called gates**. At each gate, someone independent checks the work so far, and the project can only move to the next stage once that check is passed.

**Why AI needs this more than typical software:** a normal app either works or it doesn't, and bugs are usually obvious. An AI system can look like it's working while quietly doing something risky — using data it shouldn't, giving biased or wrong answers confidently, or exposing private information. Those problems don't announce themselves the way a crashed app does. Gates exist to catch them **before** they reach real users, not after.

**Why gates instead of one big approval at the start:** most of what you learn about whether an AI idea is safe and worthwhile only becomes clear as you build it. A single upfront approval means you're betting everything on assumptions made on day one. Six smaller checkpoints mean you can stop or fix course early and cheaply, instead of discovering a problem after it's expensive to undo.

---

## The six gates, explained simply

### Gate 1 — Investment Prioritization
**The question this gate answers:** *"Out of everything we could spend time and money on, is this idea actually worth doing right now?"*

Every organization has more good ideas than it has people and budget. This gate is where someone compares this idea against everything else competing for the same resources, and makes a deliberate choice to fund it — rather than it just starting because someone was enthusiastic.

**Who's usually involved:** the sponsoring business unit, and whoever owns the overall AI/technology investment portfolio (in a large org, a portfolio or investment committee).

**What needs to exist to pass:** a short one-page pitch — the problem, who it helps, a rough size of the prize, and a rough size of the effort.

### Gate 2 — Business Case Approval
**The question this gate answers:** *"Now that we've looked closer, do the numbers actually work?"*

This is where the one-page pitch becomes a real business case: more precise costs (people, tools, cloud spend), more precise benefits (time saved, revenue protected, risk reduced), and a named owner who is accountable for those numbers actually showing up later.

**Who's usually involved:** the business sponsor, finance, and the Head of AI or equivalent technical owner.

**What needs to exist to pass:** a business case document with cost, benefit, timeline, and a named accountable owner.

### Gate 3 — Architecture & Data Readiness
**The question this gate answers:** *"Do we actually have the right data and the right technical foundation to build this properly?"*

An AI system is only as good as the data behind it. This gate checks: is the data available, is it clean enough to be useful, do we have the rights to use it, and is the proposed technical design (which models, which cloud services, how it connects to other systems) sound.

**Who's usually involved:** enterprise architecture, data engineering/data governance, and the AI delivery team.

**What needs to exist to pass:** a data readiness assessment and a one-page architecture design.

### Gate 4 — Security & Risk Review
**The question this gate answers:** *"Could this go wrong in a way that harms someone or the organization?"*

This is the gate that specifically looks for: could this leak private data, could it be tricked or attacked, could it produce biased or unfair outcomes for some group of people, and is there a human able to override it if it misbehaves.

**Who's usually involved:** security/cybersecurity, legal/compliance, and a Responsible AI reviewer.

**What needs to exist to pass:** a completed risk and security review with any required mitigations agreed.

### Gate 5 — Operational Acceptance
**The question this gate answers:** *"If we turn this on for real people tomorrow, are we actually ready to support it?"*

A working prototype and a production-ready service are different things. This gate checks there's a plan for what happens when it breaks at 2am, who monitors it, how users get help, and how you'd roll it back if something goes wrong.

**Who's usually involved:** IT operations/run-and-operate team, the service owner, and end-user representatives.

**What needs to exist to pass:** a support plan, a monitoring plan, and a rollback plan.

### Gate 6 — Scaling Decision
**The question this gate answers:** *"Now that we've run this as a small pilot, should we roll it out further — and if so, how far?"*

This gate looks at real usage data from the pilot — did people actually use it, did it deliver the benefit promised in Gate 2, were there any incidents — and makes a deliberate decision about whether, and how much, to expand it.

**Who's usually involved:** the original sponsor, the Head of AI, and — for larger scale-ups — an executive steering committee.

**What needs to exist to pass:** a pilot results summary compared against the original business case.

---

## Who signs off what (a simple RACI)

| Gate | Accountable | Consulted |
|---|---|---|
| 1. Investment Prioritization | Portfolio/Investment owner | Business sponsor |
| 2. Business Case Approval | Business sponsor | Finance, Head of AI |
| 3. Architecture & Data Readiness | Head of AI / Enterprise Architect | Data governance |
| 4. Security & Risk Review | CISO / Security lead | Legal, Responsible AI reviewer |
| 5. Operational Acceptance | IT Operations lead | Service owner |
| 6. Scaling Decision | Executive sponsor / Steering committee | Head of AI, original business sponsor |

*(In a smaller organization, one or two people may hold several of these roles — the point is that someone independent of "just wanting to ship it" signs off each gate, not that six different departments are required.)*

---

## How to use this framework

1. Use the checklist template in `/templates/stage-gate-checklist-template.md` for every AI project, however small.
2. A project cannot start work on the next stage until its current gate is marked passed.
3. Gates can move quickly for small/low-risk projects — this isn't meant to be bureaucratic. A gate can be "passed" in a 15-minute conversation for a low-risk idea, and take a full committee review for a high-risk, organization-wide one. The rigor should scale with the risk, not be identical for everything.
4. Keep a simple log (even a spreadsheet) of which projects are at which gate — this becomes your AI portfolio view.
