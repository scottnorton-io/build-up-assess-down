# Facilitator Guide

**Titanium Framework v1.0 — Facilitator Edition**

This guide provides minute-by-minute delivery instructions for the **Build Up / Assess Down: Dependency-Based PCI DSS Enablement** program.

---

## Program Overview

**Duration:** 90 minutes

**Format:** Interactive workshop with case-based learning

**Target audience:** Security leaders, PCI program owners, architects, QSAs/ISAs, GRC teams

**Learning outcome:** Participants will understand PCI DSS as a dependency stack and apply Build Up / Assess Down / Prioritized Approach lenses to their environments

---

## Pre-Session Setup (15 minutes before start)

**Materials check:**

- [ ]  Master diagram visible (slide 3)
- [ ]  Case study handouts ready
- [ ]  Whiteboard or digital collaboration space
- [ ]  Timer visible to participants

**Room setup:**

- Collaborative seating (small tables, 3-4 per group)
- Clear sightlines to visual aids
- Energy level: conversational, not lecture-hall

**Facilitator mindset:**

- You are not teaching *requirements*—you are teaching *why they break*
- Participants already know PCI causes pain; your job is to explain *the system*
- Every question is evidence of engagement—treat them as assets

---

# Part 1 — The Problem (15 minutes)

## 0:00–0:15 | *Why PCI DSS feels harder than it should*

### Opening (0:00–0:03)

**What you say (verbatim):**

> "Most people experience PCI like a yearly storm. Scramble, collect evidence, pray scope doesn't grow, rinse, repeat. Today I'm going to reframe PCI DSS as what it really is: a dependency stack. If you build the foundation correctly, compliance doesn't have to be hunted. It emits."
> 

**Delivery note:** Pause after "it emits." Let that land.

---

### Exercise: Where Did Your Last Assessment Surprise You? (0:03–0:08)

**Instructions to participants:**

> "Take 60 seconds. Think about your most recent PCI assessment or readiness effort. Where did you get surprised? Not 'what requirement was hard'—but where did reality not match expectations?"
> 

**Facilitation:**

- Let them think silently for 30 seconds
- Then pair-share for 90 seconds
- No need to collect every answer—just listen for patterns

**Expected answers (listen for these):**

- Scope expanded late
- Data showed up in logs/backups/queues
- Segmentation wasn't actually effective
- Evidence didn't exist ("we thought we were doing that")
- Ownership unclear

**Red flags:**

- If someone says "the assessor was unreasonable"—acknowledge but redirect: *"What would have made that disagreement impossible?"*
- If someone says "we didn't have time"—probe: *"What would need to be true for this to feel boring instead of urgent?"*

---

### The Diagnosis (0:08–0:15)

**What you say:**

> "Almost everyone just described the same problem: PCI exposes design debt. The surprise isn't that requirements are hard—it's that we didn't understand the system we built."
> 

**Key teaching moment (deliver slowly):**

> "PCI DSS pain is rarely 'we don't know the requirement.' It's 'we didn't design dependencies correctly, so validation exposed reality late.'"
> 

**Transition to Part 2:**

> "Let's fix that. I'm going to show you three lenses that explain why this happens—and how to prevent it."
> 

---

# Part 2 — Build Up: Dependency-Based Design (25 minutes)

## 0:15–0:40 | *Walk Requirements 1 → 12 as a dependency stack*

### The Core Model Reveal (0:15–0:18)

**Show the master diagram** (the merged Mermaid visual).

**What you say:**

> "Three lenses, one truth:
> 

> - **Build Up** creates reality—Requirements 1 through 12, in dependency order
> 

> - **Prioritized Approach** weights effort where risk hurts most—the Council's six milestones
> 

> - **Assess Down** proves reality—Requirements 12 back to 1, following evidence
> 

> 
> 

> Here's the kicker: assessors often discover architecture last."
> 

**Pause.** Let participants study the diagram for 15 seconds.

**Facilitation note:** If someone asks "Is this official?", answer:

> "This is dependency-based interpretation of PCI DSS. It doesn't replace the standard—it explains how controls actually work in systems."
> 

---

### Build Up Walkthrough (0:18–0:35)

**Format:** Rapid dependency explanation—NOT a requirement-by-requirement lecture.

For each requirement group, explain:

