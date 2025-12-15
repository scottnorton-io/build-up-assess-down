# Field Kit

**Titanium Framework v1.0 — Practitioner Edition**

This field kit contains copy-paste-ready templates for applying the Build Up / Assess Down model to real PCI DSS programs.

---

## Contents

1. Build Up Dependency Map
2. Assess Down Evidence Storyboard
3. Milestone-Weighted Remediation Ledger
4. Trusted Advisor Question Conversion Bank
5. Three Canonical Failure Modes (Case Library)

---

# 1. Build Up Dependency Map

**Purpose:** Understand how PCI DSS requirements depend on each other during design and implementation.

**How to use:** For each requirement in your scope, identify its dependency role, blast radius if weak, and early validation checkpoint.

---

## Requirements 1–2: Foundation Layer

### Requirement 1 — Network Security Controls

**Dependency role:** Defines enforceable scope boundaries

**If weak, then:** Every other requirement's scope becomes unreliable; compensating controls multiply; assessment scope expands late

**Early validation checkpoint:** Segmentation effectiveness validation before Req 11 testing (penetration test, network scan verification)

**Design questions:**

- Can you draw a line around cardholder data flows with confidence?
- Do firewall rules actually enforce that boundary?
- Has segmentation been tested, not just documented?

---

### Requirement 2 — Secure Configurations

**Dependency role:** Establishes baseline operational reality for all systems

**If weak, then:** Every control above compensates for broken foundations; drift becomes endemic; change control ineffective

**Early validation checkpoint:** Config baseline validation + automated compliance scanning before building higher-layer controls

**Design questions:**

- Are secure configurations defined and enforced?
- Can you detect configuration drift automatically?
- Do new systems inherit secure baselines by default?

---

## Requirements 3–4: Data Gravity Layer

### Requirement 3 — Protect Stored Account Data

**Dependency role:** Controls data gravity; defines what must be protected

**If weak, then:** Scope spreads to logs, backups, queues, endpoints; encryption becomes complex; retention violations accumulate

**Early validation checkpoint:** Data discovery + retention enforcement evidence before claiming Milestone 1 complete

**Design questions:**

- Where does account data actually exist (not just where it should)?
- Are retention policies enforced automatically?
- Do logs, backups, and queues respect data minimization?

---

### Requirement 4 — Protect Account Data in Transit

**Dependency role:** Protects data flows across boundaries

**If weak, then:** Data exposure in transit; man-in-the-middle risks; encryption gaps at system boundaries

**Early validation checkpoint:** Crypto validation across all identified data flows (from Req 1 boundary analysis)

**Design questions:**

- Do you know all paths account data travels?
- Is strong crypto enforced end-to-end?
- Are cipher suites and protocols current?

---

## Requirements 5–6: Operational Hygiene Layer

### Requirement 5 — Protect All Systems from Malware

**Dependency role:** Prevents control degradation via compromise

**If weak, then:** All prior design work can be undermined; detection gaps; lateral movement risk

**Early validation checkpoint:** AV/EDR deployment + detection validation before claiming systems are "protected"

**Design questions:**

- Are anti-malware controls deployed and updated?
- Can you detect malware activity, not just signatures?
- Do controls cover all system types (Linux, containers, etc.)?

---

### Requirement 6 — Develop and Maintain Secure Systems and Software

**Dependency role:** Keeps controls alive through change; immune system of the program

**If weak, then:** Security degrades with each release; vulnerabilities accumulate; SDLC bypasses emerge

**Early validation checkpoint:** SDLC evidence + change control validation before deploying to production

**Design questions:**

- Is security integrated into development workflows?
- Are vulnerabilities identified and remediated systematically?
- Does change control actually prevent unauthorized modifications?

---

## Requirements 7–9: Access Control Layer

### Requirement 7 — Restrict Access by Business Need-to-Know

**Dependency role:** Enforces least privilege based on defined scope

**If weak, then:** Over-provisioned access; insider risk; privilege creep; access reviews become theater

**Early validation checkpoint:** Access control model defined + role-based access enforced before scaling users

**Design questions:**

- Is access granted based on job function?
- Can you prove access matches current business need?
- Do access reviews drive actual changes?

---

### Requirement 8 — Identify Users and Authenticate Access

