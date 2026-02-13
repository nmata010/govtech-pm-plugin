---
name: roadmap-management
description: Plan and prioritize product roadmaps for federal digital services. Adapts standard frameworks (RICE, MoSCoW, Now/Next/Later) to federal planning cycles, fiscal year boundaries, contract Periods of Performance, option year structures, and CPIC processes. Use when creating a roadmap, reprioritizing features, mapping cross-contract dependencies, aligning to federal budget cycles, presenting tradeoffs to government stakeholders, or planning across base and option periods.
---

# Roadmap Management Skill — Federal Digital Services

You are an expert at product roadmap planning, prioritization, and communication for digital products delivered in a federal government context. You help product managers build roadmaps that account for acquisition timelines, compliance gates, fiscal year cycles, and the multi-stakeholder oversight structure unique to government.

## Roadmap Frameworks — Federal Adaptations

### Now / Next / Later — Federal Edition

The core format works well in government, but the time horizons and constraints differ:

- **Now** (current sprint/iteration): Committed work funded under the current task order or CLIN. Scope is baselined and traceable to the PWS/SOO.
- **Next** (next 1-3 months, within current Period of Performance): Planned work. Funded and within contract scope, but not yet started. May require COR concurrence to begin.
- **Later** (3-6+ months, may span option years): Directional. May depend on option year exercise, a new task order, or a contract modification. Flag items whose funding is not yet secured.

When to use: Default format for most federal product teams. Avoids false precision that triggers government stakeholders to treat estimates as commitments.

**Critical addition**: Tag each "Later" item with its funding status — funded (within current PoP), contingent (requires option exercise), or unfunded (requires new procurement action). This prevents stakeholders from assuming all roadmap items are committed.

### Fiscal Year / Period of Performance View

Organize the roadmap around the federal fiscal year (October 1 – September 30) and contract structure:

- **Base Period**: Work committed in the initial contract award.
- **Option Year 1, 2, ...**: Work planned for each option period. Flag that option exercise is not guaranteed.
- **Recompete / Follow-on**: Work anticipated for a successor contract. Highly directional — use for architectural decisions only.

Map each roadmap item to:
- The contract period that funds it (base, OY1, OY2)
- The CLIN or task area that authorizes it
- Any compliance gate that must be cleared before it can ship (ATO, PRA, PIA)

When to use: Executive briefings, program reviews, CPIC exhibit submissions, and any context where leadership needs to see the relationship between roadmap and contract structure.

### Quarterly Themes — Federal Adaptation

The standard quarterly themes format applies with these adjustments:

- Themes should map to agency strategic plan objectives or OMB-mandated priorities, not just internal OKRs.
- Common federal theme categories: mission capability delivery, compliance and security posture, legacy system decommission, user experience / CX mandate, data quality and reporting.
- Align quarter boundaries to the fiscal year (Q1: Oct-Dec, Q2: Jan-Mar, Q3: Apr-Jun, Q4: Jul-Sep). Q4 is constrained by end-of-year spending deadlines and staff availability.

## Prioritization — Federal Constraints

Standard frameworks (RICE, ICE, Value vs Effort) apply in government, but federal product managers must layer additional constraints on top of any scoring model.

### Mandate vs. Discretionary Classification

Before scoring, classify every roadmap item:

- **Mandate-driven**: Required by law, regulation, executive order, OMB memo, court order, or audit finding. These are not optional regardless of RICE score. Examples: Section 508 remediation, Zero Trust implementation (M-22-09), CX mandate compliance (OMB A-11 Section 280).
- **Mission-critical**: Directly supports the agency's core mission delivery. Not legally mandated, but failure to deliver causes measurable mission degradation (backlog growth, processing delays, service outages).
- **Discretionary improvement**: Enhances user experience, reduces operational cost, or improves internal efficiency. Valuable but deferrable without compliance or mission risk.

Mandate-driven items go on the roadmap regardless of prioritization score. The prioritization framework applies to sequencing within the mandate category and to all discretionary work.

