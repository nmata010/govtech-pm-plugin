---
name: feature-spec
description: Write structured product requirements documents (PRDs) and feature specifications for federal digital services. Incorporates federal compliance mapping (Section 508, FISMA/FedRAMP, ATO), acquisition alignment (PWS/SOO, QASP, contract vehicle constraints), government stakeholder analysis, and federal user personas. Use when speccing a new feature, writing a PRD, defining acceptance criteria, prioritizing requirements, mapping compliance obligations, or documenting product decisions within a federal contracting environment.
---

# Feature Spec Skill — Federal Digital Services

You are an expert at writing product requirements documents (PRDs) and feature specifications for digital products delivered in a federal government context. You help product managers define what to build, why, and how to measure success — while navigating federal acquisition, compliance, and oversight constraints.

## PRD Structure

A well-structured federal PRD follows this template:

### 1. Problem Statement

- Describe the user problem in 2-3 sentences. Distinguish between public-facing users (citizens, applicants, beneficiaries) and internal government users (case workers, adjudicators, analysts).
- Who experiences this problem, how often, and at what scale.
- What is the cost of not solving it: user burden (time, errors, abandonment), mission impact (backlogs, adjudication delays, compliance gaps), and oversight risk (GAO findings, OIG audits, Congressional interest).
- Ground this in evidence: user research, help desk data, processing time metrics, OIG/GAO findings, or site visits.
- If a Paperwork Reduction Act (PRA) clearance governs data collection from the public, note whether existing research was conducted under an approved PRA package or whether new clearance is required.

### 2. Mission and Policy Alignment

- Connect the feature to the agency's strategic plan, relevant OMB guidance (CX mandates, Zero Trust, AI directives), or legislative requirements.
- If this feature responds to a GAO recommendation, OIG finding, or Congressional directive, cite it. These create urgency and justify prioritization.
- Reference Digital Services Playbook principles this feature advances.

### 3. Acquisition Context

- Identify the contract vehicle (IDIQ task order, BPA call, OTA, in-house, hybrid).
- Map the feature to the relevant PWS/SOO language and CLIN(s). If the feature falls outside current scope, flag that a modification or new task order is required.
- Note Period of Performance implications and pricing model constraints (LPTA, T&M, FFP).

### 4. Goals

- 3-5 specific, measurable outcomes.
- Distinguish between **user goals** (reduced burden, faster access), **mission goals** (throughput, backlog reduction, data quality), and **compliance goals** (508 conformance, FedRAMP authorization, PRA burden reduction).
- Goals should be outcomes, not outputs ("reduce average claim processing time from 45 to 20 days" not "build claims dashboard").
- Where possible, tie goals to metrics already reported to OMB or published on performance.gov.

### 5. Non-Goals

- 3-5 things this feature explicitly will NOT do, with brief rationale (outside PWS, requires separate ATO boundary, needs PRA clearance not yet obtained, deferred to option year).
- Explicitly state what the current ATO boundary covers and what falls outside it.
- In government, documented non-goals provide a defensible basis for declining unfunded scope additions.

### 6. User Stories

Write user stories in standard format: "As a [user type], I want [capability] so that [benefit]"

#### Government-Specific Personas

Be precise about federal user types:

- **Public-facing**: Citizens, applicants, beneficiaries, claimants, filers, authorized representatives (lawyers, accountants), intermediaries (congressional caseworkers, VSOs, navigators)
- **Internal government**: Case workers, adjudicators, supervisors, QA reviewers, program analysts, ISSOs/ISSMs
- **Oversight**: CORs, inspectors general, Congressional staff

#### Government-Specific Guidelines

- Include Section 508 / WCAG 2.1 AA scenarios as first-class stories, not afterthoughts.
- Include edge cases for low-bandwidth field offices and users with limited English proficiency.
- Do not conflate the COR with the end user. The COR monitors contract performance; they are a stakeholder unless the product is a contract oversight tool.

#### Examples

- "As a benefits applicant, I want to check the status of my pending claim online so that I do not need to call the 1-800 number and wait on hold."
- "As a case worker, I want to see all documents for a case in a single view so that I can adjudicate without switching between three legacy systems."
- "As a screen reader user, I want all form fields to have programmatically associated labels so that I can complete the application independently."
- "As a COR, I want to see sprint velocity and burndown metrics so that I can report delivery progress to the CO without ad hoc status requests."

### 7. Requirements

**Must-Have (P0)**: Cannot ship without these. Must satisfy the PWS minimum requirements and compliance mandates. Compliance requirements (508, ATO controls, PRA) are P0 by default — you cannot ship a non-compliant federal system and fix it later.

**Should-Have (P1)**: Core use case works without them. Strong candidates for the next sprint within the current Period of Performance.

**Future Considerations (P2)**: Out of scope for this version. Often align with option year scope or future task orders. Document to prevent architectural decisions that make them hard later.

For each requirement: clear behavioral description, acceptance criteria, technical constraints (PIV/CAC, Login.gov, hosting environment), dependencies (other teams, contracts, agencies, shared services), and triggered compliance requirements.

### 8. Compliance Requirements

Every federal feature spec must explicitly map compliance obligations.

**Section 508 / Accessibility**
- Must conform to WCAG 2.1 Level AA. Identify components needing testing (forms, data tables, interactive widgets, PDFs, charts).
- Specify testing approach: automated (axe, Lighthouse), manual with assistive technology (JAWS, NVDA, VoiceOver), and usability testing with users who have disabilities.

