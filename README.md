# Build Up, Assess Down

### A Dependency-Based Operating Model for PCI DSS Compliance

> **Core thesis:** When security controls are designed with dependency awareness and validated continuously, compliance becomes a byproduct of operational truth rather than a seasonal scramble for evidence.
> 

**Status:** Production-ready • v1.0 Titanium • Q1 2026 Beta Launch

[Read the Paper](#paper) • [Facilitator Guide](#workshop-materials) • [Field Kit](#field-kit) • [Citation](#citation)

---

## The Problem

Organizations subject to PCI DSS routinely experience three predictable surprises:

- **Scope expands late** in the assessment cycle
- **Data appears** in unexpected locations (logs, backups, queues, endpoints)
- **Evidence becomes archaeology** rather than operational output

These are not compliance failures—they are **design failures** that PCI DSS exposes.

---

## The Framework

**Build Up / Assess Down** reconciles three critical perspectives that are often misaligned:

### The Three-Lens Model

```mermaid
flowchart TB
  subgraph BU["BUILD UP (Design Reality) — Req 1 → 12"]
    R1["Req 1: Network Security Controls<br/>(Foundation)"] --> R2["Req 2: Secure Configurations<br/>(Foundation)"]
    R2 --> R3["Req 3: Protect Stored Account Data<br/>(Data Gravity)"]
    R3 --> R4["Req 4: Protect AD in Transit<br/>(Data Gravity)"]
    R4 --> R5["Req 5: Protect from Malware<br/>(Operational Hygiene)"]
    R5 --> R6["Req 6: Secure Systems & Software<br/>(Operational Hygiene)"]
    R6 --> R7["Req 7: Need-to-Know Access<br/>(Access Control)"]
    R7 --> R8["Req 8: Identity + Authentication<br/>(Access Control)"]
    R8 --> R9["Req 9: Physical Access<br/>(Access Control)"]
    R9 --> R10["Req 10: Log & Monitor<br/>(Observability)"]
    R10 --> R11["Req 11: Test Security<br/>(Observability)"]
    R11 --> R12["Req 12: Security Policies & Programs<br/>(Governance)"]
  end

  subgraph AD["ASSESS DOWN (Validate Reality) — Req 12 → 1"]
    A12["Req 12: Governance defines scope"] --> A11["Req 11: Testing proves reality"]
    A11 --> A10["Req 10: Monitoring shows operation"]
    A10 --> A9["Req 9: Physical controls evidence"]
    A9 --> A8["Req 8: Identity evidence"]
    A8 --> A7["Req 7: Access control evidence"]
    A7 --> A6["Req 6: SDLC evidence"]
    A6 --> A5["Req 5: Malware controls evidence"]
    A5 --> A4["Req 4: Crypto evidence"]

**Status:** Production-ready • Q1 2026 Beta Launch • [View Roadmap](implementation/q1-2026-roadmap.md)