**Dependency role:** Establishes identity as foundation for access control

**If weak, then:** Logging becomes unreliable; access control unenforceable; accountability breaks down

**Early validation checkpoint:** MFA deployment + identity lifecycle validation before claiming Req 8 complete

**Design questions:**

- Are all users uniquely identified?
- Is MFA enforced for CDE access?
- Does identity lifecycle (hire/transfer/term) work reliably?

---

### Requirement 9 — Restrict Physical Access to Cardholder Data

**Dependency role:** Controls physical attack surface

**If weak, then:** Technical controls can be bypassed; physical theft risk; console access uncontrolled

**Early validation checkpoint:** Physical security controls validated before declaring CDE locations secure

**Design questions:**

- Are CDE locations physically protected?
- Is physical access logged and monitored?
- Are media destruction processes enforced?

---

## Requirements 10–11: Observability Layer

### Requirement 10 — Log and Monitor All Access to System Components and Cardholder Data

**Dependency role:** Reveals whether lower-layer controls actually operate

**If weak, then:** Incidents go undetected; compliance evidence becomes archaeology; detective controls fail

**Early validation checkpoint:** Logging + SIEM deployment + detection rule validation before claiming monitoring works

**Design questions:**

- Are critical events logged comprehensively?
- Is monitoring active, not just passive log storage?
- Can you detect misuse of account data?

---

### Requirement 11 — Test Security of Systems and Networks Regularly

**Dependency role:** Validates design assumptions and discovers reality

**If weak, then:** False confidence in controls; segmentation failures discovered late; vulnerabilities accumulate

**Early validation checkpoint:** Regular testing cadence established + results drive remediation

**Design questions:**

- Is testing continuous, not just annual?
- Do test results match design expectations?
- Does testing include segmentation effectiveness?

---

## Requirement 12: Governance Layer

### Requirement 12 — Support Information Security with Organizational Policies and Programs

**Dependency role:** Amplifies and sustains operational truth

**If weak, then:** Program lacks ownership; risk assessments disconnected from reality; policies become fiction

**Early validation checkpoint:** Governance establishes clear ownership + risk management operates continuously

**Design questions:**

- Do policies reflect operational reality?
- Is ownership clear for each requirement?
- Does risk management drive actual decisions?

---

# 2. Assess Down Evidence Storyboard

**Purpose:** Reframe evidence as continuous system output, not assessment artifacts.

**How to use:** For each requirement, define what decision the evidence supports, where it's generated, who owns it, and how often it should exist.

---

## Evidence Flow Template

### Requirement 12 — Governance & Program

**Decision this evidence supports:** "Does a security program exist with clear ownership?"

**Evidence sources:**

- Security policies (version-controlled, reviewed annually)
- Risk assessment documentation (updated continuously)
- Ownership matrix (roles and responsibilities defined)
- Training records (completion tracked)

**Owner:** CISO / Security Program Manager

**Cadence:** Continuous operation; quarterly review; annual formal update

**Titanium insight:** If program artifacts only exist during assessment prep, the program doesn't exist.

---

### Requirement 11 — Testing Security

**Decision this evidence supports:** "Are security controls tested and validated regularly?"

**Evidence sources:**

- ASV scan results (quarterly, passing)
- Internal vulnerability scan results (quarterly + after significant change)
- Penetration test reports (annual, includes segmentation)
- File integrity monitoring alerts (continuous)

**Owner:** Security Operations / IT

**Cadence:** Quarterly minimum; continuous for FIM

**Titanium insight:** Testing should expose problems during normal operations, not during assessments.

---

### Requirement 10 — Logging & Monitoring

**Decision this evidence supports:** "Can we detect and respond to misuse of account data?"

**Evidence sources:**

- SIEM correlation rules (documented, tested)
- Log retention evidence (centralized, protected)
- Alert review records (incidents investigated)
- Detection validation (rules tested against scenarios)

**Owner:** Security Operations Center (SOC)

**Cadence:** Continuous monitoring; daily review; quarterly detection validation

**Titanium insight:** Logs without detection are storage, not security.

---

### Requirements 7–9 — Access Controls

**Decision this evidence supports:** "Is access to account data controlled and monitored?"

**Evidence sources:**

