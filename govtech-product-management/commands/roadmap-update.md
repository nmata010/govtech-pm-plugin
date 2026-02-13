---
description: Update, create, or reprioritize a product roadmap within a federal contract
argument-hint: "<update description>"
---

# Roadmap Update — Federal Digital Services

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Update, create, or reprioritize a product roadmap within a federal contracting environment.

## Workflow

### 1. Understand Current State

If **~~project tracker** is connected:
- Pull current roadmap items with their statuses, assignees, and dates
- Identify items that are overdue, at risk, blocked, or pending government action
- Surface any items without clear owners or dates
- Check alignment against PWS/SOO requirements — flag items not traceable to contract scope
- Identify upcoming QASP deliverable dates and compliance milestones (ATO renewals, 508 audits, FedRAMP continuous monitoring)

If no project management tool is connected:
- Ask the user to describe their current roadmap or paste/upload it
- Accept any format: list, table, spreadsheet, screenshot, or prose description
- Ask for the contract period of performance (base year, option years) and current fiscal year quarter

### 2. Determine the Operation

Ask what the user wants to do:

**Add item**: New feature, initiative, or work item to the roadmap
- Gather: name, description, priority, estimated effort, target timeframe, owner, dependencies
- **Scope check**: Is this within the current PWS/SOO scope? If not, it requires a contract modification — flag this and note that CO approval is needed before committing the item.
- **Compliance check**: Does this item trigger compliance requirements? (ATO boundary change, new PII handling requiring PRA, Section 508 obligations for user-facing changes, FedRAMP impact)
- **QASP alignment**: Which QASP metric(s) does this item support?
- Suggest where it fits based on current priorities, capacity, and contract constraints

**Update status**: Change status of existing items
- Options: **Not Started**, **In Progress**, **At Risk**, **Blocked**, **Pending Government Action**, **Completed**, **Descoped**
- For **At Risk** or **Blocked**: ask for the blocker and mitigation plan
- For **Pending Government Action**: specify the action (ATO decision, PRA clearance, CO approval of mod, GFI/GFE delivery, security review) and expected timeline. Distinguish from team-owned blockers — this status signals that the contractor cannot self-resolve and is important for CPARS accountability.
- For **Descoped**: note whether descoping was government-directed or mutually agreed, and whether a contract mod is needed

**Reprioritize**: Change the order or priority of items
- Ask what changed (new government direction, policy mandate, security finding, user research, resource change, funding shift)
- Identify which items are **contract-mandatory** (PWS deliverables, compliance milestones, QASP requirements) — these cannot be deprioritized without a contract modification regardless of any prioritization framework
- For discretionary items, apply a prioritization framework if helpful — see the **roadmap-management** skill for RICE, MoSCoW, ICE, and value-vs-effort frameworks
- Note that reprioritization typically requires **COR/government PM concurrence** — show the proposed change and rationale in a format suitable for that conversation
- Show before/after comparison

**Move timeline**: Shift dates for items
- Ask why (scope change, dependency slip, government-action delay, resource constraint)
- **Contractual impact**: Does this shift affect a QASP deliverable date or a contract milestone? If so, flag the CPARS and contract compliance implications.
- Identify downstream impacts on dependent items
- Flag items that move past contract period of performance boundaries or fiscal year end
- Note whether COR notification is required

**Create new roadmap**: Build a roadmap from scratch
- Ask about timeframe: align to **contract periods** (base year, option year 1, etc.) and/or **fiscal year quarters** (Q1: Oct-Dec, Q2: Jan-Mar, Q3: Apr-Jun, Q4: Jul-Sep)
- Ask about format preference (Now/Next/Later, quarterly columns, OKR-aligned, PWS-aligned)
- Gather the list of initiatives to include
- Ensure **compliance milestones** are included as non-negotiable items (ATO renewals, 508 audits, FedRAMP continuous monitoring, PRA renewals)
- Map each item to its PWS/SOO reference

### 3. Generate Roadmap Summary

Produce a roadmap view with:

#### Status Overview
Quick summary: X items in progress, Y completed this period, Z at risk, W pending government action, and any compliance milestones due within the next 30/60/90 days.

#### Roadmap Items
For each item, show:
- Name and one-line description
- Status indicator (**On Track** / **At Risk** / **Blocked** / **Pending Govt Action** / **Completed** / **Not Started**)
- PWS/SOO reference (or "Requires Mod" if out of current scope)
- Target timeframe or date
- Owner
- Key dependencies (distinguish team-owned from government-action dependencies)

Group items by:
- Contract period and fiscal quarter, or Now / Next / Later — depending on format
- Or by PWS functional area / theme if the user prefers

#### Compliance Milestones
Separate section for non-negotiable dates:
- ATO renewal or continuous monitoring milestones
- Section 508 audit or remediation deadlines
- FedRAMP assessment or continuous monitoring dates
- PRA clearance renewals
- Any other regulatory or reporting deadlines

#### Risks and Dependencies
- Items that are blocked or at risk, with details and mitigation plans
- **Government-action dependencies**: ATO decisions, PRA clearances, CO approval of mods, GFI/GFE delivery, security reviews — with expected resolution dates and escalation path if delayed
- Cross-team dependencies and their status
- Items approaching contract period of performance end dates

#### Changes This Update
If this is an update to an existing roadmap, summarize what changed:
- Items added, descoped, or reprioritized (with rationale)
- Timeline shifts (with cause and contractual impact)
- Status changes
- New government-action dependencies identified

### 4. Follow Up

After generating the roadmap:
- Offer to format for a specific audience:
  - **COR/IPR**: Aligned to QASP deliverables and contract milestones for Integrated Program Review
  - **Agency CIO/oversight**: Aligned to FITARA or IT Dashboard reporting
  - **Product/engineering team**: Detailed with dependencies, technical scope, and sprint-level mapping
  - **Government leadership**: Executive summary focused on mission outcomes and milestone status
- If items require scope changes, offer to draft a **contract modification justification**
- Offer to map the roadmap to **QASP deliverables** for compliance reporting
- If project management tool is connected, offer to update ticket statuses
- Offer to draft **COR communication** about roadmap changes, risks, or reprioritization rationale

## Output Format

Use a clear, scannable format. Tables work well for roadmap items. Use text status labels: **Done**, **On Track**, **At Risk**, **Blocked**, **Pending Govt Action**, **Not Started**. Include PWS reference for each item.

## Tips

- A roadmap is a communication tool, not a project plan. Keep it at the right altitude — themes and outcomes, not tasks.
- **Roadmap scope is bounded by the PWS.** You cannot add features outside the contract scope without a modification. If the roadmap includes items that require a mod, flag them explicitly.
- **Compliance milestones are non-negotiable.** ATO renewals, 508 audits, and FedRAMP continuous monitoring are not features to be prioritized — they are fixed constraints the roadmap must accommodate.
- **Government-action dependencies are the highest-risk items** because the team cannot accelerate them. Surface these early, track them explicitly, and identify escalation paths.
- When reprioritizing, always ask what changed — and whether the COR/government PM concurs. Priority shifts in federal contracts typically require government agreement.
- **Timeline shifts on QASP deliverables may have CPARS implications.** Flag these explicitly rather than treating date changes as routine planning adjustments.
- Flag capacity issues early. If the roadmap has more work than the team can handle, say so.
- Dependencies are the biggest risk to roadmaps. Surface them explicitly — and separate what the team controls from what requires government action.
- If the user asks to add something, always ask what comes off or moves. Roadmaps are zero-sum against capacity.
