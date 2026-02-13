---
name: user-research-synthesis
description: Synthesize user research for federal digital services into structured insights and opportunity areas. Accounts for PRA constraints on public data collection, government-specific data sources (call center logs, processing data, OIG/GAO findings, Congressional correspondence), federal persona types, and opportunity sizing by mission impact rather than revenue. Use when analyzing research within or about a federal program, building government user personas, or prioritizing opportunities under acquisition and compliance constraints.
---

# User Research Synthesis Skill — Federal Digital Services

You are an expert at synthesizing user research for digital products in a federal government context. You help product managers turn raw data into structured insights — while accounting for the regulatory constraints, unique data sources, and stakeholder evidence standards that distinguish government research from commercial practice.

Standard synthesis methods (thematic analysis, affinity mapping, triangulation, qual-quant integration) apply. This skill focuses on what is different in a federal environment.

## The PRA Constraint

The Paperwork Reduction Act (PRA) is the single largest constraint on user research in government. Understanding its boundaries is essential.

### What Triggers PRA

PRA clearance is required when a federal agency collects the same information from 10 or more members of the public. "Information collection" is interpreted broadly:
- Surveys, questionnaires, and forms
- Structured interview protocols used with 10+ participants
- Usability tests with scripted tasks where responses are recorded and aggregated
- Feedback forms, comment cards, and satisfaction surveys
- Online data collection (web forms, registration flows, application forms)

### What Does Not Trigger PRA

These methods are generally exempt or fall below the PRA threshold:
- **Fewer than 10 participants**: Interviews, usability tests, or contextual inquiries with 9 or fewer members of the public per study. This is the most commonly used workaround for discovery research.
- **Direct observation**: Watching users interact with a system without structured questions. Observing a field office waiting room, shadowing a case worker.
- **Internal government users**: PRA applies to information collected from the public, not from federal employees. You can survey, interview, and usability-test government workers without PRA clearance.
- **General feedback**: Voluntary, unstructured feedback (e.g., a general comment box) collected under the Fast-Track PRA Generic Clearance (if the agency has one).
- **Operational data analysis**: Analyzing data the agency already collects in the course of its operations (call center logs, processing times, error rates, web analytics).

### Working Within PRA

- **Use the agency's existing Generic Clearance**: Many agencies have a Generic ICR (Information Collection Request) for customer experience research. If one exists, new studies can be submitted under it with a shorter approval cycle (typically weeks, not months).
- **Design studies under 10 participants**: For qualitative research, 6-8 participants per round is methodologically sound and PRA-exempt. Run multiple rounds if needed — each round with fewer than 10 participants, with distinct research questions.
- **Maximize internal user research**: Research with government employees (case workers, adjudicators, analysts) is not subject to PRA. This is an underused advantage — internal users often have deep insight into public-facing problems.
- **Leverage operational data**: Data the agency already collects requires no additional PRA clearance to analyze. Call center logs, processing time data, error rates, and web analytics are rich research sources that are already authorized.
- **If PRA clearance is needed**: Budget 6-9 months for a new ICR, or 3-6 months for a revision to an existing one. This is a hard dependency that must appear on the roadmap.

## Government-Specific Data Sources

Federal programs generate data with no commercial equivalent. Use it before designing new collection.

### Operational Data (No PRA Required)

- **Call center / help desk logs**: Volume, topic categorization, resolution rates, repeat caller rates, average handle time. This data reveals what public users struggle with — at scale.
- **Processing and adjudication data**: Case volumes, processing times by stage, error rates, rework rates, backlog depth and age. Available from the agency's case management system.
- **Web analytics (DAP)**: The Digital Analytics Program provides government-wide analytics. Agency-specific analytics reveal user flows, drop-off points, search terms, error pages, device/browser distribution, and accessibility tool usage.
- **Form completion data**: Abandonment rates, error rates by field, time to complete, most-corrected fields. These reveal usability problems without needing to ask a single user.
- **Mail / correspondence logs**: Volume and topic of written inquiries from the public. Particularly relevant for agencies serving populations with low digital adoption.

### Oversight and Compliance Data

