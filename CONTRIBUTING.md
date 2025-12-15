# CONTRIBUTING.md

# Contributing to Build Up / Assess Down

We welcome contributions that strengthen the framework while maintaining Council compatibility and practitioner utility.

---

## How to Contribute

### 1. Case Study Submissions (Additional Failure Modes)

Beyond the three canonical failure modes, we're collecting real-world scenarios that demonstrate dependency violations.

**What we're looking for:**

- Scenario description (anonymized)
- Root cause analysis (which dependency was violated)
- Where Assess Down discovered the issue (late vs. early)
- How Build Up thinking would have prevented it
- Which milestone(s) falsely appeared complete

**Submission process:**

1. Open a GitHub Issue with label `case-study`
2. Use the Case Study template
3. Maintainers will review for inclusion in Field Kit #5 (Failure Mode Library)

**Requirements:**

- Must be anonymized (no client/organization identifiers)
- Must map to PCI DSS v4.x requirements
- Must demonstrate dependency logic (not just "we forgot X")

---

### 2. Workshop Facilitation Experiences

If you've delivered the 90-minute workshop, we want to hear what worked and what didn't.

**Share:**

- Audience composition (practitioners vs. assessors vs. mixed)
- Exercises that landed vs. fell flat
- Questions that surfaced repeatedly
- Timing adjustments you made
- Additional examples you added

**Submission process:**

1. Open a GitHub Discussion in the "Show and Tell" category
2. Title: "Workshop Experience: [Audience Type] [Date]"
3. Maintainers may incorporate feedback into Facilitator Guide updates

---

### 3. Tool Implementations

Have you built tooling that operationalizes the framework?

**Examples:**

- Dependency Map generators
- Evidence Storyboard templates (GRC platform integrations)
- Milestone-weighted backlog trackers
- Automated "dependency blocker" detectors

**Submission process:**

1. Create a repository for your tool
2. Open a GitHub Issue with label `tool-integration`
3. Provide: repo link, description, framework artifact it supports
4. Maintainers will link to community tools from README

**Requirements:**

- Must explicitly reference which framework artifact(s) it supports
- Must include usage documentation
- Should be open-source (preferred but not required)

---

### 4. Cross-Framework Applications

Have you applied Build Up / Assess Down thinking to other compliance frameworks?

**Examples:**

- SOC 2 Type II dependency mapping
- ISO 27001 control relationships
- NIST CSF implementation tiers as "assess down" validation
- CMMC maturity levels as dependency stacks

**Submission process:**

1. Open a GitHub Discussion in the "Ideas" category
2. Title: "Framework Application: [Standard Name]"
3. Describe how the three-lens model maps to the target framework

**What makes a strong submission:**

- Concrete mapping (not just conceptual similarity)
- Identifies where the model breaks or requires adaptation
- Shares practitioner validation (if available)

---

### 5. Documentation Improvements

**We welcome:**

- Typo fixes and clarity improvements
- Additional diagrams or visual aids
- Glossary term additions
- Translation to other languages

**Submission process:**

1. Fork the repository
2. Make your changes
3. Submit a Pull Request with clear description

**Guidelines:**

- Maintain Council-safe language (framework as interpretation, not replacement)
- Preserve existing structure and citation formats
- For significant rewrites, open an Issue first to discuss

---

## What We're NOT Looking For

**Please do not submit:**

- Tool/vendor promotions disguised as contributions
- Content that contradicts PCI SSC guidance
- Implementations that require paid software without free alternatives
- Overly prescriptive "you must do X" guidance (framework is descriptive, not prescriptive)
- Content that breaks Council compatibility (e.g., "ignore the Prioritized Approach")

---

## Code of Conduct

### Expected Behavior

- Be respectful of different perspectives and experience levels
- Focus on what's best for practitioners and the PCI community
- Accept constructive criticism gracefully
- Prioritize framework integrity over personal/vendor interests

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or deliberately derailing discussions
- Sharing non-public assessment findings or client information
- Misrepresenting framework concepts for commercial gain

**Enforcement:** Maintainers reserve the right to remove contributions or ban contributors who violate these guidelines.

---

## Review Process

### Pull Requests

1. **Submission**: Fork, make changes, submit PR
2. **Initial review**: Maintainers check for alignment with guidelines (1-3 days)
3. **Discussion**: May request changes or clarifications
4. **Merge decision**: Accepted PRs are merged and contributor is credited

### Issues and Discussions

1. **Triage**: Maintainers label and categorize (1-5 days)
2. **Community input**: Open for discussion
3. **Resolution**: Incorporated into framework updates or closed with explanation

---

## Contributor Recognition

**How we credit contributors:**

- **Case studies**: Credited in Field Kit #5 (anonymously or by name, your choice)
- **Significant contributions**: Added to README Acknowledgments section
- **Tool integrations**: Linked from README with attribution
- **Documentation improvements**: Git commit history preserves authorship

---

## Framework Versioning

We follow semantic versioning for major framework updates:

- **Major (2.0)**: Core model changes, new lens additions
- **Minor (1.1)**: New artifacts, significant content additions
- **Patch (1.0.1)**: Typo fixes, clarifications, link updates

Contributors to minor/major releases will be acknowledged in [CHANGELOG.md](./CHANGELOG.md).

---

## Maintainer Team

**Current maintainers:**

- Scott Norton (Framework author)

**Interested in becoming a maintainer?**

After demonstrating consistent, high-quality contributions, you may be invited to join the maintainer team. Maintainers:

- Review and merge PRs
- Triage Issues and Discussions
- Ensure framework integrity and Council compatibility
- Participate in versioning decisions

---

## Questions?

Not sure if your contribution fits? Open a GitHub Discussion in the "Q&A" category and ask before investing significant effort.

---

## License Agreement

By contributing, you agree that your contributions will be licensed under the same [CC BY 4.0 license](./LICENSE) as the framework itself.

---

**Thank you for helping make PCI DSS compliance less theatrical and more operational.**
