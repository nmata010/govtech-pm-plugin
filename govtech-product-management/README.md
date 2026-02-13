# GovTech Product Management Plugin

A product management plugin for federal government technology teams, primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Covers the full PM workflow within the federal acquisition lifecycle: writing specs mapped to contract scope, managing roadmaps around periods of performance, communicating with government stakeholders, synthesizing user research under PRA constraints, analyzing competitors using federal procurement data, and tracking metrics against QASP targets.

## Installation

See marketplace and plugin installation for Cowork and Claude Code in the root level [README](../README.md)

## What It Does

This plugin gives you an AI-powered product management partner built for federal digital services. It understands the procurement, compliance, and stakeholder structures that shape government technology delivery.

- **Feature Specs & PRDs** — Generate requirements documents mapped to PWS/SOO scope and CLINs. Includes user stories, Section 508 and ATO compliance considerations, success metrics tied to mission outcomes, and open questions tagged by decision authority (COR, CO, ISSO, program office).
- **Roadmap Planning** — Create and reprioritize roadmaps organized by contract period (base year, option years) and fiscal year quarters. Handles mandate-driven items, funding status tracking, cross-contract dependencies, and ATO/PRA lead times.
- **Stakeholder Updates** — Generate status updates tailored to government audiences (COR, program office, executive leadership, IPT). Maps status colors to QASP thresholds and follows formal reporting cadences.
- **User Research Synthesis** — Turn interview notes, contact center logs, operational data, and support tickets into structured insights. Accounts for PRA constraints, frames findings around burden reduction and equity, and sizes opportunities by transaction volume.
- **Competitive Analysis** — Research competitors using federal procurement data (FPDS, USAspending, SAM, GAO protest decisions). Generates briefs with incumbent advantage assessment, past performance analysis, and protest risk evaluation.
- **Metrics Review** — Analyze product metrics across QASP-obligated, agency-reported, and team-informational tiers. Tracks ATO status, burden reduction, equity of access, and CPARS-relevant performance.

## Commands

| Command | What It Does |
|---|---|
| `/write-spec` | Write a feature spec or PRD mapped to contract scope |
| `/roadmap-update` | Update, create, or reprioritize your roadmap by period of performance |
| `/stakeholder-update` | Generate a stakeholder update for government audiences |
| `/synthesize-research` | Synthesize user research with PRA-awareness |
| `/competitive-brief` | Create a competitive analysis brief using federal procurement data |
| `/metrics-review` | Review and analyze product metrics against QASP targets |

## Skills

| Skill | What It Covers |
|---|---|
| `feature-spec` | PRD structure with PWS/SOO mapping, CLIN references, compliance impact (ATO, 508, PRA), acceptance criteria |
| `roadmap-management` | Prioritization frameworks, period of performance alignment, mandate tracking, funding status, cross-contract dependencies |
| `stakeholder-comms` | Updates by government audience (COR, CO, PMO, IPT), QASP-aligned status, escalation paths, reporting cadences |
| `user-research-synthesis` | Burden-centered analysis, PRA constraints, equity assessment, operational data synthesis, opportunity sizing by transaction volume |
| `competitive-analysis` | FPDS/USAspending analysis, incumbent advantage assessment, past performance evaluation, protest risk, win/loss analysis |
| `metrics-tracking` | QASP metrics, CPARS-relevant performance, ATO/compliance tracking, burden reduction measurement, equity metrics |

## Example Workflows

### Writing a Spec

```
You: /write-spec
Claude: What feature or problem are you speccing out?
You: We need to add a self-service status tracker for benefit applications
Claude: [Asks about PWS/SOO scope, target users, compliance requirements, success metrics]
Claude: [Generates spec with problem statement, user stories, requirements mapped to CLINs, 508/ATO impact, burden reduction metrics, open questions by decision authority]
```

### Preparing a Stakeholder Update

```
You: /stakeholder-update
Claude: What type of update? (weekly COR, monthly status, quarterly IPR, ad-hoc)
You: Monthly status for the program office
Claude: [Pulls context from project tracker, chat, and knowledge base]
Claude: [Generates status with QASP performance, milestone progress, risks with escalation paths, compliance status, and next period priorities]
```

### Synthesizing User Research

```
You: /synthesize-research
Claude: What research do you want to synthesize? You can paste interview notes, upload files, or I can pull from connected sources.
You: [Pastes contact center logs and 6 interview transcripts]
Claude: [Identifies burden patterns, pain points, and equity gaps]
Claude: [Generates synthesis with findings, burden metrics, opportunity areas sized by transaction volume, and PRA considerations for follow-up research]
```

### Competitive Analysis

```
You: /competitive-brief
Claude: Which competitor(s) or opportunity are you analyzing?
You: Analyze the incumbent on the [agency] modernization recompete
Claude: [Pulls FPDS contract history, past performance signals, job postings, and protest history]
Claude: [Generates brief with incumbent advantage assessment, competitive positioning, teaming considerations, and protest risk factors]
```

## Data Sources

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your project management and communication tools for the best experience. Without them, provide context manually.

**Included MCP connections:**
- Chat (Slack) for team context and stakeholder threads
- Project tracker (Linear, Asana, monday.com, ClickUp, Atlassian) for roadmap integration, ticket context, and status tracking
- Knowledge base (Notion) for existing specs, research, and meeting notes
- Design (Figma) for design context and handoff
- Product analytics (Amplitude, Pendo) for usage data, metrics, and behavioral analysis
- User feedback (Intercom) for support tickets, feature requests, and user conversations
- Meeting transcription (Fireflies) for meeting notes and discussion context

**Additional options:**
- See [CONNECTORS.md](CONNECTORS.md) for alternative tools in each category
