# OctoAcme Project Management Methodology

Welcome to the OctoAcme project management documentation! This README provides a comprehensive overview of how OctoAcme manages projects, from initial concept through delivery and continuous improvement.

## Table of Contents

- [Overview](#overview)
- [Core Principles](#core-principles)
- [Roles and Personas](#roles-and-personas)
- [Project Lifecycle](#project-lifecycle)
- [Key Workflows](#key-workflows)
- [Communication Strategies](#communication-strategies)
- [Quality Assurance Practices](#quality-assurance-practices)
- [Getting Started](#getting-started)

## Overview

OctoAcme's project management approach is designed for **structured, iterative delivery** of cross-functional projects that deliver product features, services, or integrations. Our methodology emphasizes customer value, clear ownership, and data-informed decisions while maintaining psychological safety for team members.

### What Makes OctoAcme Different

- **Customer-first focus**: We prioritize customer value and usability in every decision
- **Iterative delivery**: Small, testable increments enable fast feedback and adaptation
- **Clear ownership**: Every project has named leaders responsible for success
- **Evidence-based**: We measure impact and iterate based on data
- **Learning culture**: We encourage feedback, experimentation, and continuous improvement

## Core Principles

Our project management practices are built on five foundational principles:

1. **Customer-first**: Prioritize customer value and usability in all decisions
2. **Iterative delivery**: Deliver small, testable increments to enable rapid feedback
3. **Clear ownership**: Each project has a named Project Manager and Product Lead
4. **Data-informed decisions**: Measure impact and iterate based on evidence
5. **Psychological safety**: Encourage feedback, learning, and open communication

## Roles and Personas

OctoAcme projects involve several key roles, each with distinct responsibilities:

### Project Manager (PM)
**Primary responsibility**: Coordinate delivery activities, manage schedules, risks, and communications

- Creates and maintains project plans and timelines
- Manages risks, dependencies, and resource constraints
- Facilitates key meetings (kickoff, planning, retrospectives)
- Ensures consistent documentation and status reporting
- Coordinates cross-team and stakeholder communication

**Communication**: Weekly status updates, risk registers, decision logs, project board coordination

### Product Manager (PdM)
**Primary responsibility**: Define what should be built to deliver customer and business value

- Defines problem statements and success metrics
- Prioritizes the roadmap and backlog
- Collaborates with stakeholders and engineering on trade-offs
- Validates solutions through user research and metrics

**Communication**: Weekly PM alignment, roadmap updates, stakeholder briefings, acceptance criteria

### Developers
**Primary responsibility**: Design, build, test, and deliver software components

- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Help estimate and plan work
- Identify technical risks and propose mitigations

**Communication**: Daily standups, sprint planning, PR descriptions, code reviews, technical design docs

### QA/Testing
**Primary responsibility**: Validate quality and acceptance criteria

- Test features against acceptance criteria
- Perform integration and end-to-end testing
- Validate security and performance requirements
- Document and track defects

### Stakeholders
**Primary responsibility**: Provide inputs and approvals

- Review and approve project direction
- Provide business context and requirements
- Make prioritization decisions when needed
- Support cross-functional coordination

## Project Lifecycle

OctoAcme projects follow a structured five-phase lifecycle:

### 1. Initiation
**Goal**: Validate and authorize work, align stakeholders, create lightweight plan

**Key activities**:
- Confirm business need and measurable outcomes
- Identify stakeholders and champions
- Define success criteria and initial timeline
- Create Project One-pager (problem, goal, success metrics)
- Assess initial risks and resource needs

**Decision gate**: Move to planning when success metrics are clear, stakeholders agree on priority, and team availability is confirmed

### 2. Planning
**Goal**: Turn approved initiative into actionable plan and backlog

**Key activities**:
- Hold kickoff meeting with stakeholders and delivery team
- Create prioritized backlog with acceptance criteria
- Estimate scope (T-shirt sizing or story points)
- Define Definition of Done (DoD)
- Identify dependencies and integration points
- Create release plan and milestone map

**Deliverables**: Prioritized backlog, release timeline, Definition of Done, test plan

### 3. Execution
**Goal**: Build, test, review, and iterate on deliverables

**Key activities**:
- Follow team rhythm (daily standups, weekly delivery syncs, sprint reviews)
- Manage work through project board (Backlog → Ready → In Progress → In Review → QA → Done)
- Conduct code reviews and automated testing
- Track velocity and burndown
- Update risk register weekly
- Escalate blockers as needed

**Focus**: Maintain quality while delivering incremental value

### 4. Release & Deployment
**Goal**: Deploy features to production safely and with full observability

**Key activities**:
- Verify all acceptance criteria are met
- Ensure passing CI and security scans
- Draft release notes and rollback plan
- Deploy to staging and run smoke tests
- Deploy to production (automated pipeline preferred)
- Run post-deploy verifications
- Announce release to stakeholders

**Release types**: Patch (hotfixes), Minor (incremental features), Major (significant functionality)

### 5. Close & Retrospective
**Goal**: Capture learnings and convert them into actionable improvements

**Key activities**:
- Conduct retrospective (45-75 minutes)
- Identify what went well and what could improve
- Create 2-3 prioritized action items with owners
- Track improvements in backlog
- Celebrate successes and share learnings

**Focus**: Continuous improvement through measured, iterative changes

## Key Workflows

### Sprint/Iteration Planning
- Timebox planning to agreed sprint length (typically 1-2 weeks)
- Pull items that meet Definition of Done and have clear acceptance criteria
- Respect team capacity and avoid overcommitment
- Review dependencies and risks

### Pull Request Workflow
- Keep PRs small (≤ 400 lines when possible)
- Include issue link and acceptance criteria in PR description
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging
- Ensure all CI checks pass

### Risk Management
- Maintain Risk Register with: ID, Description, Impact, Likelihood, Owner, Mitigation, Status
- Identify risks during planning and ongoing execution
- Assess impact and likelihood
- Define mitigation plans and contingencies
- Monitor and review at weekly syncs

### Blocker Escalation Path
1. **Level 1**: Team-level triage in daily standup
2. **Level 2**: PM escalates to Product Lead and dependent teams
3. **Level 3**: Sponsor-level escalation for business-impacting issues

For security incidents, follow the security incident runbook and notify Security on-call immediately.

## Communication Strategies

### Regular Cadence
- **Daily standups** (15 min): Progress, blockers, dependencies
- **Weekly PM + PdM sync**: Alignment on priorities and risks
- **Twice-weekly team standups**: Delivery progress (or as agreed)
- **Sprint/iteration demos**: Showcase completed work
- **Monthly stakeholder updates**: Progress, metrics, and upcoming plans
- **Ad-hoc escalations**: As needed for urgent issues

### Weekly Status Template
```
Progress this week:
- [List key accomplishments]

Next steps:
- [Planned work for coming week]

Risks & blockers:
- [Current risks and impediments]

Ask / decisions needed:
- [Questions or decisions requiring input]
```

### Incident Communication
When incidents occur:
1. Provide triage summary
2. Communicate actions being taken
3. Share expected timeline for resolution
4. Schedule post-incident blameless retrospective

### Single Source of Truth
Maintain project status in one location (project README or release doc) to ensure stakeholders have accurate, current information.

## Quality Assurance Practices

OctoAcme maintains high quality standards through multiple complementary practices:

### Testing Strategy
- **Unit tests**: For new logic and business rules
- **Integration tests**: Where components interact
- **End-to-end smoke tests**: For critical flows before release
- **Security scanning**: Automated in CI pipeline
- **Manual QA**: For feature acceptance when automated testing is insufficient

### Definition of Done (DoD)
Every team defines their DoD, typically including:
- Code complete and reviewed
- Tests written and passing
- Documentation updated
- Acceptance criteria met
- Security scans passed
- Ready for deployment

### Quality Metrics
- Test coverage percentage
- CI pass rate
- Production error rates
- Performance metrics (latency, throughput)
- Customer satisfaction scores

### Code Review Standards
- At least one approval required before merge
- Reviews focus on: correctness, maintainability, security, performance
- Small PRs enable faster, more thorough reviews
- Constructive feedback and collaborative improvement

## Getting Started

### For New Team Members

1. **Read this README** to understand the overall methodology
2. **Review the Project One-pager** for your current project
3. **Attend the project kickoff** or schedule a catch-up with the PM
4. **Check the project board** to see current work and priorities
5. **Join the team standup** to understand daily rhythm
6. **Review detailed process docs**:
   - [Project Initiation Guide](octoacme-project-initiation.md)
   - [Project Planning](octoacme-project-planning.md)
   - [Execution & Tracking](octoacme-execution-and-tracking.md)
   - [Release & Deployment](octoacme-release-and-deployment.md)
   - [Risk Management & Communication](octoacme-risks-and-communication.md)
   - [Retrospectives](octoacme-retrospective-and-continuous-improvement.md)
   - [Roles & Personas](octoacme-roles-and-personas.md)

### For Project Managers

- Start with the [Project Initiation Guide](octoacme-project-initiation.md)
- Use templates from individual process documents
- Maintain the Risk Register and project board
- Facilitate regular communication and retrospectives

### For Product Managers

- Define clear success metrics in the Project One-pager
- Prioritize backlog based on customer value and business impact
- Participate in weekly PM syncs and stakeholder updates
- Validate solutions with user research and data

### For Developers

- Review acceptance criteria before starting work
- Keep PRs small and well-documented
- Participate in code reviews and knowledge sharing
- Flag technical risks and dependencies early

## Key Artifacts Reference

All OctoAcme projects should maintain these core artifacts:

- **Project Charter / One-pager**: Problem, goal, success metrics, stakeholders, timeline
- **Roadmap and Release Plan**: High-level timeline with milestones
- **Sprint/Iteration Backlog**: Prioritized work items with estimates and acceptance criteria
- **Acceptance Criteria & Definition of Done**: Clear quality standards
- **Risk Register**: Identified risks with mitigation plans
- **Retrospective Notes**: Learnings and action items for improvement

## Using These Docs with Copilot Spaces

To leverage these process documents with GitHub Copilot:

- Keep the Project Charter updated in your project repository
- Add process-specific documentation to `.copilot/` for context-aware assistance
- Reference specific process docs in your Copilot Space configuration
- Use persona definitions to shape role-specific guidance

---

**Questions or feedback?** Contact your Project Manager or Product Manager, or contribute improvements to these docs through a pull request.
