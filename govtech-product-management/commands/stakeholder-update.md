---
description: Generate a stakeholder update tailored to federal audience and reporting cadence
argument-hint: "<update type and audience>"
---

# Stakeholder Update

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a stakeholder update tailored to the federal audience, reporting cadence, and communication protocol.

## Workflow

### 1. Determine Update Type

Ask the user what kind of update:
- **Sprint Review / COR Check-in**: Regular cadence update on delivery progress, QASP metrics, blockers, and next sprint objectives
- **Monthly Status Report**: Formal contractor status report — often a contract deliverable (CDRL). Progress against PWS/SOO, QASP compliance, risks, staffing, financial status
- **IPT (Integrated Program Team)**: Cross-functional coordination across government and contractor teams on shared objectives and dependencies
- **Quarterly IPR (Integrated Program Review)**: High-level program health, milestone progress, budget execution, risk posture, strategic alignment
- **Launch / Release**: Announcement of a capability deployment with scope, ATO/security status, rollout plan, and impact
- **Ad-hoc — Escalation**: Urgent issue requiring COR or CO attention (QASP breach, staffing gap, scope concern, security incident)
- **Ad-hoc — Congressional Inquiry**: Response to a Congressional question about the program or service
- **Ad-hoc — Audit Response**: Input for GAO, OIG, or other oversight body inquiry

Also ask:
- Is this a **formal contract deliverable** (CDRL) with specific format and submission requirements, or an **informal communication**?

### 2. Determine Audience

Ask who the update is for:
- **COR / COR team**: Primary government oversight. Detailed delivery and compliance status. Most frequent recipient. This is the default communication path.
- **Contracting Officer (CO/KO)**: Contractual authority. Receives formal deliverables, escalations, and items requiring contractual action (modifications, option exercise, cure notices).
- **Program Leadership / Program Office**: Mission owners. Outcome-focused, strategic framing. Interested in mission impact, not task-level detail.
- **ISSO / Authorizing Official (AO)**: Security and compliance posture. ATO status, security findings, POA&M progress, vulnerability remediation.
- **Congressional liaison**: Responding to inquiries from Congress about the program. Requires specific format, fact-checked precision, and coordination with agency comms.
- **OMB / oversight**: IT Dashboard updates, FITARA reporting, CX metrics, or responses to OMB data calls.
- **Delivery team**: Technical detail, implementation context, blockers, decisions needed. Internal to the contractor team.

**Communication protocol note**: In federal contracting, the COR is the primary point of contact between the contractor and the government. Updates to the CO, program leadership, or other government stakeholders should typically route through or be coordinated with the COR. Confirm the appropriate routing with the user.

### 3. Pull Context from Connected Tools

If **~~project tracker** is connected:
- Pull status of roadmap items and milestones
- Identify completed items since last update
- Surface items that are at risk or blocked
- Pull sprint or iteration progress
- Check items against PWS/SOO task areas and CLINs

If **~~chat** is connected:
- Search for relevant team discussions and decisions
- Find blockers or issues raised in channels
- Identify key decisions made asynchronously

If **~~meeting transcription** is connected:
- Pull recent meeting notes and discussion summaries
- Find decisions and action items from relevant meetings

If **~~knowledge base** is connected:
- Search for recent meeting notes
- Find decision documents or design reviews

If no tools are connected, ask the user to provide:
- What was accomplished since the last update
- Current blockers or risks (distinguish internal vs. cross-contract vs. government-dependent)
- Key decisions made or needed (and who has decision authority)
- QASP metric status for the period
- Staffing or key personnel changes
- What is coming next

### 4. Generate the Update

Structure the update for the target audience. See the **stakeholder-comms** skill for detailed templates, G/Y/R status definitions aligned to QASP thresholds, and federal risk categories.

**For COR / COR team**:
- QASP compliance status (Green/Yellow/Red per metric with thresholds)
- Delivery progress mapped to PWS/SOO task areas
- Completed items with acceptance criteria met
- Items in progress with expected completion
- Blockers requiring government action (with specific asks and deadlines)
- Risks with federal risk categories (funding, ATO, procurement, clearance, cross-contract, political, compliance) and mitigation plans
- Key personnel or staffing status
- Next sprint/period objectives
- Keep structured for scanning. CORs manage multiple contracts — make this easy to process.