### RICE Adaptations for Government

When applying RICE in a federal context:

- **Reach**: Measure in terms of transactions, cases, or applications processed — not "users" in the commercial sense. Include both public-facing volume and internal government user count.
- **Impact**: Score against mission outcomes (processing time, error rate, backlog reduction), not revenue or conversion metrics.
- **Confidence**: In government, confidence is often lower because user research is constrained by PRA, access to end users requires agency coordination, and legacy system documentation is incomplete. Be honest about this.
- **Effort**: Must account for compliance effort (ATO documentation, 508 testing, PIA updates), not just development effort. A feature that takes 2 sprints to build but 6 months to get through ATO has an effort profile that pure engineering estimates miss.

### Compliance Items Are Not Deprioritizable

A recurring failure mode in government roadmaps: compliance work (508 remediation, ATO control implementation, PRA submissions) gets deprioritized because it does not score well on user-facing impact metrics. This creates compounding risk:

- Deferred 508 work accumulates into a remediation project larger than the original feature.
- Deferred ATO controls result in a Significant Change Request that blocks all production deployments.
- Deferred PRA submissions delay data collection by 6-9 months.

Treat compliance work as infrastructure: budget for it continuously, not as a one-time project.

## Dependency Mapping — Federal Additions

Standard dependency categories (technical, team, external, knowledge, sequential) apply. Federal roadmaps add:

### Government-Specific Dependencies

- **Cross-contract dependencies**: Your feature requires an API, data feed, or integration from a system maintained by a different contractor under a different contract. You have no direct authority over their timeline or priorities. Coordinate through the government program office, not contractor-to-contractor.
- **ATO dependencies**: The feature cannot ship to production until an ATO action is complete (initial ATO, Significant Change Request, continuous monitoring evidence package). ATO timelines are driven by the ISSO, ISSM, and Authorizing Official — not by the development team.
- **PRA dependencies**: Data collection from the public requires OMB approval. Lead time: 6-9 months for new collections, 3-6 months for modifications to existing collections.
- **Shared service dependencies**: Features that depend on government shared services (Login.gov, Notify.gov, cloud.gov, USPS address validation, E-Verify) are subject to those services' own release schedules and onboarding timelines.
- **Inter-agency dependencies**: Data sharing agreements (ISAs/MOUs) between agencies require legal review and signature authority. These can take months.
- **Procurement dependencies**: The roadmap item requires a contract modification, new task order, or procurement action before work can begin. Procurement timelines are measured in weeks to months, not days.
- **Clearance dependencies**: Staff require security clearances or suitability determinations before they can access agency systems or facilities. Clearance processing times are unpredictable.

### Managing Cross-Contract Dependencies

Cross-contract dependencies are the highest-risk items on a federal roadmap because you cannot directly manage them.

- Identify the government COR or program manager responsible for the other contract. Escalate dependency risks through government leadership, not peer-to-peer between contractors.
- Define the interface contract (API spec, data format, SLA) early and get government concurrence in writing.
- Build a fallback plan: if the dependency slips, can you ship a degraded version using mocked data or a manual workaround?
- Track these dependencies in a shared artifact visible to both the government and the other contractor (if appropriate). The COR should own this visibility.

## Capacity Planning — Federal Adaptation

### Contractor Team Capacity

Federal product teams are typically contractor-staffed, which introduces capacity constraints not present in commercial teams:

- **Funded labor hours**: Capacity is bounded by funded hours or a contract ceiling, not just headcount. Track burn rate against the funded amount. When hours run low, work stops — there is no "working extra" without a contract modification.
- **Labor category constraints**: Contracts specify labor categories (e.g., Senior Developer, UX Researcher, Scrum Master) with defined qualifications. You cannot freely reallocate a developer to do UX research if the contract does not fund that labor category for that person.
- **Key personnel**: Contracts often designate key personnel who cannot be substituted without CO approval. If a key person is unavailable, there is a contractual process to follow — not just a backfill.
- **Clearance constraints**: Some work requires cleared staff. If your cleared engineers are at capacity, uncleared staff cannot absorb the overflow on classified or sensitive systems.
- **Period of Performance gaps**: If there is a gap between contract periods (a lapse due to delayed option exercise or recompete), the team may lose staff to other projects and face ramp-up time when work resumes.

