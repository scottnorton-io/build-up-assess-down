# Keynote Deck

**Titanium Framework v1.0 — Keynote Edition**

**Title:** Build Up, Assess Down: Why PCI DSS Feels Backwards (and How Trusted Advisors Fix It)

**Duration:** 45 minutes (12 slides + Q&A)

**Target audience:** Security leaders, QSAs/ISAs, PCI program owners, compliance executives

---

# Slide-by-Slide Speaker Script

## Slide 1 — Title

**Visual:**

- Title: **Build Up, Assess Down**
- Subtitle: *Why PCI DSS feels backwards—and how to make compliance a byproduct of good design*
- Your name + credentials
- Minimal, clean design

**Speaker notes (30 seconds):**

> "Most people experience PCI like a yearly storm. Scramble, collect evidence, pray scope doesn't grow, rinse, repeat. Today I'm going to reframe PCI DSS as what it really is: a dependency stack. If you build the foundation correctly, compliance doesn't have to be hunted. It emits."
> 

**Delivery cues:**

- Pause after "It emits" — let that land
- Make eye contact
- Energy: confident, conversational

---

## Slide 2 — The Pain Everyone Shares

**Visual:**

- Heading: **The three surprises that ruin PCI seasons**
- Three bullet points (large text):
    - Scope expands late
    - Data shows up where nobody expected
    - Evidence becomes archaeology

**Speaker notes (2 minutes):**

> "Before we dive into solutions, let's acknowledge the pain. Raise your hand if any of these sound familiar."
> 

**[Pause for hands]**

> "First: scope expansion. You thought you had 20 systems in scope. Then the assessor asks about that analytics platform, or those backup servers, or the logs that get shipped to your SIEM. Suddenly you have 40 systems."
> 

> "Second: data discovery. You did a data cleanup project. Purged old cardholder data. Then someone finds PAN in application logs. Or backups. Or that queue nobody remembered. Or endpoints."
> 

> "Third: evidence archaeology. The assessor asks for proof that something happened quarterly all year. And you realize nobody was generating that evidence—because you thought the control was someone else's job."
> 

**[Pause]**

> "Here's the pattern: PCI pain is rarely 'we don't know the requirement.' It's 'we didn't understand the system we built.' PCI exposes design debt."
> 

**Delivery cues:**

- Interactive: get audience participation on the hand-raise
- Use real examples from your experience if you have them
- Emphasize the last line: "PCI exposes design debt"

---

## Slide 3 — The Core Model (Hero Slide)

**Visual:**

- The merged Mermaid diagram (Build Up × Prioritized Approach × Assess Down)
- Title: **Three lenses, one truth**
- Minimal text overlay:
    - Build Up: Requirements 1 → 12
    - Prioritized Approach: 6 Milestones (risk overlay)
    - Assess Down: Requirements 12 → 1

**Speaker notes (3 minutes):**

> "Let me show you three lenses that explain why those surprises happen—and how to prevent them."
> 

**[Reveal diagram]**

> "First lens: **Build Up**. This is how systems are actually designed and implemented. Requirements 1 through 12, in dependency order. You start with network security controls and segmentation. Then secure configurations. Then data protection. Then SDLC and change control. You build upward, each layer depending on the one below."
> 

> "Second lens: **Prioritized Approach**. This is the Council's six milestones. It's a risk-weighting overlay. It tells you where to spend effort based on where risk hurts most. Milestone 1: remove sensitive authentication data and limit retention. Milestone 2: protect systems and networks. And so on."
> 

> "Third lens: **Assess Down**. This is how assessments actually work. Assessors don't start at Requirement 1 and march forward. They start at Requirement 12—governance and program maturity—and work backwards through evidence. By the time they validate Requirement 1, they've already inferred whether your architecture is real or aspirational."
> 

**[Pause, let them look at the diagram]**

> "Here's the kicker: assessors often discover architecture last. That's why scope surprises happen late if you didn't validate boundaries early."
> 

**Delivery cues:**

- Give audience 15 seconds to study the diagram
- Point to each section as you describe it
- The "kicker" line is critical—deliver it clearly

---

## Slide 4 — Build Up Is How Systems Actually Work

**Visual:**

- Heading: **PCI DSS Requirements are dependencies, not topics**
- Four key insights (large text):
    - If Req 1–2 are weak, everything above lies
    - If Req 3 is messy, scope spreads
    - If Req 10/11 are weak, you can't prove operation
    - Req 12 amplifies truth; it can't create it