1. What it does (dependency role)
2. What breaks if it's weak (blast radius)
3. One concrete example

### Requirements 1–2: Foundation Layer (0:18–0:22)

**Req 1 — Network Security Controls**

**What you say:**

> "Req 1 defines enforceable scope boundaries. If this is wrong, every other requirement's scope is unreliable. You can't protect what you can't define."
> 

**Example:**

> "Segmentation looks clean on a diagram. Then Req 11 testing shows flat routing. Suddenly everything is in scope. That's a Req 1 failure discovered at Req 11."
> 

**Req 2 — Secure Configurations**

**What you say:**

> "Baselines determine your operational reality. Weak configs mean every control above is compensating for a broken foundation."
> 

**Key insight:**

> "If Req 1–2 are weak, everything above lies."
> 

---

### Requirements 3–4: Data Gravity Layer (0:22–0:26)

**Req 3 — Protect Stored Account Data**

**What you say:**

> "Data gravity defines scope. AD minimization isn't a nice-to-have—it's the single biggest scope lever you control."
> 

**Example:**

> "Milestone 1 says 'remove SAD, limit retention.' Teams do a data cleanup project. But logs, backups, queues, and endpoints still contain PAN. Req 3 and Req 10 both fail—because this wasn't treated as an *architecture problem*."
> 

**Req 4 — Protect AD in Transit**

**What you say:**

> "Strong crypto in transit. Dependency: you must know *where* data moves (Req 1) before you can protect those paths."
> 

---

### Requirements 5–6: Operational Hygiene Layer (0:26–0:29)

**Req 5 — Malware Defense**

**Req 6 — Secure SDLC + Change Control**

**What you say:**

> "These keep controls alive. You can design perfectly, but if malware compromise or uncontrolled changes happen, all prior work degrades."
> 

**Key insight:**

> "Req 6 is where v4.0.1 gets serious. SDLC isn't theater—it's the immune system."
> 

---

### Requirements 7–9: Access Control Layer (0:29–0:32)

**Req 7 — Need-to-Know Access**

**Req 8 — Identity + Authentication**

**Req 9 — Physical Controls**

**What you say:**

> "Access control assumes the foundation works. You can't enforce least privilege meaningfully if scope is undefined or data is everywhere."
> 

---

### Requirements 10–11: Observability Layer (0:32–0:35)

**Req 10 — Logging + Monitoring**

**Req 11 — Testing Security**

**What you say:**

> "You can't monitor what wasn't designed. You can't test what doesn't exist. These requirements *reveal* whether the stack below actually works."
> 

**Critical insight:**

> "Req 11 is where segmentation reality gets discovered. If you wait until penetration testing to validate Req 1, you've already lost."
> 

---

### Requirement 12: Governance Layer (0:35–0:38)

**Req 12 — Security Policies + Programs**

**What you say:**

> "Governance is the amplifier, not the starting point. Req 12 doesn't create security—it scales and sustains what's real."
> 

**Key reframing moment (deliver with emphasis):**

> "You don't start with policies. You end with them. Policies codify operational truth. If the truth is weak, the policies are fiction."
> 

---

### Build Up Summary (0:38–0:40)

**What you say:**

> "That's Build Up. Requirements are dependencies. If you design bottom-up with dependency awareness, you don't fight PCI—you architect it away."
> 

**Transition:**

> "But teams don't usually build this way. They use the Council's Prioritized Approach. Let's reconcile that."
> 

---

# Part 3 — The Prioritized Approach (Reconciled) (15 minutes)

## 0:40–0:55 | *Milestones are a risk overlay, not the build order*

### The Tension (0:40–0:42)

**What you say:**

> "The Council's Prioritized Approach groups requirements into six milestones based on risk reduction. It's smart. But here's the problem: teams treat milestones as the *implementation sequence*. That causes siloed fixes and late surprises."
> 

**Show milestones 1–6 on the diagram.**

---

### The Reconciliation (0:42–0:50)

**What you say (this is your signature line—deliver it clean):**

> "The Prioritized Approach tells you where risk hurts most. Build Up tells you how to remove it. Assess Down tells you how it will be proven. All three are true at once."
> 

**Walk through Milestone 1 as proof:**

**Milestone 1: Remove SAD / Limit Data Retention**