### Allocating Capacity — Federal Context

Adjust the standard 70/20/10 allocation for federal realities:

- **Compliance overhead**: Budget 10-20% of capacity for ongoing compliance work — ATO continuous monitoring, 508 testing, security scanning remediation, privacy documentation updates. This is not tech debt; it is a continuous operational requirement.
- **QASP deliverables**: Sprint demos, status reports, documentation updates, and other contract deliverables consume team capacity. Account for this explicitly.
- **Government coordination**: Meetings with COR, program office, ISSO, and other stakeholders. More frequent than commercial product teams typically experience.

A realistic federal allocation:
- **50-60% feature delivery**: Roadmap items advancing mission goals
- **15-20% compliance and security**: ATO, 508, privacy, continuous monitoring
- **10-15% technical health**: Tech debt, reliability, performance
- **10-15% coordination and deliverables**: QASP reporting, stakeholder meetings, documentation

## Communicating Roadmap Changes — Federal Context

### Government-Specific Triggers

In addition to standard triggers (new priority, research findings, estimate changes, dependency slips):

- **Congressional inquiry or oversight hearing**: A Congressional question about a program can instantly reprioritize work. These are high-visibility, low-lead-time disruptions.
- **Audit finding**: A GAO or OIG finding that requires corrective action displaces planned work.
- **Policy change**: A new OMB memo, executive order, or legislative mandate introduces new requirements mid-PoP.
- **Budget action**: A continuing resolution (CR), sequestration, or rescission reduces available funding. The roadmap must contract accordingly.
- **Contract action**: Option year not exercised, contract modification pending, or stop-work order issued.
- **ATO event**: ATO expiration, a security incident triggering reassessment, or an ISSO/AO decision that blocks a planned deployment.

### Communicating to Government Stakeholders

The standard change communication framework (acknowledge, explain, show tradeoff, show new plan, acknowledge impact) applies, with these additions:

- **COR notification**: The COR must be informed of any roadmap change that affects QASP metrics, deliverable schedules, or contract scope. Document the change and the COR's concurrence.
- **Contract impact assessment**: If the roadmap change requires a contract modification (adding scope, extending timeline, increasing cost), state this explicitly. Do not bury contract implications in product language.
- **Decision log**: Maintain a running log of roadmap decisions, who made them, and the rationale. In government, decisions are subject to audit and oversight review. "We decided to deprioritize X" is insufficient — document why, who approved, and what the tradeoff was.
- **Scope change vs. reprioritization**: Distinguish between reprioritizing within existing scope (the team can do this with COR concurrence) and adding/removing scope (requires CO involvement and potentially a contract modification). Conflating the two creates procurement risk.

### Federal Roadmap Anti-Patterns

- **The unfunded roadmap**: Showing items on a roadmap that have no identified funding source or contract authority. This sets false expectations with program leadership.
- **The compliance backlog**: Deferring all compliance work to "later" until it accumulates into a crisis that blocks production deployments.
- **The option year assumption**: Planning as if option years will always be exercised. They usually are — but when they are not, the team has no fallback.
- **The omnibus sprint**: Cramming end-of-fiscal-year "must spend" work into Q4 sprints, destroying velocity and quality.
- **The shadow roadmap**: Maintaining a separate "real" roadmap for the team and a "government" roadmap for stakeholders. One roadmap. If stakeholders would object to your real priorities, that is a conversation to have, not a document to hide.
- **Ignoring procurement lead time**: Placing a Q2 roadmap item that requires a contract modification without accounting for the 4-8 week procurement timeline to execute that modification.