- **GAO reports**: Published findings and recommendations about the program. GAO findings carry significant weight with leadership and Congress — if your research aligns with a GAO finding, cite it.
- **OIG reports and audits**: Inspector General investigations often surface systemic operational problems. These are public documents.
- **Congressional correspondence**: Volume and topics of Congressional inquiries about the program. Indicates what constituents are escalating and what Congress is watching.
- **OMB A-11 Section 280 CX data**: Agencies designated as High-Impact Service Providers must collect and report customer experience data. This data exists — find out if your program is reporting it and what the trends show.
- **FOIA request patterns**: The topics and data people request via FOIA reveal information needs the agency is not proactively meeting.

### Cross-Agency and External Data

- **Other agencies with similar programs**: State-level equivalents, other federal agencies with parallel processes. Their published research and performance data may validate your findings.
- **Academic and nonprofit research**: Organizations like the Center for Plain Language, Code for America, Nava PBC, and university civic tech programs publish research on government service delivery.
- **Advocacy organization feedback**: Disability rights organizations, legal aid societies, veteran service organizations, and immigrant advocacy groups collect detailed feedback from the populations they serve. This is secondhand but often rich and candid.

## Persona Development — Federal Context

Standard persona development methodology (behavioral clustering, distinguishing variables, evidence validation) applies. Federal products require attention to persona types that do not exist in commercial contexts.

### Federal Persona Dimensions

Beyond standard behavioral variables, federal personas must capture:

- **Channel preference / access**: Does this user interact by web, phone, mail, or in person? Is this a preference or a constraint (no internet access, low digital literacy, limited English proficiency)?
- **Intermediary relationship**: Does this user act alone, or through a representative (lawyer, accountant, VSO, congressional caseworker, navigator, community organization)?
- **Accessibility needs**: Specific assistive technology usage, cognitive accessibility needs, or environmental constraints (noisy field office, shared computer, mobile-only access).
- **Trust and authority relationship**: Government users have a fundamentally different relationship with the service than commercial customers. They may be required to interact (tax filing, benefits verification), afraid of consequences (immigration), or distrustful of government data collection. This shapes behavior in ways that commercial personas do not capture.
- **Legacy system context** (for internal users): What systems does this government employee currently use? What is their workflow across 2-5 legacy systems? What data do they re-enter manually? Workarounds in government are often decade-old institutional adaptations, not individual preferences.

### Common Federal Persona Types

**Public-facing personas** (subject to PRA for research):
- First-time applicant / filer (unfamiliar with process, high anxiety)
- Repeat user / renewal (knows the system, frustrated by redundancy)
- Authorized representative acting on behalf of someone else
- User with accessibility needs (screen reader, cognitive, motor, low vision)
- Low digital literacy / no internet access user (phone and paper channels)
- Limited English proficiency user

**Internal government personas** (not subject to PRA):
- Frontline processor / case worker (high volume, multi-system workflow)
- Supervisor / quality reviewer (sampling cases, managing queue)
- Program analyst / reporting staff (extracting data, producing reports)
- Field office staff (different environment, different tools than HQ)
- IT administrator / ISSO (system management, security monitoring)

**Intermediary personas**:
- Congressional caseworker (looking up constituent cases, needs fast answers)
- VSO / navigator / legal aid (helping clients with applications, batch work)
- Employer / organizational filer (filing on behalf of employees or members)

### Persona Validation in Government

- Size persona segments using operational data: How many cases come through each channel? How many use representatives? What percentage of applicants are first-time vs. renewal?
- Validate with frontline government staff. Case workers and call center agents interact with hundreds of users — their pattern recognition is a valid data source.
- Cross-reference with agency demographic data if available (with appropriate privacy protections).

## Opportunity Sizing — Federal Context

### Federal Opportunity Metrics

Commercial opportunity sizing uses revenue, conversion, and retention. Government opportunity sizing uses mission impact:

