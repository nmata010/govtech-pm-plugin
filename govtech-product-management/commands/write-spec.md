---
description: Write a federal feature spec or PRD with compliance mapping and acquisition context
argument-hint: "<feature or problem statement>"
---

# Write Spec

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Write a feature specification or product requirements document (PRD) for a federal digital service.

## Workflow

### 1. Understand the Feature

Ask the user what they want to spec. Accept any of:
- A PWS/SOO task area deliverable ("Online application portal per PWS 3.2")
- A mandate-driven requirement ("OMB memo M-24-XX requires accessible digital forms by Q3")
- A finding remediation ("GAO-24-XXXXX recommends reducing processing backlog")
- A problem statement ("Applicants abandon the form at step 4 because it requires documents they don't have")
- A user need ("Field office staff need to process renewals without switching between three systems")
- A vague idea ("We should reduce the burden on call center staff")

### 2. Gather Context

Ask the user for the following. Be conversational — do not dump all questions at once. Ask the most important ones first and fill in gaps as you go:

- **User problem**: What problem does this solve? Who experiences it — the public, agency staff, or both?
- **Target users**: Which user segment(s) does this serve? Consider public-facing users, internal agency staff, and intermediaries (e.g., VSOs, case workers, navigators).
- **Mandate or discretionary**: Is this required by law, regulation, Executive Order, OMB policy, or a GAO/OIG finding? Or is it a team-identified improvement? This determines whether it can be deprioritized.
- **Evidence basis**: What drives this? GAO/OIG finding, Congressional inquiry, OMB directive, operational data, user research, COR direction?
- **Acquisition context**: Which PWS/SOO task area does this fall under? Which CLIN? Is this within current contract scope or does it require a modification?
- **Compliance surface**: Does this touch public-facing web (Section 508), system boundaries (ATO impact), PII (privacy impact), or public data collection (PRA)?
- **Success metrics**: How will we know this worked? Frame in terms of mission outcomes, not feature adoption.
- **Approval authority**: Who needs to approve — COR, CO, program leadership, ISSO? In what order?
- **Prior art**: Has this been attempted before? Existing solutions, legacy systems, or prior contract efforts?

### 3. Pull Context from Connected Tools

If **~~project tracker** is connected:
- Search for related tickets, epics, or features
- Pull in any existing requirements or acceptance criteria
- Identify dependencies on other work items
- Check mapping to PWS/SOO task areas and CLINs

If **~~knowledge base** is connected:
- Search for related research documents, prior specs, or design docs
- Pull in relevant user research findings (note PRA status of research cited)
- Find related meeting notes or decision records

If **~~design** is connected:
- Pull related mockups, wireframes, or design explorations
- Search for design system components relevant to the feature
- Check existing 508/WCAG compliance patterns in the design system

If these tools are not connected, work entirely from what the user provides. Do not ask the user to connect tools — just proceed with available information.

### 4. Generate the PRD

Produce a structured PRD with these sections. See the **feature-spec** skill for detailed guidance on federal user stories, compliance requirements mapping, acceptance criteria, and QASP-aligned success metrics.

- **Problem Statement**: The user problem, who is affected (public, agency staff, or both), evidence basis, and mission impact of not solving it (2-3 sentences). Note if evidence comes from PRA-cleared research or operational data.

- **Mission and Policy Alignment**: How this maps to agency strategic plan goals, OMB guidance, GAO/OIG findings, Executive Orders, or Digital Services Playbook principles. This establishes the "why" in government terms.

- **Acquisition Context**: Contract vehicle, PWS/SOO task area mapping, applicable CLIN(s), Period of Performance implications, and whether this requires a contract modification. If scope is ambiguous, flag for COR/CO discussion.

- **Goals**: 3-5 specific, measurable outcomes tied to mission metrics (burden reduction, processing time, error rate, backlog, cost per transaction, equity of access). Distinguish between user goals, mission goals, and compliance goals.

- **Non-Goals**: 3-5 things explicitly out of scope, with brief rationale for each. Include rationale for anything deferred to a future period of performance or option year.

