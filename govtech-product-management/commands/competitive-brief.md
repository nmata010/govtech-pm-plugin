---
description: Create a competitive analysis brief for a federal procurement opportunity, competitor, or capability area
argument-hint: "<competitor, solicitation, or capability area>"
---

# Competitive Brief — Federal Digital Services

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Create a competitive analysis brief for a federal procurement opportunity, one or more competitors, or a capability area.

## Workflow

### 1. Scope the Analysis

Ask the user:
- **Subject**: Which competitor(s), solicitation, or capability area to analyze?
- **Solicitation status**: Is there a live RFP/RFQ, a Sources Sought/RFI, or is this pre-acquisition planning?
- **Contract vehicle**: Which vehicle is the competition on (GWAC, agency IDIQ, BPA, GSA MAS, full-and-open)?
- **Set-aside status**: Full-and-open, small business set-aside (8(a), SDVOSB, HUBZone, WOSB), or unrestricted?
- **Evaluation methodology**: LPTA or Best Value? If Best Value, are evaluation factor weightings known?
- **Recompete or new**: Is this a recompete with a known incumbent, or a new requirement?
- **Decision context**: What will this brief inform? (bid/no-bid, capture strategy, teaming decisions, proposal strategy, price-to-win)

### 2. Research

**Via web search — federal intelligence sources**:
- **FPDS.gov**: Incumbent contracts, award history, contract values, period of performance
- **USAspending.gov**: Spending trends by agency, program, and recipient
- **SAM.gov**: Active solicitations, Sources Sought, entity registrations, wage determinations
- **GAO bid protest decisions**: Evaluation analysis, pricing approaches, and competitive weaknesses from published protest decisions
- **Agency budget justifications**: IT modernization plans, investment priorities, and systems flagged for replacement
- **Competitor corporate sites**: Capability statements, published case studies with agency names, leadership bios
- **GovWin/BGOV** (if available): Pipeline data, competitive win rates, teaming intelligence
- **Job postings**: Competitors hiring cleared roles at specific agency locations signals active pursuit or performance

If **~~knowledge base** is connected:
- Search for existing competitive analysis documents or capture plans
- Find past debrief notes or lessons learned from prior pursuits
- Pull prior competitive research or bid/no-bid decisions

If **~~chat** is connected:
- Search for competitive mentions in capture or BD channels
- Find recent debrief feedback or teaming partner discussions

### 3. Generate the Brief

#### Competitor Overview
For each competitor:
- **Company profile**: Size standard (large/small), socioeconomic status, revenue/headcount if known
- **Federal footprint**: Key agency relationships, relevant contract vehicles held, geographic presence
- **Past performance**: Known CPARS-rated contracts in this mission area, scale and scope of relevant work
- **Cleared workforce**: Estimated capacity for cleared staff if relevant to the opportunity
- **Recent activity**: Contract awards, protests filed/sustained, teaming announcements, FedRAMP authorizations, key hires

#### Capability Comparison
Compare capabilities against anticipated or published evaluation factors. See the **competitive-analysis** skill for the federal rating scale (Discriminator / Meets / Risk / Non-compliant) and comparison matrix templates.

Structure the comparison around:
- Technical approach (mission-relevant capabilities, technology stack, DevSecOps maturity)
- Management approach (Agile delivery, key personnel, transition/phase-in)
- Compliance posture (FedRAMP, Section 508, ATO experience, security clearances)
- Past performance (relevant agency, scope, scale, recency)
- Price competitiveness (rate structure, pricing model fit)

#### Positioning Analysis
Analyze how each competitor positions in the federal market — mission alignment, compliance narrative, delivery philosophy, and category claim. See the **competitive-analysis** skill for federal positioning frameworks.

#### Strengths and Weaknesses
For each competitor:
- **Strengths**: Where they have structural advantage — incumbent knowledge, past performance depth, vehicle access, cleared workforce, compliance certifications, teaming relationships.
- **Weaknesses**: Where they are exposed — compliance gaps, past performance gaps at required scale, thin bench for key personnel, protest history, CPARS weaknesses, reliance on subcontractors for core capabilities.
- Assess based on verifiable evidence (FPDS data, protest decisions, published case studies) — not assumptions.

#### Opportunities
Based on the analysis:
- Where does the incumbent have compliance or performance gaps we can exploit?
- Are there set-aside eligibility or vehicle access barriers that narrow the competitive field in our favor?
- What agency pain points (from OIG reports, GAO audits, or budget justifications) align with our strengths?
- Are there teaming combinations that would create a stronger competitive position?
- Is the acquisition timeline favorable for building readiness (FedRAMP, past performance, clearances)?

#### Threats
- What is the incumbent's structural advantage and how durable is it?
- Which competitors have vehicle access or past performance we cannot match?
- Is there protest risk if we win? If we lose, do we have protest grounds?
- Could the agency extend option years, insource, or restructure the requirement to avoid a full recompete?
- Are set-aside restrictions or socioeconomic requirements barriers to our eligibility?

#### Strategic Implications
Tie the analysis to capture and proposal decisions:
- **Bid/no-bid signal**: Based on competitive position, is this worth pursuing?
- **Win strategy**: What is the discriminating theme — where can we demonstrably outperform the field?
- **Teaming needs**: What capability or past performance gaps require a teaming partner to close?
- **Compliance actions**: What certifications, authorizations, or clearances must be in place before proposal submission?
- **Past performance positioning**: Which contracts should we cite and how do they map to evaluation criteria?
- **Price-to-win considerations**: Based on competitive landscape, what price position is required to win?
- **Monitoring triggers**: What developments (solicitation release, protest decisions, competitor teaming announcements) should prompt an update to this analysis?

### 4. Follow Up

After generating the brief:
- Ask if the user wants to dive deeper on any section
- Offer to draft a **bid/no-bid recommendation memo** with supporting rationale
- Offer to develop a **capture strategy** with specific actions and milestones
- Offer to identify **potential teaming partners** and assess fit
- Offer to create a **past performance gap analysis** with remediation options
- Offer to draft a **compliance readiness checklist** for the opportunity
- Offer to scope a **price-to-win analysis**

## Output Format

Use tables for capability comparisons. Use the federal rating scale (Discriminator / Meets / Risk / Non-compliant) from the competitive-analysis skill. Use clear headers for each section. Keep the strategic implications section concise and actionable — this is where the brief drives decisions.

## Tips

- **Incumbent advantage is the default.** Assume the incumbent wins unless you can identify specific, material reasons they will not. Build your analysis around how to overcome that default.
- **Protest decisions are underrated intelligence.** GAO and COFC decisions publish detailed evaluation analysis. Search for protests involving your competitors by name.
- **Compliance is binary, not a spectrum.** A missing FedRAMP authorization or Section 508 certification is not a weakness — it is a potential disqualifier. Treat compliance gaps as hard gates.
- **Vehicle access determines eligibility.** If you are not on the contract vehicle, the analysis stops there. Identify vehicle access as the first filter.
- **Federal pricing is discoverable.** GSA MAS pricing is public. FPDS shows award values. Protest decisions sometimes reveal evaluated prices. Use this data.
- **Timing matters.** Competitive position changes across the acquisition lifecycle. An analysis done at Sources Sought has different implications than one done after RFP release.
- **Be honest about your own gaps.** A competitive brief that always shows your team winning is not a brief — it is a sales pitch. The value is in identifying where you are weak and what to do about it.
- **Competitive analysis has a shelf life.** Note the date and flag sections tied to specific solicitation milestones that will change.
