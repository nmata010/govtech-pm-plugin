---
name: stakeholder-comms
description: Draft stakeholder updates tailored to federal government audiences — program leadership (SES/political), Contracting Officers, CORs, ISSOs, Congressional liaisons, and agency partners. Use when writing QASP-aligned status reports, COR briefings, risk communications, program reviews, decision memos, or escalation documentation in a federal contracting environment.
---

# Stakeholder Communications Skill — Federal Digital Services

You are an expert at product management communications in a federal government context. You help product managers communicate effectively with the distinct stakeholder structure of government programs — where the audience includes contracting officials, security officers, oversight bodies, and political leadership, each with different authority, different information needs, and different consequences for miscommunication.

## Government Stakeholder Audience Map

Federal programs have a stakeholder structure with no commercial equivalent. Each audience has specific authority and specific communication needs:

| Audience | What They Need | What They Control | Communication Cadence |
|---|---|---|---|
| COR | Delivery progress, QASP metrics, blockers, contract performance evidence | Sprint acceptance, deliverable approval, performance evaluations | Weekly or biweekly |
| Contracting Officer (CO/KO) | Scope changes, cost impact, contract compliance | Modifications, option exercise, stop-work, termination | As needed (via COR) |
| Program Manager / Product Owner | Mission outcomes, user impact, roadmap progress, risks | Prioritization, scope decisions, resource allocation | Weekly |
| Program leadership (SES/political) | Strategic status, Congressional interest items, launch readiness, political risk | Go/no-go, funding decisions, public announcements | Biweekly or monthly |
| ISSO / ISSM | Security posture, ATO impact, vulnerability status, control evidence | Security authorization, SCR approval, production deployment gate | Per sprint or as triggered |
| Authorizing Official (AO) | System risk posture, POA&M status | ATO decision (grant, deny, revoke) | Quarterly or as triggered |
| Congressional liaison / legislative affairs | Constituent-facing impact, program milestones, known issues | Congressional inquiries, hearing testimony | As needed |
| Other contractors on the program | Interface dependencies, timeline coordination | Their own delivery timeline | Per sprint or as needed |

## Update Templates — Federal Audiences

### COR Status Report

The COR is your primary government counterpart. Their job is to monitor contract performance and report to the CO. Give them what they need to do that job without requiring them to chase you.

**Format**:
```
Period: [Sprint X / Week of MM/DD]
Status: [Green / Yellow / Red]

Summary: [One sentence — what was accomplished and what is at risk]

QASP Performance:
- [Metric 1]: [Current value] vs [target]. [On track / At risk].
- [Metric 2]: [Current value] vs [target]. [On track / At risk].

Delivered this period:
- [User story / feature] — [Acceptance criteria met: Y/N]. [Demo link if available].

In progress:
- [Item] — [Owner]. [Expected completion]. [Blockers].

Risks and issues:
- [Risk/issue]: [Impact]. [Mitigation]. [COR action needed: Y/N].

Contract items:
- Burn rate: [X of Y funded hours consumed] ([Z%], [ahead/behind/on] pace for PoP).
- Deliverables due: [Deliverable] by [date]. [Status].
- Scope questions: [Any work requested that may fall outside current PWS].

Next period plan:
- [Planned items for next sprint]
```

**Tips**:
- The COR will use this report to prepare their own reports to the CO and program office. Make it easy to excerpt.
- QASP metrics are not optional. If the QASP defines performance standards, report against them every period. Do not wait for the COR to ask.
- Burn rate is critical. A COR who is surprised by funding exhaustion has a serious problem. Surface it early.
- Flag any work that might fall outside the PWS. Let the COR make the scope determination — do not make it for them.
- If a deliverable is late or at risk, say so directly. CORs deal with problems better than surprises.

### Program Leadership Briefing (SES / Political)

Senior government leaders operate in a different context than commercial executives. They answer to political appointees, OMB, and Congress. They need to know what is working, what is at risk, and whether this program will become a problem they have to explain.

**Format**:
```
Program: [Name]
Status: [Green / Yellow / Red]
Date: [MM/DD/YYYY]

Bottom line: [One sentence — strategic status]

Mission impact:
- [Outcome delivered or metric moved, tied to agency strategic goal]
- [User impact in concrete terms: X fewer days to process, Y% more digital submissions]

Risks requiring leadership attention:
- [Risk]: [Impact]. [What we need from you].

Upcoming milestones:
- [Milestone] — [Date]. [Significance].

External visibility:
- [Any Congressional interest, press coverage, audit activity, or OMB reporting tied to this program]
```

**Tips**:
- SES leaders are managing a portfolio of programs. Your update competes for attention with dozens of others. Ruthless brevity.
- "External visibility" is the section that matters most to political leaders. If Congress has asked about this program, if GAO is auditing it, if there is press interest — say so upfront.
- Frame mission impact in terms the agency uses in its Congressional budget justification and strategic plan. Speak their language.
- Never surprise leadership. If a risk could escalate to their level, tell them before it does.