- Access control matrices (role-based, documented)
- MFA logs (coverage validated)
- Access review records (quarterly, with revocations)
- Physical access logs (badge system, visitor logs)

**Owner:** Identity and Access Management (IAM) / Facilities

**Cadence:** Continuous enforcement; quarterly access reviews

**Titanium insight:** Access reviews should drive real changes, not rubber-stamp existing state.

---

### Requirement 6 — Secure SDLC

**Decision this evidence supports:** "Is change controlled and security-tested?"

**Evidence sources:**

- SDLC documentation (security gates defined)
- Vulnerability scan results (pre-production testing)
- Change tickets (approval workflow enforced)
- Patch management records (timely remediation)

**Owner:** Engineering / DevOps / Change Management

**Cadence:** Per-change validation; monthly patching cycles

**Titanium insight:** If deployments bypass SDLC, the control is aspirational.

---

### Requirement 5 — Malware Defense

**Decision this evidence supports:** "Are systems protected from and monitored for malware?"

**Evidence sources:**

- AV/EDR deployment evidence (coverage validated)
- Signature/definition update logs (current)
- Malware detection alerts (investigated)
- Phishing simulation results (user awareness tested)

**Owner:** Security Operations / IT

**Cadence:** Continuous operation; daily/weekly reviews

**Titanium insight:** Anti-malware must detect threats, not just exist.

---

### Requirements 3–4 — Data Protection

**Decision this evidence supports:** "Is account data minimized, protected at rest, and protected in transit?"

**Evidence sources:**

- Data discovery results (where AD actually exists)
- Encryption validation (at rest + in transit)
- Retention policy enforcement (automated deletion)
- Key management procedures (rotation, access control)

**Owner:** Data Governance / Engineering

**Cadence:** Quarterly data discovery; continuous encryption enforcement

**Titanium insight:** Data you didn't know existed can't be protected.

---

### Requirement 2 — Secure Configurations

**Decision this evidence supports:** "Are systems hardened and drift-controlled?"

**Evidence sources:**

- Configuration baselines (documented, enforced)
- Compliance scan results (automated checks)
- Configuration management database (CMDB) records
- Remediation tracking (drift corrected)

**Owner:** IT Operations / Platform Engineering

**Cadence:** Continuous enforcement; monthly validation

**Titanium insight:** Baselines that aren't enforced are documentation, not controls.

---

### Requirement 1 — Network Security Controls

**Decision this evidence supports:** "Is scope accurately defined and segmentation effective?"

**Evidence sources:**

- Network diagrams (current, validated)
- Firewall rule reviews (least-privilege enforced)
- Segmentation testing results (penetration test, network scans)
- Data flow documentation (matches reality)

**Owner:** Network Engineering / Security Architecture

**Cadence:** Annual segmentation testing; quarterly firewall reviews; continuous enforcement

**Titanium insight:** Segmentation is validated last in assessments—validate it early in design.

---

# 3. Milestone-Weighted Remediation Ledger

**Purpose:** Prevent milestone theater by explicitly tracking dependencies.

**How to use:** For each remediation item, document which dependency it relies on, which milestone it supports, risk reduced, and any dependency blockers.

---

## Ledger Template

| Remediation Item | Req Dependency | Milestone | Risk Reduced (Blast Radius × Likelihood) | Dependency Blocker | Status |
| --- | --- | --- | --- | --- | --- |
| Data retention cleanup (PAN in logs) | Req 3 (data protection) + Req 10 (logging) | M1, M5 | High × High = Critical | Requires Req 1 scope clarity first | Blocked |
| Implement MFA for CDE access | Req 8 (authentication) | M4 | Medium × High = High | Requires Req 7 access model defined | Ready |
| Segmentation effectiveness testing | Req 1 (NSC) + Req 11 (testing) | M2 | Critical × Medium = High | None—should be done early | In Progress |
| SDLC security gate implementation | Req 6 (secure SDLC) | M3 | Medium × Medium = Medium | Requires Req 2 baselines established | Blocked |
| SIEM correlation rule deployment | Req 10 (monitoring) | M4 | High × Medium = High | Requires Req 8 identity + Req 7 access controls | Blocked |
| Quarterly access reviews | Req 7 (access control) | M4 | Medium × Low = Medium | Requires Req 8 identity lifecycle working | Ready |

