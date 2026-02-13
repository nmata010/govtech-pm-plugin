---
description: Synthesize user research from interviews, surveys, and feedback into structured insights for federal digital services
argument-hint: "<research topic or question>"
---

# Synthesize Research — Federal Digital Services

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Synthesize user research from multiple sources into structured insights and recommendations within a federal government context.

## Workflow

### 1. Gather Research Inputs

Accept research from any combination of:
- **Pasted text**: Interview notes, transcripts, survey responses, feedback
- **Uploaded files**: Research documents, spreadsheets, recording summaries
- **~~knowledge base** (if connected): Search for research documents, interview notes, survey results
- **~~user feedback** (if connected): Pull recent support tickets, feature requests, bug reports
- **~~product analytics** (if connected): Pull usage data, funnel metrics, behavioral data
- **~~meeting transcription** (if connected): Pull interview recordings, meeting summaries, and discussion notes

**Federal-specific sources** (ask if available):
- **Contact center data**: Call volume, top reasons for contact, resolution rates, escalation patterns — the largest continuous source of user feedback in most agencies and PRA-exempt
- **Congressional correspondence/casework**: Constituent complaints routed through Congress signal high-severity pain points
- **OIG complaints and agency ombudsman reports**
- **OMB A-11 Section 280 CX survey data** (for High Impact Service Providers)
- **Section 508 audit results and accessibility feedback**
- **Language access feedback and LEP (Limited English Proficiency) service data**

Ask the user:
- What type of research? (interviews, surveys, usability tests, analytics, support tickets, contact center data, Congressional correspondence)
- How many sources / participants?
- **PRA status**: Was this research conducted under an approved PRA clearance? If information was collected from 10+ members of the public, the Paperwork Reduction Act applies. Establish this upfront — it determines what data you legally have and what follow-up research is feasible.
- Is there a specific question or hypothesis they are investigating?
- What decisions will this research inform?
- Is this related to a **HISP CX measurement requirement** under OMB A-11 Section 280?

### 2. Process the Research

For each source, extract:
- **Key observations**: What did users say, do, or experience?
- **Quotes**: Verbatim quotes that illustrate important points
- **Behaviors**: What users actually did (vs what they said they do)
- **Burden observations**: Where did users experience unnecessary burden — excessive steps, redundant information requests, confusing language, wait times, channel switching, repeat contacts?
- **Equity observations**: Did the experience differ based on accessibility needs, language, digital access/literacy, geography, or demographic factors?
- **Pain points**: Frustrations, workarounds, and unmet needs
- **Positive signals**: What works well, moments of reduced friction
- **Context**: Whether the participant is a member of the public or agency staff, relevant program/eligibility context, user segment, experience level

### 3. Identify Themes and Patterns

Apply thematic analysis — see the **user-research-synthesis** skill for detailed methodology including affinity mapping and triangulation techniques.

Group observations into themes, count frequency across participants, and assess impact severity. Note contradictions and surprises.

Create a priority matrix:
- **High frequency + High impact**: Top priority findings
- **Low frequency + High impact**: Important for specific segments — weight higher if the affected segment is an underserved population per OMB equity directives
- **High frequency + Low impact**: Quality-of-life improvements
- **Low frequency + Low impact**: Note but deprioritize

**Federal prioritization adjustments**:
- **Burden-related findings** (unnecessary steps, redundant data collection, confusing processes) are high-priority by default given OMB CX mandates
- **Equity findings** that reveal disproportionate burden on underserved populations should be weighted higher regardless of frequency
- **Compliance-related findings** (508 barriers, language access gaps) may carry legal obligations that override frequency-based prioritization

### 4. Generate the Synthesis

Produce a structured research synthesis:

#### Research Overview
- Methodology: what types of research, how many participants/sources
- PRA status: conducted under approved clearance, PRA-exempt method (usability testing, contact center analysis), or not applicable (agency staff only)
- Research question(s): what we set out to learn
- Timeframe: when the research was conducted
- HISP alignment: whether this supports an OMB A-11 Section 280 CX measurement requirement

