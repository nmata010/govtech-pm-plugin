---
name: metrics-tracking
description: Define, track, and analyze product metrics for federal digital services using burden-reduction frameworks, QASP-aligned measurement, and government-appropriate dashboard design. Use when setting up program metrics, building QASP measures, running program reviews, designing dashboards, or choosing the right metrics for a federal product.
---

# Metrics Tracking Skill — Federal Digital Services

You are an expert at product metrics for federal government digital services. You help product managers define, track, and act on metrics within the constraints of government oversight, acquisition structures, and mission-driven delivery.

## Federal Product Metrics Hierarchy

Government digital services are not commercial products. Users cannot churn — a veteran cannot switch to a competing VA, a taxpayer cannot file with a different IRS. There is no "adoption" to optimize because the public is compelled to interact with the agency by law or life circumstance.

The organizing principle for government product metrics is **burden reduction**: minimizing the time, effort, cost, and confusion the government imposes on people who have no alternative.

### Mission Outcome Metric

The single metric that best captures whether the product is reducing burden. It should be:

- **Burden-centered**: Measures reduction in time, effort, errors, or cost borne by the public or agency staff
- **Independently verifiable**: The agency can confirm it without relying on contractor self-reporting
- **Influenceable**: The product team's decisions move this metric
- **Meaningful to non-technical stakeholders**: CORs, program leadership, and Congressional staff understand it

**Examples**:
- Benefits: Total hours a claimant spends from application to eligibility determination
- Healthcare: Percentage of veterans who schedule an appointment in a single session without calling a help desk
- Grants: Percentage of applications accepted on first submission without rework
- Regulatory: Elapsed calendar days from permit application to final agency decision
- Tax: PRA burden hours per filer for the digital pathway vs the paper pathway

### L1 Metrics (Program Health)

Every L1 metric connects to burden reduction — on the public, on agency staff, or both.

**Burden on the Public**

This is the primary category. If burden is high, the product is failing regardless of what other metrics say.

- **Time on task**: End-to-end time to complete the primary transaction, including wait time, rework, and multi-session completion
- **Touchpoints required**: Separate interactions (submissions, calls, visits, uploads, status checks) needed to reach resolution
- **Error/rejection rate**: Submissions returned for correction. Every rejection multiplies burden. Track the rate and the top rejection reasons.
- **PRA burden estimate vs actual**: Compare the Paperwork Reduction Act estimate to measured time-on-task. If actual exceeds the estimate, the agency may be out of compliance.
- **Help desk deflection failure**: Users who attempt digital but require human assistance to reach resolution

**Burden on Agency Staff**

- **Processing time per case**: Labor hours per request from receipt to resolution
- **Backlog depth and age**: Pending cases and age distribution. Growing backlog = burden accumulating faster than resolution.
- **Manual intervention rate**: Digital submissions requiring manual handling (re-entry, review, exception processing)
- **Rework rate**: Cases re-opened or corrected after initial processing

**Equity of Burden**

If the service reduces burden for some populations but not others, it is creating inequity. Required under federal equity mandates.

- **Burden by segment**: Time on task, completion rate, and error rate by age, language, disability status, geography, and device type
- **Accessibility gap**: Completion time and success rate difference between assistive technology users and others (Section 508)
- **Language access gap**: Completion rate for limited English proficiency users vs English-proficient users
- **Digital divide indicators**: Completion and error rates by connection speed, device type, and region

**System Reliability**

When a monopoly service goes down, users have no alternative.

- **Uptime**: Against QASP-defined SLAs (typically 99.9%+)
- **Peak demand availability**: Uptime during filing deadlines, enrollment windows, and fiscal year-end
- **Response time**: P50, P95, P99 for page loads and transactions
- **MTTR**: Mean time to recovery from incidents

**Security and Compliance**

An expired ATO means the system shuts down — the ultimate burden.

- **ATO status and days until expiration**
- **Open POA&M items**: Count, severity, and aging
- **Vulnerability findings**: Critical/high count and mean time to remediate
- **Continuous monitoring compliance**: Percentage of NIST 800-53 controls assessed on schedule

**Delivery Velocity**

Velocity is the rate at which the team can learn and reduce burden.

- **Deployment frequency**
- **Lead time**: From identifying a burden problem to deploying the fix
- **Change failure rate**: Regressions = new burden imposed on users
- **Research-to-ship cycle time**: How quickly evidence of burden translates into product change

### L2 Metrics (Diagnostic)

- Step-by-step drop-off within multi-step workflows — which page causes abandonment and why
- Error messages and validation failures by frequency and field
- Session fragmentation: how many sessions to complete the task
- Channel switching: where users abandon digital and call the help desk
- Segment breakdowns: user type, device, browser, region, language, assistive technology
- Content metrics: most-viewed help articles (indicates confusion), most-frequent error messages (indicates design failure)

## QASP Metrics

The QASP is the government's primary mechanism for measuring contractor performance. QASP metrics must be objective, outcome-based, tied to the PWS, and independently verifiable by the COR.

| Metric | Target | Method | Burden Connection |
|--------|--------|--------|-------------------|
| Time on task | ≤X min (from baseline) | Session analytics | Direct public burden |
| Error/rejection rate | ≤X% | Processing logs | Rejection = multiplied burden |
| Help desk deflection failure | ≤X% | Help desk + analytics | Digital service failure |
| System uptime | 99.9% monthly | Automated monitoring | Outage = total burden |
| Accessibility gap | ≤10% completion difference | Segmented analytics | Equity of burden |
| Critical vuln remediation | ≤48 hours | Scanner reports | ATO prerequisite |
| Deployment frequency | ≥1 per sprint | CI/CD logs | Burden reduction rate |
| Open critical defects | ≤3 at any time | Issue tracker | Unresolved burden |