- **User Stories**: Standard format ("As a [user type], I want [capability] so that [benefit]"), grouped by federal persona type:
  - **Public-facing users** (applicants, beneficiaries, taxpayers)
  - **Internal agency staff** (processors, reviewers, supervisors)
  - **Intermediaries** (VSOs, navigators, case workers, Congressional caseworkers)
  - **Oversight roles** (COR, ISSO, auditors)

- **Compliance Requirements** (these are P0 by default — not subject to prioritization tradeoffs):
  - **Section 508 / WCAG**: Accessibility requirements for any user-facing component. Every public-facing user story must include 508/WCAG acceptance criteria. These are legal requirements under Section 508 of the Rehabilitation Act, not optional enhancements.
  - **Security / ATO**: Impact on system boundary, new or modified security controls, Assessment & Authorization implications. Engage ISSO early if boundary changes.
  - **Privacy / PII**: Data elements collected or processed, Privacy Impact Assessment requirements, System of Records Notice (SORN) implications.
  - **PRA**: If the feature collects information from 10+ members of the public, a PRA clearance or generic clearance may be required. Identify early — PRA clearance can take 6-12 months.

- **Feature Requirements**: Categorized as Must-Have (P0), Should-Have (P1), and Future Considerations (P2), each with acceptance criteria. Compliance requirements listed above are always P0 and are listed separately to prevent them from being traded off against feature work.

- **Success Metrics**: QASP-aligned where applicable. Include leading indicators (change quickly) and lagging indicators (change over time), with specific targets. Use government-relevant measures: burden reduction (time, steps, cost), processing time, backlog reduction, error/rework rate, channel shift, call center deflection, 508 conformance, CX survey scores.

- **Stakeholder Map**: Who must approve, review, or be informed — with decision authority noted. Typical map: COR (approval), CO (if scope/contract impact), ISSO (if security impact), AO (if ATO impact), program leadership (strategic alignment), 508 coordinator (accessibility review).

- **Open Questions**: Unresolved questions tagged with who needs to answer (COR, CO, ISSO, engineering, design, policy, legal). Flag any questions that block compliance work — these should be resolved first.

- **Timeline Considerations**: Hard deadlines (ATO expiration, fiscal year end, option year exercise, Congressional mandate, OMB reporting deadline), dependencies (cross-contract, shared services, clearance processing), and phasing recommendations. Note if timeline crosses Period of Performance boundaries.

### 5. Review and Iterate

After generating the PRD:
- Ask the user if any sections need adjustment
- Offer to expand on specific sections
- Offer to map requirements to PWS/SOO language for traceability
- Offer to draft QASP-aligned acceptance criteria for COR review
- Offer to prepare a COR review package
- Offer to assess whether the scope requires a contract modification
- Offer to create follow-up artifacts (design brief, engineering ticket breakdown, 508 test plan)

## Output Format

Use markdown with clear headers. Keep the document scannable — busy stakeholders should be able to read just the headers and bold text to get the gist. Compliance Requirements should be visually distinct from Feature Requirements to reinforce that they are non-negotiable.

## Tips

- Be opinionated about scope. It is better to have a tight, well-defined spec than an expansive vague one. In federal context, scope clarity also prevents contract disputes.
- If the user's idea is too big for one spec, suggest breaking it into phases aligned to sprint boundaries or option year periods, and spec the first phase.
- Compliance is infrastructure, not a feature. Section 508, ATO security controls, PRA, and privacy requirements are P0 by default — they are legal obligations, not prioritization decisions. Do not allow them to be deferred or traded off. "We'll add accessibility later" is not an acceptable approach.
- Every feature should trace back to a PWS/SOO task area. If it doesn't map, it may be out of scope — flag this for COR discussion before investing in the spec.
- Success metrics should be specific, measurable, and government-relevant. "Improve user experience" is not a metric. "Reduce average application processing time from 12 days to 4 days" is.
- Non-goals are as important as goals. They prevent scope creep, which in federal contracting can trigger modification requirements.
- Open questions should be genuinely open — do not include questions you can answer from context. Tag each with the specific role who can resolve it.
- PRA constrains what user research you can cite as evidence. If research involved 10+ members of the public without PRA clearance, note this limitation. Operational data and internal staff research are not PRA-constrained.
- Scope additions beyond the current PWS/SOO may require a contract modification through the CO. Identify this early — modifications take time and require funding.