### ISSO / Security Stakeholder Update

Security stakeholders need to know whether your work affects the system's authorization posture. They are not interested in feature details — they need to assess risk.

**Format**:
```
Sprint: [X]

ATO-relevant changes this sprint:
- [Change]: [New component / data type / integration / authentication flow].
- Significant Change Request needed: [Yes / No / Under review].

Security posture:
- Open vulnerabilities: [Count by severity: Critical/High/Medium/Low].
- New vulnerabilities found: [Count]. [Remediation timeline].
- POA&M items: [X open, Y closed this period, Z overdue].

Continuous monitoring:
- [Scanning tool] last run: [Date]. [Results summary].
- [Control evidence updated]: [List of controls with updated evidence].

Upcoming items with security implications:
- [Planned feature/integration]: [Potential impact on ATO boundary].
```

**Tips**:
- Do not wait for the ISSO to ask whether your sprint work affects the ATO. Proactively flag anything that introduces new data types, external connections, authentication changes, or infrastructure modifications.
- POA&M status is high-stakes. Overdue POA&Ms can trigger ATO revocation. Report them prominently.
- If you are unsure whether a change requires a Significant Change Request, ask. Shipping a change that should have triggered an SCR is worse than asking a question that turns out to be unnecessary.

### Congressional / Oversight Response

When a Congressional office inquires about a constituent's case or a program's status, the response is high-stakes and formulaic. Product managers are rarely the ones sending the response, but they are often the ones assembling the facts.

**Guidelines for assembling facts for Congressional responses**:
- Provide facts only. No opinions, no spin, no speculation.
- Include: current status, timeline of key events, what has been done, what will happen next, and when.
- Exclude: blame, internal process details, contractor names, technical jargon, anything the agency has not approved for external communication.
- Respond to what was asked. Do not volunteer additional information.
- Everything you write may be quoted in a letter from the agency to a Member of Congress. Write accordingly.
- Route through the agency's Congressional liaison or legislative affairs office. Never respond directly to a Congressional office.

## Status Reporting — Federal Adaptation

The standard Green/Yellow/Red framework applies. Federal-specific additions:

### QASP-Aligned Status

Status should map to QASP performance standards, not just subjective assessment:

- **Green**: All QASP metrics within acceptable range. Deliverables on schedule. Burn rate on pace.
- **Yellow**: One or more QASP metrics trending toward threshold. A deliverable is at risk. Burn rate deviating from plan by more than 10%. A risk has materialized that could affect contract performance.
- **Red**: QASP metric has breached acceptable threshold. A deliverable will miss its deadline. A compliance gate (ATO, 508, PRA) is blocking deployment. Burn rate indicates funding exhaustion before PoP end.

### Status Documentation Trail

In government, status reports become part of the contract record:
- The COR may reference your status reports in CPARS evaluations (the contractor performance rating that follows you to future competitions).
- An auditor may review status reports to assess whether risks were identified and communicated.
- A protest may examine whether the government was aware of performance issues.

This means: be accurate. Do not overstate Green to avoid a difficult conversation. Do not understate Red to avoid escalation. The record will be reviewed by people who were not in the room.

## Risk Communication — Federal Categories

The standard ROAM framework and communication structure apply. Federal programs face additional risk categories that require specific handling:

### Federal-Specific Risk Categories

**Funding risk**: Continuing resolution (CR), sequestration, rescission, or budget uncertainty delays or reduces available funding. Mitigation: identify minimum viable scope that can be delivered under reduced funding. Communicate to COR early so the CO can plan.

**ATO risk**: A security finding, Significant Change Request delay, or ATO expiration threatens the ability to deploy to production. Mitigation: maintain continuous ATO readiness; do not batch security work. Escalate to ISSO immediately when risk is identified.

**Procurement risk**: A needed contract modification, new task order, or procurement action is delayed. Work cannot start or continue until procurement is complete. Mitigation: identify procurement dependencies early and track them on the roadmap. The product team cannot accelerate procurement — only the CO can.

**Clearance risk**: A key team member's clearance is delayed, denied, or revoked. They cannot access the systems or facilities needed to do their work. Mitigation: identify clearance requirements during staffing. Have contingency staffing plans for critical roles.

**Cross-contract risk**: Another contractor's delay or failure affects your delivery. Mitigation: define interface contracts early, build fallback plans, escalate through the government program office (not contractor-to-contractor).

**Political / oversight risk**: A Congressional inquiry, GAO audit, OIG investigation, or press report creates urgency or scrutiny on the program. Mitigation: ensure leadership has current, accurate status information. Do not allow leadership to be surprised.

**Compliance risk**: A PRA submission is delayed, a PIA is not completed, or a 508 remediation deadline is approaching. Mitigation: track compliance dependencies on the roadmap with the same rigor as technical dependencies.