**What you say:**

> "Milestone 1 attacks data gravity. That's the right risk target. But if you do data cleanup without fixing architecture—without validating Req 1 boundaries, without enforcing Req 3 retention policies in logs and backups—you get tactical wins and strategic failure."
> 

**Example (use this verbatim):**

> "You run a Milestone 1 project. Delete old cardholder data. Great. Six months later, Req 10 evidence shows PAN in application logs. Req 3 evidence shows PAN in backup retention. Milestone 1 looked done, but dependencies weren't honored."
> 

**Teaching moment:**

> "Milestones are a *risk lens*. They help you prioritize *where* to spend effort. But they don't replace *how* to build or validate. That's what Build Up and Assess Down provide."
> 

---

### Exercise: Milestone vs Dependency Tension (0:50–0:55)

**Instructions to participants:**

> "In your group, pick one milestone. Identify one dependency that—if ignored—would make that milestone *look* complete but actually fail."
> 

**Time:** 3 minutes group discussion, 2 minutes share-out

**Expected answers:**

- M1 (data retention) without Req 1 (scope clarity) = data still in logs/backups
- M2 (protect systems) without Req 6 (SDLC) = protections degrade on next release
- M4 (monitor access) without Req 7/8 (access controls) = monitoring noise, not signal

**Red flag:**

- If groups can't find tension, prompt: *"What would make your assessor disagree that this milestone is done?"*

**Facilitation:**

- Affirm every answer that shows dependency awareness
- Redirect answers that blame assessors or tooling

---

# Part 4 — Assess Down: Why Assessments Feel Backwards (20 minutes)

## 0:55–1:15 | *Evidence flows 12 → 1*

### The Assessor Perspective (0:55–1:00)

**What you say:**

> "Assessors don't start at Req 1 and march forward. They start at Req 12—governance and program maturity—and work backwards through evidence. By the time they validate Req 1, they've already inferred whether your architecture is real or aspirational."
> 

**Show Assess Down flow on diagram.**

**Key insight:**

> "Assessors discover architecture last. That's why scope surprises happen late if boundary reality wasn't validated early."
> 

---

### Evidence as System Output (1:00–1:07)

**What you say:**

> "Here's the shift: evidence should not be something you *produce for an assessment*. Evidence should be something your systems *generate continuously* because controls are operating."
> 

**Walk Req 12 → 1 at the *evidence level*:**

**Req 12:** Policies, ownership, risk assessments → *proves program exists*

**Req 11:** ASV scans, vulnerability mgmt, pen test → *proves testing operates*

**Req 10:** Logs, alerts, incident tickets → *proves monitoring works*

**Req 7–9:** Access reviews, MFA logs, badge records → *proves access controls operate*

**Req 6:** SDLC evidence, patch records → *proves change is controlled*

**Req 5:** AV logs, email gateway blocks → *proves malware defense works*

**Req 3–4:** Encryption evidence, data discovery → *proves data is protected*

**Req 2:** Config baselines, compliance scans → *proves hardening is real*

**Req 1:** Segmentation validation, network diagrams + testing → *proves scope is accurate*

**Emphasize Req 1 explicitly:**

> "Req 1 is validated last. If your network reality doesn't match your scope assertion, everything unravels. That's why early segmentation validation is critical—even though it happens 'out of order' in Assess Down."
> 

---

### Case Study: Segmentation Is a Diagram (1:07–1:15)

**Scenario (read aloud):**

> "You have a beautiful network diagram. CDE is segmented. Firewall rules documented. Req 1 looks solid. You proceed through the year. Req 11 penetration testing happens. Tester pivots from out-of-scope system into CDE. Segmentation failed. Suddenly 40 additional systems are in scope."
> 

**Group discussion prompt (5 minutes):**

> "Where did this fail in Build Up? Where did this get discovered in Assess Down? What milestone would have helped—and why didn't it?"
> 

**Expected answers:**

- Build Up failure: Req 1 wasn't validated early (dependency ignored)
- Assess Down discovery: Req 11 testing revealed reality
- Milestone relevance: M2 (protect systems/networks) looked done, but segmentation *effectiveness* was assumed, not proven

**Facilitator coaching:**