**Speaker notes (3 minutes):**

> "Build Up is engineering logic. Requirements are stacked. Let me explain what I mean."
> 

> "Requirement 1: network security controls. This defines your scope boundaries. If this is wrong, every other requirement's scope becomes unreliable. You can't protect what you can't define."
> 

> "Requirement 2: secure configurations. This establishes your operational baseline. Weak configs mean every control above is compensating for a broken foundation."
> 

> "Together, Requirements 1 and 2 are your foundation. If they're weak, everything above lies."
> 

> "Requirement 3: protect stored account data. This controls data gravity. If data minimization fails, scope spreads to logs, backups, queues, endpoints. This isn't a compliance problem—it's an architecture problem."
> 

> "Requirements 10 and 11: logging, monitoring, and testing. These reveal whether the stack below actually works. You can't monitor what wasn't designed. You can't test what doesn't exist."
> 

> "Requirement 12: governance and policies. This is the amplifier, not the starting point. Policies codify operational truth. If the truth is weak, the policies are fiction."
> 

**[Pause]**

> "You don't start with policies. You end with them."
> 

**Delivery cues:**

- Walk through the dependency logic clearly
- The final line ("You don't start with policies") is a key reframe—deliver with emphasis

---

## Slide 5 — The Trusted Advisor Shift

**Visual:**

- Large quote in center:
    - **"Stop 'passing PCI.' Start designing for truth."**
- Small text below: Compliance is the exhaust. Security is the engine.

**Speaker notes (2 minutes):**

> "This is where the mental model shift happens. Most organizations optimize for passing assessments. They think like auditors. 'What does the assessor want to see? What evidence do we need to produce?'"
> 

> "Trusted Advisors think differently. They ask: 'How does this really work day-to-day? What happens when this breaks? How do we know this control operates?'"
> 

> "Auditors ask: 'Show me.' Advisors ask: 'How does this work?' That question changes everything."
> 

**[Pause]**

> "Compliance is the exhaust. Security is the engine. If you want compliance, stop chasing compliance. Chase good design, clean scope boundaries, and controls that operate every day."
> 

**Delivery cues:**

- The quote on screen should be the visual anchor
- Deliver "Compliance is the exhaust" slowly and clearly
- This is a philosophical turning point in the talk

---

## Slide 6 — The Prioritized Approach: The Correction

**Visual:**

- Heading: **The Council milestones are a risk overlay—not the build order**
- Six milestones listed with icons
- Callout box: *"Milestones weight effort. Build Up sets dependencies. Assess Down validates outcomes."*

**Speaker notes (3 minutes):**

> "Let's talk about the Prioritized Approach. The Council's six milestones are smart. They group requirements by risk reduction. Milestone 1 attacks data gravity. Milestone 2 protects systems and networks. And so on."
> 

> "But here's the problem: teams treat milestones as the implementation sequence. They do Milestone 1 projects without understanding dependencies. And that causes siloed fixes and late surprises."
> 

> "Let me give you an example. Milestone 1 says 'remove sensitive authentication data and limit data retention.' So you run a data cleanup project. Delete old cardholder data from databases. Mark the milestone complete."
> 

> "Six months later, during assessment prep, Requirement 10 evidence shows PAN in application logs. Requirement 3 evidence shows PAN in backup retention. Requirement 1 analysis shows logs are replicated to an analytics platform—new scope."
> 

> "What happened? Milestone 1 targeted the right risk. But the dependencies weren't honored. Scope wasn't clear. Retention policies weren't enforced at the system level. It was a tactical win and a strategic failure."
> 

**[Pause]**

> "Here's the reconciliation. The Prioritized Approach tells you where risk hurts most. Build Up tells you how to remove it. Assess Down tells you how it will be proven. All three are true at once."
> 

**Delivery cues:**

- Use the Milestone 1 example verbatim—it's concrete and relatable
- The reconciliation line is your signature—deliver it cleanly

---

## Slide 7 — Assess Down: Why Assessments Feel Backwards

**Visual:**

- Heading: **Assessments start at governance and end at architecture**
- Flow diagram showing Req 12 → 11 → 10 → ... → 1
- Key insight in callout: *"Assessors discover architecture last. That's why scope surprises happen late."*

**Speaker notes (3 minutes):**

> "Now let's talk about Assess Down. Assessors don't start at Requirement 1 and march forward. They start at Requirement 12—governance—and work backwards."
> 

> "Why? Because governance defines the program. Policies set expectations. Ownership determines who's accountable. Risk assessments define scope."
> 