---

## How to Use This Ledger

**Identify dependency blockers:**

- If Req 1 scope is unclear, don't claim data minimization (M1) is complete
- If Req 2 baselines don't exist, SDLC gates (M3) will be ineffective
- If Req 7/8 access controls are weak, monitoring (M4) generates noise

**Prioritize by risk + dependency:**

- High risk + no blockers = do now
- High risk + blockers = resolve blockers first
- Low risk + blockers = defer until dependencies resolve

**Avoid milestone theater:**

- Don't mark M1 complete if PAN still exists in logs/backups
- Don't mark M2 complete if segmentation isn't tested
- Don't mark M4 complete if monitoring can't detect misuse

---

# 4. Trusted Advisor Question Conversion Bank

**Purpose:** Shift from auditor thinking to advisor thinking.

**How to use:** Practice converting compliance questions into design questions.

---

## Question Conversions

### Requirement 1 — Network Security Controls

**Auditor question:** "Show me your network diagram and firewall rules."

**Advisor question:** "How do you know segmentation is effective when the network changes?"

**Why it matters:** Diagrams show intent; testing shows reality.

---

### Requirement 3 — Protect Stored Account Data

**Auditor question:** "Do you retain PAN?"

**Advisor question:** "Where would PAN show up if retention controls failed?"

**Why it matters:** Retention policies are aspirational until enforcement is automated.

---

### Requirement 6 — Secure SDLC

**Auditor question:** "Do you have a secure development lifecycle?"

**Advisor question:** "What happens when developers need to ship fast—does security get bypassed?"

**Why it matters:** SDLC gates that get skipped under pressure aren't controls.

---

### Requirement 7 — Access Control

**Auditor question:** "Show me your last quarterly access review."

**Advisor question:** "How do you know access still matches job function after org changes?"

**Why it matters:** Access reviews are theater if they don't drive revocations.

---

### Requirement 10 — Logging & Monitoring

**Auditor question:** "Are you logging critical events?"

**Advisor question:** "If account data were exfiltrated today, how long until you'd know?"

**Why it matters:** Logging without detection is compliance theater.

---

### Requirement 11 — Testing Security

**Auditor question:** "Show me your last penetration test."

**Advisor question:** "Do pen test findings change how you design systems, or just create remediation tickets?"

**Why it matters:** Testing should inform design, not just validate point-in-time compliance.

---

### Requirement 12 — Governance & Policies

**Auditor question:** "Is this documented in policy?"

**Advisor question:** "What happens when this process breaks—does anyone notice?"

**Why it matters:** Policies that don't match operational reality are fiction.

---

## Practice Exercise

For each requirement in your scope:

1. Write the typical auditor question
2. Convert it to an advisor question that probes operational reality
3. Ask your team the advisor question—what do you learn?

---

# 5. Three Canonical Failure Modes (Case Library)

**Purpose:** Learn from predictable failure patterns.

**How to use:** Study each scenario, identify where dependencies broke, and how Build Up / Assess Down would prevent recurrence.

---

## Failure Mode #1: "We Did Milestone 1"

### Scenario

Organization runs a Milestone 1 (Remove SAD / Limit Retention) project:

- Data retention policies updated
- Old cardholder data purged from primary databases
- Project marked complete
- Leadership celebrates risk reduction

Six months later during assessment prep:

- Req 10 review shows PAN in application logs
- Req 3 audit shows PAN in backup retention (90 days)
- Req 1 analysis shows logs replicated to analytics platform (new scope)
- Milestone 1 status: **failed**

### Root Cause (Dependency Violated)

**Build Up failure:**

- Req 1 (scope) wasn't clear—data flows to logs/backups/analytics not mapped
- Req 3 (data protection) policy didn't cover all storage locations
- Tactical cleanup without architectural fix

**Assess Down discovery:**

- Req 10 evidence (logs) exposed retention violations
- Req 3 evidence (backups) exposed policy gaps
- Req 1 evidence (scope validation) exposed new in-scope systems

### How Build Up / Assess Down Prevents This

**Build Up (design correctly):**