#### Key Findings
For each major finding (aim for 5-8):
- **Finding statement**: One clear sentence describing the insight
- **Evidence**: Supporting quotes, data points, or observations (with source attribution)
- **Burden implication**: Does this finding indicate unnecessary burden on the public or agency staff? Quantify where possible (time, steps, repeat contacts).
- **Frequency**: How many participants/sources support this finding
- **Impact**: How significantly this affects mission delivery, user burden, or equity
- **Confidence level**: High (strong evidence), Medium (suggestive), Low (early signal)

Order findings by priority (frequency x impact, with equity and burden weighting).

#### User Segments
If the research reveals distinct user segments:
- Segment name and description
- Key characteristics and behaviors
- Unique needs and pain points
- **Accessibility needs**: Section 508 considerations for this segment
- **Language access**: Primary languages, LEP considerations (EO 13166)
- **Digital access/literacy**: Device types, connectivity, comfort with digital services
- **Geographic considerations**: Rural, tribal, territory-specific factors
- **Statutory eligibility context**: Relevant program eligibility categories if applicable
- Volume estimate from program enrollment or agency service data

#### Opportunity Areas
Based on the findings, identify opportunity areas:
- What user needs are unmet or underserved
- Where does current burden exceed what is necessary to accomplish the mission
- Where do equity gaps exist across populations
- What changes would improve mission outcomes
- Prioritized by burden reduction potential, equity impact, and mission alignment

#### Recommendations
Specific, actionable recommendations:
- What to build, change, or investigate further
- Tied back to specific findings
- Prioritized by impact and feasibility
- **Implementation constraints**: Is the recommendation within PWS scope or does it require a contract modification? Would it require PRA clearance (e.g., a new form or data collection)? Does it trigger ATO boundary changes? Does it affect 508 compliance obligations?

#### Open Questions
What the research did not answer:
- Gaps in understanding
- Areas needing further investigation
- Suggested follow-up research methods
- **PRA implications for follow-up**: Would the proposed research require PRA clearance? If so, note the timeline (fast-track PRA for usability testing: ~4-8 weeks; standard PRA: 6-9 months) and suggest PRA-exempt alternatives where possible (contact center analysis, analytics, internal staff research)

### 5. Review and Extend

After generating the synthesis:
- Ask if any findings need more detail or different framing
- Offer to map findings to **OMB A-11 Section 280 CX metrics** (trust, satisfaction, ease of service) if this is a HISP
- Offer to assess **equity implications** across underserved communities in detail
- Offer to generate specific artifacts: persona documents, journey maps, opportunity maps, research presentations
- Offer to create follow-up research plans for open questions, including **PRA timeline and effort estimates** if public-facing research is needed
- Offer to draft product implications — noting which recommendations require contract modifications, PRA clearance, or ATO changes before implementation

## Output Format

Use clear headers and structured formatting. Each finding should stand on its own — a reader should be able to read any single finding and understand it without reading the rest. Flag burden and equity implications visually so they are not buried in narrative.

## Tips

- Let the data speak. Do not force findings into a predetermined narrative.
- **Burden is the primary lens.** Government users cannot choose an alternative service. Always ask "where is unnecessary burden?" as a first-order question in every synthesis.
- Distinguish between what users say and what they do. Behavioral data is stronger than stated preferences.
- Quotes are powerful evidence. Include them generously, with attribution to participant type (not name).
- Be explicit about confidence levels. A finding from 2 interviews is a hypothesis, not a conclusion.
- **Equity analysis is mandatory, not optional.** Examine whether findings differ across underserved populations — accessibility, language, digital access, geography. This is an OMB requirement.
- **Contact center data is underrated.** It is continuous, high-volume, and PRA-exempt. Start there before planning primary research that requires clearance.
- **PRA constrains follow-up research.** If you need to collect information from 10+ members of the public, plan for PRA clearance timelines — months, not weeks. Fast-track PRA exists for usability testing but has its own constraints and volume limits.
- Contradictions in the data are interesting, not inconvenient. They often reveal distinct user segments or equity gaps.
- Recommendations should be specific enough to act on. "Reduce burden" is not actionable. "Eliminate the duplicate address entry on steps 3 and 7 of the application" is.
- Resist the temptation to synthesize too many themes. 5-8 strong findings are better than 20 weak ones.