**For Contracting Officer (CO/KO)**:
- Executive summary (3-5 sentences max)
- Contract performance status (on track / at risk / issue)
- Items requiring contractual action (modifications, option exercise, funding adjustments)
- QASP compliance summary (not full detail — flag breaches or near-breaches)
- Financial status (burn rate, funding runway, CLIN status)
- Formal and precise. This is a contractual relationship.

**For Program Leadership / Program Office**:
- TL;DR: mission impact in 2-3 sentences
- Status color (G/Y/R) with one-line rationale
- Key outcomes delivered (framed as mission progress, not tasks completed)
- Strategic risks with mitigation (focus on mission, funding, and political risks)
- Decisions needed with options, recommendation, and deadline
- Alignment to agency strategic plan and OMB guidance
- Under 300 words. Frame everything in terms of mission outcomes.

**For ISSO / Authorizing Official**:
- ATO status and expiration timeline
- POA&M progress (open items, remediation status, overdue items)
- New security findings from scanning or assessment
- Vulnerability remediation status
- Compliance changes (new controls, configuration changes, boundary modifications)
- Upcoming security milestones or assessment dates

**For Congressional liaison**:
- Fact-checked, precise, and neutral in tone
- Program purpose and current status
- Key metrics demonstrating value (transactions processed, burden reduced, cost savings)
- Timeline and milestone context
- No speculation, no internal jargon, no opinion
- Coordinate with agency communications office before delivery

**For OMB / oversight**:
- Metrics aligned to reporting framework (IT Dashboard, FITARA, CX)
- Program health indicators with supporting data
- Budget execution status
- Modernization progress against milestones
- Risk items flagged proactively

**For delivery team**:
- What shipped (with links and ticket references)
- What is in progress (with owners and target dates)
- Blockers — distinguish between team-resolvable, government-dependent, and cross-contract
- Decisions needed (with options and recommendation)
- What is coming next sprint/iteration
- Any compliance or security work affecting the backlog

**For launch / release announcements**:
- What deployed and to which environment
- ATO/security clearance status for the release
- Scope of the release mapped to PWS/SOO
- User impact and expected outcomes
- Known limitations or issues with workarounds
- Rollout plan (phased, full, pilot) and rollback plan
- Success metrics and monitoring approach
- Feedback channels and issue reporting process

### 5. Review and Deliver

After generating the update:
- Ask if the user wants to adjust tone, detail level, or emphasis
- Confirm whether the update needs COR review before wider distribution
- If this is a CDRL, confirm it meets the contract-specified format and delivery requirements
- Offer to format for the delivery channel (email, document, slide deck, chat post)
- If **~~chat** is connected, offer to draft the message for sending

## Output Format

Keep updates scannable. Use bold for key points, bullets for lists. Use G/Y/R status aligned to QASP thresholds for COR and CO audiences. Executive and program leadership updates should be under 300 words. COR updates should be comprehensive but structured for quick scanning.

## Tips

- The most common mistake in stakeholder updates is burying the lead. Start with the most important thing.
- Never surprise the COR. If there is bad news, the COR should hear it from you first and directly — not discover it in a report or from their leadership.
- Status colors (Green/Yellow/Red) should reflect reality, not optimism. Yellow is not a failure — it is good risk communication. In federal context, G/Y/R should map to QASP thresholds, not subjective assessment.
- Asks should be specific and actionable. "We need a decision" is not an ask. "We need the COR to approve the updated test plan by Friday to maintain the sprint timeline" is.
- For program leadership, frame everything in terms of mission outcomes, not activities and tasks. "Reduced average processing time from 12 days to 4 days" — not "completed 23 story points."
- If there is bad news, lead with it. Do not hide it after good news.
- Distinguish between what you are contractually obligated to report and what is informational. CDRL deliverables have format, content, and timing requirements — treat them accordingly.
- Match the length to the audience's attention and need. Program leadership gets a few bullets. The COR gets the details they need to perform surveillance. The CO gets contractual essentials only.
- Congressional responses require extraordinary precision. Every fact must be verifiable. Coordinate with agency communications.
- Be mindful of information classification. Do not include CUI, FOUO, or sensitive security details in channels not authorized for that information.