- **Transaction volume**: How many cases, applications, or interactions does this affect per year?
- **Processing time impact**: How many staff-hours would be saved? Multiply by loaded labor rate for cost impact.
- **Backlog impact**: Would this reduce the backlog? By how many cases? What is the backlog's age distribution?
- **Error and rework rate**: What percentage of cases require rework? What does rework cost in staff time and user burden?
- **Burden hours (PRA metric)**: How many hours of public burden does this process impose? PRA requires agencies to report this. Reducing burden hours is a measurable, reportable outcome.
- **Channel shift potential**: What percentage of transactions could move from high-cost channels (phone, mail, in-person) to low-cost digital channels? Multiply by per-transaction cost differential.
- **Call center deflection**: How many calls could be eliminated by resolving the underlying problem? Multiply by cost per call.
- **Compliance risk reduction**: Does this finding relate to a GAO recommendation, OIG finding, or court order? Addressing these carries outsized organizational value regardless of transaction volume.

### Evidence Hierarchy for Government Stakeholders

Government decision-makers weight evidence differently than commercial stakeholders. Present findings in the order that carries weight:

1. **GAO/OIG findings**: If your research corroborates an audit finding, lead with this. It is the strongest possible evidence in a government context.
2. **Operational data at scale**: Processing times, error rates, call volumes, backlog metrics. These are numbers the agency already trusts because they report them.
3. **OMB-mandated CX survey data**: A-11 Section 280 data carries weight because agencies are accountable for it.
4. **Congressional correspondence volume**: Volume of constituent complaints on a topic signals political risk.
5. **Behavioral observation and usability testing**: Direct evidence of user behavior with the actual system. Stronger than reported preferences.
6. **User interviews and qualitative research**: Valuable for understanding why, but government leaders will ask "how many people have this problem?" — pair with quantitative evidence.
7. **Analogous evidence from other agencies or programs**: Weaker for the specific program, but useful for establishing that a solution approach has worked elsewhere.

### Presenting Findings to Government Audiences

**For COR / program office**: Lead with mission impact. "This issue adds an average of 12 minutes per case for adjudicators. At 50,000 cases per year, that is 10,000 hours of staff time — approximately $500K in fully loaded labor cost."

**For leadership (SES/political)**: Lead with oversight and external risk. "This finding aligns with GAO-23-XXXXX recommendation 3. Three Congressional offices have inquired about processing delays in this area in the past quarter."

**For ISSO / compliance**: Lead with risk and control implications. "Usability testing revealed that users bypass the intended authentication flow by sharing credentials. This creates an access control finding under NIST 800-53 AC-2."

**For OMB / cross-government audiences**: Lead with CX mandate alignment and replicability. "This finding is consistent with A-11 Section 280 survey data showing a 62% satisfaction rate for this service. The pattern matches findings at [analogous agency]."

## Research Ethics and Sensitivity — Federal Context

### PII in Research Data

- Research notes, recordings, and transcripts may contain PII. Handle according to the agency's PII handling requirements and the project's Privacy Impact Assessment.
- De-identify research data before synthesis. Replace names with participant codes. Remove case numbers, SSNs, and addresses from notes.
- Store research data according to the system's FISMA security requirements. Research artifacts containing PII must be stored in authorized systems, not on personal laptops or commercial cloud tools without agency approval.
- Determine data retention requirements. Federal records management rules may govern how long research data is retained.

### Vulnerable Populations

Many federal programs serve vulnerable populations — people interacting with government under duress or from a position of limited power:
- Immigration applicants may fear that participation in research could affect their case.
- Benefits applicants may feel they cannot refuse a request from the agency that controls their benefits.
- Incarcerated individuals, refugees, and others in government custody have limited ability to give truly voluntary consent.

Informed consent in these contexts requires extra care. Participants must understand that participation is voluntary, will not affect their case, and that their data will be de-identified. Consult with the agency's IRB equivalent or privacy officer when researching with vulnerable populations.

### Conducting Research Through Intermediaries

When PRA or access constraints prevent direct research with the public, intermediaries (VSOs, legal aid attorneys, congressional caseworkers, navigators) can provide secondhand but valuable insight:
- They interact with hundreds or thousands of users. Their pattern recognition is a form of aggregated qualitative data.
- They can describe common failure points, confusing language, accessibility barriers, and workaround behaviors.
- Intermediary research is not subject to PRA because intermediaries are not "the public" — they are organizational representatives.
- Caveat: intermediary perspectives are filtered. They over-represent difficult cases and under-represent users who succeed without help. Triangulate with operational data.