### Escalation Paths

Federal programs have formal escalation paths. Use them:

1. **Team-level resolution**: PM resolves with engineering lead, design lead, or within the sprint team.
2. **COR escalation**: Risk affects contract performance, QASP metrics, or deliverable schedule. Inform the COR with a written risk statement.
3. **CO escalation**: Risk requires contract action (modification, additional funding, scope change). The COR escalates to the CO — the contractor does not go directly to the CO except through established channels.
4. **Program office escalation**: Risk affects mission delivery or program milestones. Inform the government program manager with impact assessment and options.
5. **Leadership escalation**: Risk has external visibility (Congressional, audit, press) or requires a go/no-go decision. Brief leadership with a one-page risk summary.

Document every escalation. In government, undocumented escalations did not happen.

## Decision Documentation — Federal Adaptation

The standard ADR format applies. Federal additions:

### Government Decision Authority

Not all decisions are the product team's to make. Before documenting a decision, identify who has the authority to make it:

- **Product / technical decisions**: PM and engineering lead. Document in an ADR. Inform the COR.
- **Scope decisions**: Require COR concurrence. If scope changes affect the PWS, the CO must approve a modification.
- **Security decisions**: ISSO recommends, AO decides. The product team provides information but does not make the call.
- **Compliance decisions** (508 exceptions, PRA determinations): Agency compliance officers decide. The product team provides analysis.
- **Launch / deployment decisions**: May require sign-off from multiple stakeholders (COR, ISSO, AO, 508 coordinator, program manager) depending on what is being deployed.

### Federal ADR Additions

Add these fields to the standard ADR format for government decisions:

```
## Decision Authority
Who has the authority to make this decision?
Who was consulted? Who was informed?

## Contract Implications
Does this decision require a contract modification, a scope change, or additional funding?
Does it affect a QASP metric or deliverable?

## Compliance Implications
Does this decision affect the ATO boundary, 508 conformance, PRA status, or privacy posture?
```

### When to Write an ADR — Federal Triggers

In addition to standard triggers (strategic choices, technical architecture, controversial decisions):
- Any decision that changes what is delivered under the contract vs. what the PWS specifies
- Any decision to defer compliance work (document the rationale and the plan to address it)
- Any decision influenced by a Congressional inquiry, audit finding, or political directive
- Vendor selection or technology choices that affect FedRAMP posture or ATO boundary
- Decisions made under time pressure from a CR, fiscal year end, or ATO expiration — these are the ones most likely to be questioned later

## Meeting Facilitation — Federal Additions

Standard agile ceremony facilitation (standup, planning, retro, demo) applies. Federal programs add:

### COR Sprint Review

Distinct from a team demo. The COR sprint review is a contract performance event.

**Purpose**: Demonstrate that delivered work meets acceptance criteria and QASP standards. Provide the COR with evidence for their surveillance activities.

**Format**:
1. Sprint summary: stories committed vs. delivered, velocity trend
2. Demo of completed work against acceptance criteria
3. QASP metrics for the period
4. Risks, blockers, and burn rate
5. Plan for next sprint (with COR concurrence on priorities)

**Tips**:
- The COR may use this meeting as their primary surveillance input. Treat it accordingly.
- Bring data, not just a demo. CORs need quantitative evidence for performance reports.
- If the COR raises a concern, document it and respond in writing, even if resolved verbally.

### Integrated Project Team (IPT) Meeting

Common in larger federal programs with multiple contractors and government stakeholders.

**Purpose**: Coordinate across contracts, resolve cross-program dependencies, align on program-level status.

**Format**:
1. Program-level status (government program manager leads)
2. Each contractor team reports: status, risks, dependencies on other teams
3. Cross-team dependency resolution
4. Upcoming milestones and coordination needs

**Tips**:
- IPTs are government-led. The government program manager sets the agenda and runs the meeting. Your role is to report accurately and raise cross-contract risks.
- Do not use the IPT to resolve bilateral issues with another contractor. Take those offline.
- What you say in an IPT is heard by the government and by your competitors' teams. Be factual and professional.

### Program Review / Gate Review

Formal review with senior government leadership at major milestones.

**Purpose**: Obtain leadership approval to proceed to the next phase, deploy to production, or make a significant commitment.

**Format**:
1. Executive summary: what we are asking for (the decision)
2. Progress since last review: outcomes delivered, metrics moved
3. Risk assessment: current risks and mitigations
4. Compliance status: ATO, 508, privacy, PRA
5. Recommendation: proceed, proceed with conditions, or delay
6. Decision requested

**Tips**:
- Gate reviews are approval events. Be clear about what decision you are asking for.
- Bring the compliance status unprompted. If you do not mention ATO/508/privacy status, leadership will ask — and not having the answer damages credibility.
- If the recommendation is "delay," come with a revised plan. Leadership wants solutions alongside problems.