> "Then assessors move to Requirements 11 and 10. Testing and monitoring. These prove whether controls actually operate. Are vulnerabilities being found and fixed? Are logs being reviewed? Can you detect misuse of account data?"
> 

> "Finally, assessors validate the foundation. Requirements 1 through 6. Segmentation. Configurations. Data protection. SDLC."
> 

> "By the time they get to Requirement 1, they've already inferred whether your architecture is real or aspirational."
> 

**[Pause]**

> "Requirement 1 is validated last. If your network reality doesn't match your scope assertion, everything unravels. That's why early segmentation validation is critical—even though it happens 'out of order' in Assess Down."
> 

**Delivery cues:**

- Walk through the flow clearly
- Emphasize that segmentation is discovered last but should be validated first

---

## Slide 8 — Essentials vs Signals

**Visual:**

- Two-column layout:
    - Left: **Essentials (Req 1–6)** — Build Zones
    - Right: **Maturity Signals (Req 7–12)** — Signal Zones
- Icons for each requirement group

**Speaker notes (2 minutes):**

> "Here's a practical way to think about this. I split PCI DSS into two categories: Essentials and Signals."
> 

> "Essentials—Requirements 1 through 6—are the build zones. These are foundational controls. Network segmentation. Secure configurations. Data protection. Crypto in transit. Malware defense. Secure SDLC. If these are weak, everything else is compensation."
> 

> "Signals—Requirements 7 through 12—are the maturity zones. Access control. Authentication. Physical security. Logging. Testing. Governance. These reveal whether your program operates continuously or only during assessment prep."
> 

> "Signals don't compensate for weak foundations. They expose them."
> 

**Delivery cues:**

- This framework (Essentials vs Signals) is easy to remember and apply
- Position it as a mental model they can take home

---

## Slide 9 — The Three Failure Modes

**Visual:**

- Heading: **How PCI programs break**
- Three scenarios (brief text):
    1. "We did Milestone 1" (but logs/queues/backups still contain AD)
    2. "Segmentation is a diagram" (but not validated)
    3. "Policies before reality" (beautiful docs, weak enforcement)

**Speaker notes (3 minutes):**

> "Let me show you three failure modes I see repeatedly."
> 

> "Failure Mode 1: 'We did Milestone 1.' Teams run data cleanup projects. But they don't map data flows first. Logs, backups, queues, and endpoints still contain PAN. Milestone 1 looked done, but dependencies weren't honored."
> 

> "Failure Mode 2: 'Segmentation is a diagram.' Network architecture looks clean on paper. Firewall rules documented. Then Requirement 11 penetration testing happens. The tester pivots from an out-of-scope system into the CDE. Segmentation failed. Forty additional systems are suddenly in scope. Six months of remediation."
> 

> "Failure Mode 3: 'Policies before reality.' Organizations invest heavily in governance. Beautiful security policies. Detailed procedures. Requirement 12 looks mature. But during the assessment, evidence shows deployments bypass SDLC gates. Monitoring alerts get ignored. Access reviews rubber-stamp existing state. Policies don't match operational reality."
> 

**[Pause]**

> "Each failure mode is the same root cause: design and validation weren't aligned."
> 

**Delivery cues:**

- These scenarios are case studies—make them concrete
- The pattern ("design and validation weren't aligned") ties back to Build Up / Assess Down

---

## Slide 10 — The Trusted Advisor Operating Loop

**Visual:**

- Circular diagram:
    - Enable → Clarify → Prove → Optimize → [repeat]
- Brief text for each:
    - Enable: Harden, segment, minimize data
    - Clarify: Make scope/flows legible
    - Prove: Evidence generated continuously
    - Optimize: Reduce friction and scope

**Speaker notes (2 minutes):**

> "So how do you fix this? Here's the Trusted Advisor operating loop."
> 

> "First: enable. Build the foundations. Harden systems. Segment networks. Minimize data. Establish secure SDLC."
> 

> "Second: clarify. Make scope and data flows legible. Can you draw a line around cardholder data with confidence? Do you know where data moves?"
> 

> "Third: prove. Evidence should be generated continuously because controls are operating. Not produced seasonally for assessments."
> 

> "Fourth: optimize. Reduce friction. Shrink scope. Eliminate unnecessary data. Make compliance boring."
> 

**[Pause]**

> "This is how you turn PCI into business-as-usual instead of seasonal panic."
> 

**Delivery cues:**