**Security and ATO**
- Does this feature fall within an existing ATO boundary or require a new/modified one?
- If new or modified: FISMA impact level, FedRAMP applicability, net-new NIST 800-53 controls triggered (PII storage, API interfaces, authentication).
- Determine if a Significant Change Request is required. If so, ISSO/ISSM and AO approval is a blocking dependency.
- Build security documentation into sprint workflow — not as a post-development gate.

**Privacy**
- Does the feature handle PII? If yes, confirm existing PIA coverage or flag a new/updated PIA as a dependency. Determine SORN applicability.

**PRA**
- If the feature collects information from 10+ members of the public, PRA clearance is likely required. PRA takes 6-9 months — this is a hard scheduling constraint.

### 9. Success Metrics

#### QASP-Aligned Metrics

Feature metrics should roll up to QASP performance standards:
- **SLAs**: Uptime, response time, incident response time
- **Quality**: Defect rate, test coverage, accessibility conformance rate
- **Delivery**: Sprint velocity consistency, committed stories delivered
- **User satisfaction**: Task completion rate, satisfaction score, help desk volume
- **Security**: Mean time to remediate vulnerabilities, continuous monitoring compliance

#### Government-Specific Outcome Metrics

- **Channel shift**: % of transactions moving from paper/phone/in-person to digital
- **Processing time reduction**: End-to-end case processing time vs. baseline
- **Backlog reduction**: Change in pending case/application volume
- **Cost per transaction**: Unit cost of processing a single case/application
- **CX survey scores**: OMB A-11 Section 280 mandated customer experience surveys
- **Help desk / call center volume**: Reduction in support contacts
- **Congressional inquiry volume**: Reduction in casework inquiries for this process
- **Compliance posture**: Open POA&Ms closed, audit findings resolved

#### Setting Targets

- Base on the current baseline. If none exists, the first goal is to establish one.
- Align evaluation checkpoints with QASP reporting periods and COR surveillance schedules.
- Be prepared to report metrics to the COR, program office, and potentially OMB or Congress.

### 10. Stakeholder Map

| Stakeholder | Interest | Approval Authority |
|---|---|---|
| Product Owner / Program Manager | Mission outcomes, user satisfaction | Feature scope and priority |
| Contracting Officer (CO/KO) | PWS compliance, cost management | Contract modifications, scope changes |
| COR | Delivery quality, QASP metrics | Sprint acceptance, deliverable approval |
| ISSO / ISSM | ATO boundary, control implementation | Security authorization |
| Authorizing Official (AO) | System risk posture | ATO decision |
| 508 Program Manager | WCAG conformance | Accessibility sign-off |
| Privacy Officer | PIA/SORN adequacy | Privacy authorization |
| Program leadership (SES) | Congressional interest, administration priorities | Launch go/no-go |

### 11. Open Questions

Tag each with who should answer: engineering, design, COR, CO, ISSO, privacy officer, 508 coordinator, legal, program office, or another agency/shared service.

Distinguish between:
- **Blocking**: Must answer before development starts ("Does this require a new ATO boundary?" "Is PRA clearance required?")
- **Non-blocking**: Can resolve during implementation
- **Cross-contract**: Requires coordination with another contractor or agency

### 12. Timeline Considerations

- Hard deadlines: Congressional reporting dates, fiscal year end (September 30), OMB memo deadlines, ATO expiration dates.
- Acquisition milestones: Option year exercise dates, task order expiration, recompete timeline.
- Risk: If work spans the base period into an option year, the option may not be exercised.
- Align phasing with sprint boundaries and QASP reporting periods.

## Acceptance Criteria — Government Additions

Use standard Given/When/Then or checklist format. In federal systems, always include:

- **Accessibility criteria**: Reference specific WCAG success criteria (e.g., 1.3.1, 4.1.3, 1.4.3).
- **Security criteria**: Role-based access enforcement, audit logging for data creation/modification/deletion, authentication requirements.
- **Negative test cases**: Unauthorized access attempts are denied and logged. PII is not exposed in error messages or URLs.

**Example — checklist format**:
- [ ] Applicant can enter confirmation number on status check page
- [ ] Invalid confirmation number shows clear error message (not a stack trace)
- [ ] All form fields have programmatically associated labels (WCAG 1.3.1)
- [ ] Error messages announced to screen readers via aria-live (WCAG 4.1.3)
- [ ] Unauthenticated requests return 401
- [ ] All status check requests logged with timestamp and IP for audit
- [ ] Page loads in under 2 seconds on a standard government network

## Requirements Categorization — Federal Adaptation

The base MoSCoW framework applies with these adjustments:

- **Must have** includes baseline 508 conformance and security controls within the ATO boundary. These are non-negotiable.
- **Won't have (this time)** should cite the mechanism for future inclusion (option year scope, follow-on task order, contract modification).
- If everything is P0, nothing is P0. This is especially dangerous in government — overloaded scope leads to missed deadlines, which triggers oversight scrutiny.
- Compliance requirements do not get deprioritized. You cannot defer 508 or security controls to a future sprint.

## Scope Management — Federal Context

### Government-Specific Scope Risks

- A government stakeholder requests a feature outside the PWS. The team builds it to maintain the relationship, but it is unfunded work.
- "Small" additions exceed funded hours or FFP ceiling without a contract modification.
- The ATO boundary expands to cover new functionality without a Significant Change Request.
- Another contractor's delay forces your team to absorb their scope.

### Preventing Scope Creep

- Every requirement must trace to authorized work in the PWS/SOO.
- Any scope addition requires a scope removal, a contract modification, or a timeline extension — documented with the COR.
- When a stakeholder requests out-of-scope work, respond with: "We agree this is valuable. Here is what it would take to add it, and here is what we would need to defer or modify in the contract to accommodate it."
- Track scope changes in a decision log the COR can reference.
- Review the parking lot during option year planning or task order development.
