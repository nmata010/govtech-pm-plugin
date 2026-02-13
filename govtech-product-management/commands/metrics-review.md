---
description: Review and analyze federal digital service metrics with QASP alignment, trend analysis, and actionable insights
argument-hint: "<time period or metric focus>"
---

# Metrics Review

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Review and analyze federal digital service metrics, assess QASP compliance, identify trends, and surface actionable insights for program stakeholders.

## Workflow

### 1. Gather Metrics Data

If **~~product analytics** is connected:
- Pull key service metrics for the relevant time period
- Get comparison data (previous period, same period last fiscal year, QASP targets)
- Pull segment breakdowns if available (channel, user type, region)

Supplement with federal data sources as available:
- **DAP** (Digital Analytics Program) for web traffic and behavior
- **Call center / contact center logs** for volume, handle time, resolution rates
- **Processing / transaction data** for backlog, cycle time, error rates
- **OMB A-11 Section 280 CX data** if applicable
- **QASP surveillance data** from COR monitoring
- **Operational system logs** for uptime, response time, error rates

If no analytics tool is connected, ask the user to provide:
- The metrics and their values (paste a table, screenshot, or describe)
- Comparison data (previous period, QASP thresholds, targets)
- Any context on recent changes (releases, incidents, policy changes, staffing)

Ask the user:
- What time period to review? (last sprint, last month, last quarter, fiscal year-to-date)
- What metrics to focus on? Or should we review the full service metrics suite?
- Are there QASP thresholds or contractual targets to compare against?
- What is the current Period of Performance phase? (base year, option year, approaching end)
- Any known events that might explain changes (releases, outages, policy changes, staffing shifts, continuing resolution impacts)?

### 2. Organize the Metrics

Structure the review using the metrics hierarchy from the **metrics-tracking** skill:

- **Mission Outcome** at the top: the primary measure of whether the service is achieving its intended public benefit (e.g., burden reduction, processing time, successful transaction completion)
- **L1 Service Health Indicators**: service delivery (uptime, response time), user experience (task completion, satisfaction, accessibility compliance), operational efficiency (processing time, backlog, cost per transaction), compliance posture (ATO status, 508 conformance, security findings)
- **L2 Diagnostic Metrics** for drill-down into specific areas

Clearly distinguish:
- **QASP-obligated metrics** — contractual; misses have remediation/cure notice implications
- **Agency-reported metrics** — required for OMB, FITARA, IT Dashboard, or Congressional reporting
- **Team-informational metrics** — used internally to guide product decisions

If the user has not defined their metrics hierarchy, help them identify their mission outcome metric and key L1 indicators before proceeding.

### 3. Analyze Trends

For each key metric:
- **Current value**: What is the metric today?
- **Trend**: Up, down, or flat compared to previous period? Over what timeframe?
- **vs QASP threshold**: Is it within contractual tolerance? How much margin exists?
- **vs Target**: How does it compare to the goal or agency benchmark?
- **Rate of change**: Is the trend accelerating or decelerating?
- **Anomalies**: Any sudden changes, spikes, or drops?

Identify correlations:
- Do changes in one metric correlate with changes in another?
- Are there leading indicators that predict lagging metric changes?
- Do segment breakdowns reveal that an aggregate trend is driven by a specific channel, user type, or region?
- Do fiscal year boundaries, continuing resolutions, or policy changes explain discontinuities?

### 4. Generate the Review

#### Summary
2-3 sentences: overall service health, QASP compliance status, most notable changes, key callout.

#### QASP Compliance Scorecard
Table format for contractual metrics:

| QASP Metric | Current | Threshold | Margin | Trend | Status |
|-------------|---------|-----------|--------|-------|--------|
| [Metric] | [Value] | [Threshold] | [+/- margin] | [Direction] | [Green / Yellow / Red] |

**Status definitions**: Green = meets threshold with healthy margin. Yellow = within 10% of threshold or trending toward breach. Red = threshold breached, remediation required.

#### Service Performance Scorecard
Table format for non-QASP metrics:

| Metric | Current | Previous | Change | Target | Status |
|--------|---------|----------|--------|--------|--------|
| [Metric] | [Value] | [Value] | [+/- %] | [Target] | [On track / At risk / Miss] |

#### Trend Analysis
For each metric worth discussing:
- What happened and how significant is the change
- Why it likely happened (attribution based on known events, correlated metrics, segment analysis)
- Whether this is a one-time event or a sustained trend
- Whether the trend has contractual, compliance, or reporting implications

#### Bright Spots
What is going well:
- Metrics exceeding QASP thresholds with healthy margin
- Burden-reduction gains (time saved, steps eliminated, channel shift to self-service)
- Positive trends to sustain or highlight in stakeholder reporting
- Segments, channels, or features showing strong performance

#### Areas of Concern
What needs attention:
- QASP metrics approaching or breaching thresholds
- Compliance metrics trending negatively (508 findings, security vulnerabilities, ATO conditions)
- Service delivery degradation (increased processing time, growing backlog, rising error rates)
- Early warning signals before they become contractual issues
- Metrics where we lack visibility or data quality is insufficient

#### Recommended Actions
Specific next steps based on the analysis:
- **QASP remediation**: Steps to address or prevent threshold breaches; COR notification if required
- **Investigations**: Dig deeper into a concerning trend (specify data source and method)
- **Service improvements**: Changes to address user pain points or mission gaps
- **Compliance actions**: Remediation for 508, security, or ATO-related findings
- **Escalations**: Items requiring COR, CO, ISSO, or program leadership attention
- **Reporting preparation**: Metrics to highlight in upcoming IPR, IT Dashboard update, or OMB submission

#### Context and Caveats
- Known data quality issues or gaps in instrumentation
- Events that affect comparability (outages, policy changes, fiscal year transitions, continuing resolutions)
- PRA constraints on collecting additional user data (note: collecting operational/transactional data does not require PRA clearance)
- Period of Performance context (approaching option year, end of contract)
- Metrics we should be tracking but are not yet

### 5. Follow Up

After generating the review:
- Ask if any metric needs deeper investigation
- Offer to format findings for a specific audience (COR status report, IPR briefing, OMB reporting, program leadership)
- Offer to draft a QASP remediation plan for any metrics at risk
- Offer to create a dashboard spec for ongoing monitoring (noting 508 compliance requirements)
- Offer to set up a metrics review template aligned to the contract reporting cadence

## Output Format

Use tables for scorecards. Separate QASP-obligated metrics from informational metrics. Use Green/Yellow/Red status for QASP metrics. Keep the summary tight — the reader should get the essential story in 30 seconds.

## Tips

- Start with QASP compliance status. If contractual metrics are at risk, that is the lead story regardless of other trends.
- Absolute numbers without context are useless. Always show comparisons (vs QASP threshold, vs previous period, vs target, vs benchmark).
- Be careful about attribution. Correlation is not causation. If a metric moved, acknowledge uncertainty about why.
- Segment analysis often reveals that an aggregate metric masks important differences. A flat overall number might hide one channel improving and another degrading.
- Not all metric movements matter. Small fluctuations are noise. Focus attention on meaningful changes — especially those approaching QASP thresholds.
- If a metric is missing its target, do not just report the miss — recommend what to do about it and who needs to be notified.
- Distinguish between metrics the team controls and metrics affected by external factors (policy changes, staffing, cross-contract dependencies). Attribution matters for remediation planning.
- Metrics reviews should drive decisions. If the review does not lead to at least one action, it was not useful.
- Fiscal year boundaries reset some comparisons. Be explicit about when year-over-year comparisons cross fiscal year lines.