- If groups blame the pentester: *"The tester revealed truth. What would have made that truth obvious earlier?"*
- If groups say "test more often": *"Yes—and what does that tell you about when Req 1 should be validated?"*

**Teaching close:**

> "This is the pattern. Build Up creates reality. Assess Down reveals it. If you don't validate early, you pay late."
> 

---

# Part 5 — The Payoff: Compliance as Exhaust (15 minutes)

## 1:15–1:30 | *Bring it home*

### The Mantra (1:15–1:17)

**What you say (slow, clear, memorable):**

> "Compliance is the exhaust. Security is the engine. If you want compliance, stop chasing compliance. Chase good design, clean scope boundaries, and controls that operate every day."
> 

**Let that settle.**

---

### Trusted Advisor vs Auditor Behaviors (1:17–1:22)

**What you say:**

> "Auditors ask: 'Show me.' Trusted Advisors ask: 'How does this really work day-to-day?' That question changes everything."
> 

**Contrast table (show or speak):**

**Auditor behavior:**

- "Show me your last quarterly access review."
- "Do you retain PAN?"
- "Is this documented?"

**Advisor behavior:**

- "How do you know access still matches job function after org changes?"
- "Where would PAN show up if retention controls failed?"
- "What happens when this process breaks?"

**Key insight:**

> "Advisors help you design for truth. Auditors validate truth. Both are necessary. But if you only think like an auditor, you'll always be reactive."
> 

---

### Key Outcomes When the Model Is Applied (1:22–1:25)

**What you say:**

> "When you Build Up with dependency awareness, use milestones to weight risk, and validate continuously using Assess Down logic, here's what happens:"
> 
- Fewer compensating controls
- Smaller, stable scope
- Predictable assessments
- Evidence that already exists
- Less stress on teams
- Compliance becomes boring

**Anchor line:**

> "If you build PCI DSS correctly, the assessment doesn't validate effort—it confirms reality."
> 

---

### Final Exercise: Apply the Model (1:25–1:30)

**Instructions:**

> "Pick one pain point from your current PCI program. In 2 minutes, identify:
> 

> 1. Where it failed in Build Up (which dependency was weak)
> 

> 2. Where it will be discovered in Assess Down (which requirement exposes it)
> 

> 3. Which milestone you thought addressed it—and why it didn't"
> 

**Facilitation:**

- This is self-reflection, not share-out (unless time permits)
- Walk the room; listen for insights
- Affirm anyone who identifies a *dependency gap* vs blaming tools/people

---

### Close (1:30)

**What you say:**

> "You now have a mental model most PCI programs are missing. You understand dependencies. You know how to use milestones without being trapped by them. You know how evidence flows. Go build systems where compliance takes care of itself."
> 

**Final instruction:**

> "Your field kit includes the dependency map, evidence storyboard template, and the three failure-mode case studies. Use them. And remember: don't prepare for an assessment. Design for truth."
> 

---

## Post-Session Debrief (Facilitator Self-Check)

**Evaluation questions:**

- Did participants identify dependencies, not just requirements?
- Did anyone have an 'aha' moment about milestones vs build order?
- Did case discussions surface real examples vs theoretical debate?
- Did the Assess Down section explain *why* surprises happen?

**Red flags to watch for next time:**

- Participants debating requirement interpretations (redirect to dependencies)
- Participants blaming assessors (redirect to design accountability)
- Participants asking for tools/products (redirect to mental model first)

**Refinement notes:**

- Which examples landed strongest?
- Which exercises felt rushed?
- Where did energy dip?

---

## Appendix: Facilitator Quick Reference

### Timing At-a-Glance

- 0:00–0:15 | Part 1: The Problem
- 0:15–0:40 | Part 2: Build Up
- 0:40–0:55 | Part 3: Prioritized Approach
- 0:55–1:15 | Part 4: Assess Down
- 1:15–1:30 | Part 5: The Payoff

### Key Phrases to Repeat

- "Compliance is the exhaust. Security is the engine."
- "Build Up creates reality. Assess Down proves it. Milestones weight risk."
- "You don't start with policies. You end with them."
- "If you build PCI DSS correctly, the assessment confirms reality."

### Facilitation Principles

- **Dependency thinking > requirement memorization**
- **System awareness > checklist completion**
- **Design accountability > assessor blame**
- **Evidence as continuous output > seasonal scramble**