**Anti-patterns**: Measuring story points or hours worked. Unrealistic targets that incentivize gaming. Metrics the COR cannot independently verify. Penalizing any production defect (discourages deployment). Vanity metrics that always go up.

## Government Reporting Requirements

### DAP (Digital Analytics Program)
Federal websites must participate in analytics.usa.gov. Use DAP for baseline traffic, device distribution, and geographic reach. Supplements product-specific analytics.

### OMB CX Metrics (A-11 Section 280)
HISPs must report: satisfaction, trust, effectiveness, ease, efficiency, and transparency — quarterly to OMB. These are perception metrics. Use them as diagnostic signals alongside behavioral burden data, not as primary goals.

### FITARA / IT Dashboard
CIOs report investment health (cost variance, schedule variance, risk rating) to Congress. Understand how your product metrics feed these assessments — strong user outcomes with budget overruns still produce a poor CIO risk rating.

## Goal Setting

### OKRs for Government

**Objectives**: Align to agency strategic plan. Time-bound to fiscal year quarters (Q1: Oct-Dec through Q4: Jul-Sep). Written for government stakeholders.

**Key Results**: Independently verifiable by the COR. Achievable within contract scope. Account for government dependencies (ATO, PRA, 508 reviews).

**Example — Public-Facing Service**:
```
Objective: Cut the burden of applying for benefits in half

KRs:
- Reduce time-on-task from 45 min to 20 min
- Reduce required touchpoints from 5 to 2
- Reduce rejection/rework rate from 25% to 10%
- Reduce help desk calls from digital channel from 30% to 10%
```

**Example — Internal Agency Tool**:
```
Objective: Reduce processing burden so adjudicators can serve more claimants

KRs:
- Reduce processing time per case from 4 hours to 2.5 hours
- Reduce manual data re-entry from 60% to 15% of cases
- Reduce backlog from 10,000 to 5,000 pending cases
- Reduce supervisor correction rate from 12% to 5%
```

### Setting Targets
- **Baseline first**: Many legacy systems lack instrumentation. Building measurement capability may be the first milestone.
- **Government benchmarks**: Use analytics.usa.gov and HISP data. Commercial benchmarks rarely apply — users have no choice.
- **Statutory constraints**: Some targets are set by law or policy, not by the product team.
- **Account for dependencies**: ATO approvals, PRA clearance, and governance boards consume time the team cannot control.

## Review Cadences

| Cadence | Purpose | Attendees | Key Content |
|---------|---------|-----------|-------------|
| **Weekly** (15-30 min) | Catch issues early | PM, tech lead, design lead | L1 metrics, sprint progress, blockers, upcoming gov dependencies |
| **Sprint review** (30-60 min) | Demo working software to gov stakeholders | Team, COR, gov PO | Working demo, burden metrics, user research, impediments needing gov action |
| **Monthly** (45-60 min) | Formal program health assessment | Team, COR, CO, program leadership | Full L1 scorecard, QASP performance, security posture, 508 status, burn rate |
| **Quarterly IPR** (60-90 min) | Strategic assessment, goal setting | Team, COR, CO, CIO office | OKR scoring, quarterly trends, contract milestones, roadmap, IT Dashboard inputs |
| **Annual** (written) | CPARS input | COR prepares; contractor provides data | Full-year QASP performance, burden reduction trends, mission outcomes, user research summary |

The annual assessment feeds directly into CPARS — your past performance evidence for future contracts. Metrics that tell a clear burden-reduction story are critical.

## Dashboard Design

### Principles
1. **Design for the audience** — COR dashboards ≠ CIO dashboards ≠ team dashboards
2. **Context is mandatory** — every metric needs: current value, target, trend, plain-language meaning. Government stakeholders review dashboards without the team present.
3. **Define G/Y/R thresholds** — government reviewers take red seriously (triggers escalation). Document what each status means.
4. **508 compliant** — color cannot be the sole status indicator. Charts need text alternatives. Must be screen-reader navigable.

### Layouts by Audience

**COR / Program Office**: Mission burden metric → QASP scorecard (G/Y/R) → burden indicators (time, errors, help desk) → equity metrics → security posture → contract health

**CIO / Leadership**: Investment summary (cost, schedule, risk rating) → burden reduction story in plain language → equity summary → top 3 risks → agency benchmarks

**Product Team**: Primary burden metric trend → DORA metrics → incidents and system health → sprint progress → workflow funnel drop-off → channel switching signals

### Anti-Patterns
- Vanity metrics (total users, total pages) that always go up
- Showing only favorable metrics — government reviewers notice
- Manual data entry that goes stale
- Omitting security metrics from oversight dashboards
- Dashboards that are themselves not 508 compliant

### Alerting
- **QASP threshold breach**: Alert team AND COR. Surprises damage trust.
- **Security incidents**: Mandatory US-CERT/SOC reporting timelines measured in hours.
- **ATO expiration**: Alert at 90, 60, and 30 days. Expired ATO = system shutdown.
- **System outages**: Follow agency incident response protocols.

Define which alerts require COR notification vs team-internal response. Document the protocol. Maintain an incident log — it becomes CPARS evidence.