- Walk through the loop clockwise
- Emphasize "make compliance boring"—that's the goal

---

## Slide 11 — The Mantra

**Visual:**

- Large, centered quote:
    - **"Compliance is the exhaust. Security is the engine."**
- No other text

**Speaker notes (1 minute):**

> "Let me leave you with this."
> 

**[Long pause, let the slide settle]**

> "Compliance is the exhaust. Security is the engine."
> 

> "If you want compliance, stop chasing compliance. Chase good design. Chase clean scope boundaries. Chase controls that operate every day."
> 

> "When you build systems where security is real, compliance becomes a byproduct. It emits."
> 

**Delivery cues:**

- This is the emotional peak of the talk
- Slow delivery, clear enunciation
- Let the silence work for you

---

## Slide 12 — Call to Action

**Visual:**

- Heading: **Build Up early. Assess Down continuously. Use milestones intelligently.**
- Three bullet points:
    - Don't prepare for an assessment. Design for truth.
    - Don't start with policies. Start with architecture.
    - Don't wait for Req 11 to validate Req 1.
- Contact info / QR code for resources

**Speaker notes (2 minutes):**

> "Here's what I want you to do."
> 

> "First: Build Up early. Validate your foundations before you build higher-layer controls. Don't assume segmentation works—test it. Don't assume data is minimized—prove it."
> 

> "Second: Assess Down continuously. Generate evidence as a system output, not a seasonal artifact. If your monitoring only produces reports during assessment prep, it's not monitoring."
> 

> "Third: Use milestones intelligently. They tell you where risk hurts most. But honor dependencies. Don't mark Milestone 1 complete if data still exists in logs. Don't mark Milestone 2 complete if segmentation isn't tested."
> 

**[Pause]**

> "Don't prepare for an assessment. Design for truth. Then the assessment just confirms what you already know."
> 

> "Thank you."
> 

**Delivery cues:**

- Concrete, actionable guidance
- End strong and clear
- Open for Q&A

---

# Q&A Preparation

## Anticipated Questions

**Q: "Is this framework officially endorsed by the PCI Council?"**

A: "This is a dependency-based interpretation of PCI DSS. It doesn't replace the standard—it explains how controls actually work in systems. The Prioritized Approach is Council guidance. Build Up and Assess Down are mental models for understanding design and validation flows."

---

**Q: "How do I convince leadership to invest in Build Up when we're under assessment pressure?"**

A: "Show them the failure modes. Ask: would you rather pay now for architecture, or pay later when scope expands by 40 systems? The cost of late discovery is always higher than the cost of early validation."

---

**Q: "What if our assessor doesn't think this way?"**

A: "Good assessors already do. They start at governance and work backwards. If your assessor only asks for evidence without understanding your system, that's a signal. Build Up and Assess Down make their job easier because you're speaking the same language."

---

**Q: "Where do I start if my program is already in chaos?"**

A: "Three checkpoints. First: validate Requirement 1 scope—do you actually know your boundaries? Second: run data discovery—where does account data really exist? Third: test one control end-to-end—pick logging or access reviews and prove it operates continuously. That'll expose your biggest gaps."

---

**Q: "How does this apply to v4.0.1?"**

A: "v4.0.1 rewards this thinking. The shift to customized approaches and continuous validation aligns perfectly with Build Up / Assess Down. Design for outcomes, not checkboxes. That's what the Council is pushing toward."

---

# Post-Talk Resources

**Materials to share:**

- Field Kit (templates)
- Facilitator Guide (for internal training)
- Failure mode case studies
- Dependency map (one-pager)

**Follow-up engagement:**

- 90-minute workshop
- Assessment readiness review
- Trusted Advisor consulting

---

# Delivery Checklist

**Before you present:**

- [ ]  Master diagram renders correctly
- [ ]  Timing rehearsed (aim for 40–42 minutes to leave Q&A buffer)
- [ ]  Key phrases memorized (compliance is the exhaust, you don't start with policies, etc.)
- [ ]  Failure mode examples ready
- [ ]  Energy level: conversational but authoritative

**During presentation:**

- [ ]  Pause after key insights
- [ ]  Make eye contact during pivotal lines
- [ ]  Use the diagram to anchor explanations
- [ ]  Invite participation (hand-raise on Slide 2)

**After presentation:**

- [ ]  Capture questions for refinement
- [ ]  Note which examples landed strongest
- [ ]  Collect contact info for follow-up
- [ ]  Debrief: what worked, what to adjust