- Map all data flows **before** data cleanup (Req 1 dependency)
- Enforce retention policies at **system level** (Req 3 architecture)
- Validate logs, queues, backups, endpoints **as part of M1**

**Assess Down (validate early):**

- Test Req 3 retention enforcement in logs/backups **before** claiming M1 complete
- Validate Req 1 scope includes downstream data stores
- Generate evidence continuously, not seasonally

**Milestone lesson:**

- M1 targets the right risk (data gravity)
- But without Req 1 scope clarity + Req 3 architectural enforcement, it's tactical theater

---

## Failure Mode #2: "Segmentation Is a Diagram"

### Scenario

Organization has a clean network architecture:

- CDE clearly segmented on paper
- Firewall rules documented
- Req 1 assessment prep looks solid

Req 11 annual penetration test:

- Tester compromises out-of-scope workstation
- Pivots through misconfigured routing to CDE database
- Segmentation: **failed**
- Scope expansion: 40+ additional systems now in scope
- Remediation cost: 6 months + significant expense

### Root Cause (Dependency Violated)

**Build Up failure:**

- Req 1 was documented, not **validated**
- Segmentation effectiveness assumed, not tested
- Treated Req 1 as a documentation exercise, not an architectural control

**Assess Down discovery:**

- Req 11 testing (last in Assess Down flow) revealed Req 1 reality
- Architecture was inferred late, not confirmed early

### How Build Up / Assess Down Prevents This

**Build Up (design correctly):**

- Treat Req 1 as **foundation dependency**—validate early
- Test segmentation effectiveness during design, not just annually
- Use Req 11 methods (penetration testing, network scanning) as **design validation**, not just compliance checkbox

**Assess Down (validate early):**

- Don't wait until Req 11 annual test to discover Req 1 reality
- Implement continuous segmentation validation (quarterly network scans, rule reviews)
- Validate scope boundaries before building controls on top

**Milestone lesson:**

- M2 (Protect Systems & Networks) looked complete
- But segmentation **effectiveness** was assumed, not proven
- Dependencies (Req 1 validation) were ignored

---

## Failure Mode #3: "Policies Before Reality"

### Scenario

Organization invests heavily in Req 12 (Governance):

- Beautiful security policies
- Detailed procedures
- Governance framework documented
- Risk assessments conducted
- Req 12 looks mature

During assessment:

- Req 6 SDLC evidence shows deployments bypassing security gates
- Req 10 monitoring evidence shows alerts ignored
- Req 7 access reviews show no revocations (rubber-stamped)
- Assessment finding: **policies don't match operational reality**
- Compensating controls required across multiple requirements

### Root Cause (Dependency Violated)

**Build Up failure:**

- Started at Req 12 (governance) instead of Req 1–6 (foundations)
- Policies codified aspirations, not operational truth
- Governance amplified fiction, not reality

**Assess Down discovery:**

- Req 12 artifacts looked strong
- But Req 6/7/10 evidence contradicted policy claims
- Program maturity was theater

### How Build Up / Assess Down Prevents This

**Build Up (design correctly):**

- **Don't start with policies—end with them**
- Build Req 1–6 foundations first (scope, config, data, SDLC)
- Use Req 12 to codify and amplify what's **already working**

**Assess Down (validate early):**

- Test whether technical controls (Req 1–11) actually operate
- Use Req 12 governance to drive accountability, not create documents
- Evidence should prove operation, not just policy existence

**Milestone lesson:**

- M6 (Maintain InfoSec Policy) was prioritized early
- But without technical reality (M1–M5), governance is fiction
- Dependencies (build foundations first) were reversed

---

## Pattern Recognition Exercise

For each failure mode:

1. Identify which **Build Up dependency** was violated
2. Identify where **Assess Down** discovered the failure
3. Identify which **milestone** looked complete but wasn't
4. Design a prevention strategy using the framework

---

## Summary: Using the Field Kit

**Dependency Map:** Understand how requirements stack during design

**Evidence Storyboard:** Reframe evidence as continuous system output

**Remediation Ledger:** Avoid milestone theater with dependency tracking

**Question Bank:** Shift from auditor thinking to advisor thinking

**Failure Modes:** Learn from predictable patterns

**Key principle:** Build Up creates reality. Assess Down proves it. Milestones weight risk. Compliance emits from good design.
