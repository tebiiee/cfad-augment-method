# CFAD 2.0: Context Files Templates

## 🎯 Purpose
Templates for context files that maintain project state and provide quick reference for agents throughout the development lifecycle.

---

## 📋 Template: mission.md

```markdown
# Project Mission & Context

**Last Updated**: [YYYY-MM-DD]
**Project Status**: [Phase X: Status]
**Current Sprint**: [Sprint X - Theme]

## 🎯 Project Vision
**Vision Statement**: [One clear sentence describing what this project will be]
**Mission Statement**: [One clear sentence describing why this project matters]
**Value Proposition**: [What unique value this product delivers]

## 👥 Target Users
**Primary Persona**: [Main user type] - [Key characteristics]
**Secondary Persona**: [Secondary user type] - [Key characteristics]
**Market Size**: [TAM/SAM/SOM summary]

## 🏗️ Technical Overview
**Tech Stack**: [Primary technologies]
**Architecture**: [High-level architecture approach]
**Deployment**: [Deployment strategy]
**Key Integrations**: [Third-party services]

## 📊 Current Status
**Phase**: [Current phase and progress]
**Sprint**: [Current sprint and focus]
**Stories Completed**: [X/Y stories complete]
**Next Milestone**: [Next major milestone]

## 🎯 MVP Scope
**Core Features**: [List of MVP features]
**Success Metrics**: [How success is measured]
**Timeline**: [Expected completion]

## 🚨 Key Constraints
**Technical**: [Technical limitations or requirements]
**Business**: [Business constraints or deadlines]
**Resource**: [Team or budget constraints]

## 📋 Quick Reference
**Repository**: [GitHub URL]
**Staging**: [Staging environment URL]
**Production**: [Production URL if deployed]
**Documentation**: [Key documentation links]

---
*This file provides quick context for agents. Keep it concise and current.*
```

---

## 📋 Template: roadmap.md

```markdown
# Project Roadmap & Progress

**Last Updated**: [YYYY-MM-DD]
**Current Phase**: [Phase X]
**Current Sprint**: [Sprint X]

## 🗺️ Overall Project Roadmap

### Phase 1: Research & Analysis ✅
**Status**: [Complete/In Progress/Pending]
**Duration**: [Start Date] - [End Date]
**Key Deliverables**:
- ✅ Market research and competitive analysis
- ✅ Product definition and feature prioritization
- ✅ Technical feasibility and architecture planning
- ✅ Project blueprint and MVP scope

### Phase 2: Architecture & Planning ✅
**Status**: [Complete/In Progress/Pending]
**Duration**: [Start Date] - [End Date]
**Key Deliverables**:
- ✅ Technical architecture design
- ✅ All hyper-detailed stories created
- ✅ Development environment setup
- ✅ CI/CD pipeline configuration

### Phase 3: Implementation 🔄
**Status**: [Complete/In Progress/Pending]
**Duration**: [Start Date] - [End Date]
**Current Focus**: [Current implementation focus]

## 📋 Sprint Progress

### Sprint 1: MVP Development
**Goal**: [Sprint goal]
**Status**: [X/Y stories complete]
**Timeline**: [Start Date] - [End Date]

#### Completed Stories ✅
- **Story 001**: User Authentication - ✅ Complete (login/register working)
- **Story 002**: Dashboard Layout - ✅ Complete (responsive design implemented)

#### In Progress Stories 🔄
- **Story 003**: Core Feature Implementation - 🔄 In Progress (60% complete)

#### Pending Stories ⏳
- **Story 004**: User Profile Management - ⏳ Pending
- **Story 005**: Data Visualization - ⏳ Pending

### Sprint 2: Post-MVP Features
**Goal**: [Sprint goal]
**Status**: [Planned/In Progress/Complete]
**Timeline**: [Start Date] - [End Date]

#### Planned Stories 📋
- **Story 006**: Advanced User Features - 📋 Planned
- **Story 007**: Analytics Dashboard - 📋 Planned
- **Story 008**: Notification System - 📋 Planned

## 📊 Progress Metrics

### Development Velocity
- **Stories per Sprint**: [Average stories completed]
- **Story Points per Sprint**: [If using points]
- **Cycle Time**: [Average time per story]

### Quality Metrics
- **Test Coverage**: [X% overall coverage]
- **Bug Rate**: [Bugs per story]
- **User Approval Rate**: [% of stories approved on first submission]

### Timeline Performance
- **On Schedule**: [% of milestones met on time]
- **Scope Changes**: [Number of scope adjustments]
- **Blockers Resolved**: [Average resolution time]

## 🎯 Upcoming Milestones

### Next 2 Weeks
- [ ] Complete Sprint 1 MVP development
- [ ] User acceptance testing for core features
- [ ] Production deployment preparation

### Next Month
- [ ] Sprint 2 planning and execution
- [ ] User feedback collection and analysis
- [ ] Performance optimization

### Next Quarter
- [ ] Feature expansion based on user feedback
- [ ] Scale and performance improvements
- [ ] Market expansion planning

## 🚧 Current Blockers & Risks

### Active Blockers
**Blocker 1**: [Description]
- **Impact**: [How it affects progress]
- **Owner**: [Who is resolving]
- **ETA**: [Expected resolution]

### Risk Mitigation
**Risk 1**: [Risk description]
- **Probability**: [High/Medium/Low]
- **Impact**: [High/Medium/Low]
- **Mitigation**: [Mitigation strategy]

## 📈 Success Tracking

### Business Metrics
- **User Acquisition**: [Current numbers and targets]
- **User Engagement**: [Key engagement metrics]
- **Revenue Metrics**: [If applicable]

### Technical Metrics
- **Performance**: [Load times, response times]
- **Reliability**: [Uptime, error rates]
- **Scalability**: [Current capacity and limits]

## 🔄 Recent Updates
**[Date]**: [Brief update on recent progress]
**[Date]**: [Brief update on recent progress]
**[Date]**: [Brief update on recent progress]

---
*This roadmap is updated after each story completion and major milestone.*
```

---

## 📋 Template: decisions.md

```markdown
# Architectural & Business Decisions Log

**Last Updated**: [YYYY-MM-DD]
**Project**: [Project Name]

## 🎯 Purpose
This document tracks all major decisions made during the project lifecycle, providing context and rationale for future reference and onboarding.

---

## 🏗️ Technical Architecture Decisions

### TAD-001: Technology Stack Selection
**Date**: [YYYY-MM-DD]
**Phase**: Phase 1 - Research
**Decision Maker**: Architect Agent
**Status**: Approved

**Decision**: Use [Technology Stack]
**Rationale**: 
- [Reason 1]: [Explanation]
- [Reason 2]: [Explanation]
- [Reason 3]: [Explanation]

**Alternatives Considered**:
- [Alternative 1]: [Why not chosen]
- [Alternative 2]: [Why not chosen]

**Impact**: [Impact on project timeline, complexity, team]
**Review Date**: [When to review this decision]

### TAD-002: Database Architecture
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Architect Agent
**Status**: Approved

**Decision**: Use [Database Solution]
**Rationale**:
- [Reason 1]: [Explanation]
- [Reason 2]: [Explanation]

**Alternatives Considered**:
- [Alternative 1]: [Why not chosen]

**Impact**: [Impact on scalability, performance, cost]
**Dependencies**: [What depends on this decision]

### TAD-003: Authentication Strategy
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Architect Agent + Developer Agent
**Status**: Approved

**Decision**: Implement [Authentication Method]
**Rationale**:
- [Security considerations]
- [User experience impact]
- [Implementation complexity]

**Security Implications**: [Security considerations]
**User Experience Impact**: [UX considerations]

---

## 💼 Business Decisions

### BAD-001: MVP Scope Definition
**Date**: [YYYY-MM-DD]
**Phase**: Phase 1 - Research
**Decision Maker**: Product Manager Agent
**Status**: Approved

**Decision**: MVP includes [List of features]
**Rationale**:
- [Business value reasoning]
- [Market timing considerations]
- [Resource constraints]

**Excluded from MVP**:
- [Feature 1]: [Why excluded and when to include]
- [Feature 2]: [Why excluded and when to include]

**Success Criteria**: [How MVP success will be measured]
**Review Trigger**: [When to review scope]

### BAD-002: Target Market Focus
**Date**: [YYYY-MM-DD]
**Phase**: Phase 1 - Research
**Decision Maker**: Product Manager Agent
**Status**: Approved

**Decision**: Focus on [Target Market Segment]
**Rationale**:
- [Market size and opportunity]
- [Competitive landscape]
- [Go-to-market strategy alignment]

**Market Research**: [Key research findings supporting decision]
**Competitive Advantage**: [How we differentiate in this market]

---

## 🎨 Design Decisions

### DES-001: Design System Approach
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Designer Agent
**Status**: Approved

**Decision**: Use [Design System/Framework]
**Rationale**:
- [Consistency benefits]
- [Development speed impact]
- [Maintenance considerations]

**Brand Alignment**: [How it aligns with brand]
**Accessibility**: [Accessibility compliance approach]

### DES-002: User Experience Flow
**Date**: [YYYY-MM-DD]
**Phase**: Phase 1 - Research
**Decision Maker**: Designer Agent + Product Manager Agent
**Status**: Approved

**Decision**: Primary user flow is [Flow Description]
**Rationale**:
- [User research findings]
- [Usability testing results]
- [Business goal alignment]

**User Testing**: [Testing results supporting decision]
**Iteration Plan**: [How flow will be refined]

---

## 🔧 Implementation Decisions

### IMP-001: Development Workflow
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Project Manager Agent + Developer Agent
**Status**: Approved

**Decision**: Use [Workflow Strategy]
**Rationale**:
- [Team collaboration benefits]
- [Quality assurance impact]
- [Deployment strategy alignment]

**Branch Strategy**: [Git branching approach]
**Review Process**: [Code review requirements]
**Deployment Process**: [How deployments work]

### IMP-002: Testing Strategy
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: QA Agent + Developer Agent
**Status**: Approved

**Decision**: Implement [Testing Approach]
**Coverage Requirements**: [Test coverage targets]
**Testing Tools**: [Tools and frameworks used]
**Automation Level**: [What's automated vs manual]

---

## 📊 Process Decisions

### PRO-001: Sprint Length and Structure
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Project Manager Agent
**Status**: Approved

**Decision**: [Sprint length] sprints with [Structure]
**Rationale**:
- [Team velocity considerations]
- [Stakeholder feedback cycle]
- [Release planning alignment]

**Review Cadence**: [When sprints are reviewed]
**Adjustment Criteria**: [When to change sprint structure]

### PRO-002: Quality Gates
**Date**: [YYYY-MM-DD]
**Phase**: Phase 2 - Architecture
**Decision Maker**: Project Manager Agent + QA Agent
**Status**: Approved

**Decision**: Implement [Quality Gate Strategy]
**Approval Points**: [When user approval is required]
**Automation**: [What quality checks are automated]
**Escalation**: [How quality issues are escalated]

---

## 🔄 Decision Review Process

### Regular Review Schedule
- **Monthly**: Review all decisions for continued relevance
- **Phase Transitions**: Review phase-specific decisions
- **Major Milestones**: Comprehensive decision review

### Decision Change Process
1. **Identify Need**: Document why decision needs changing
2. **Impact Analysis**: Assess impact of change
3. **Stakeholder Review**: Get appropriate approvals
4. **Implementation Plan**: Plan transition to new decision
5. **Documentation**: Update this log and communicate change

### Decision Categories
- **Reversible**: Can be changed with minimal impact
- **One-way**: Difficult or expensive to reverse
- **Experimental**: Temporary decisions for testing

---

## 📋 Decision Summary

### Current Active Decisions: [X]
### Decisions Under Review: [X]
### Reversed Decisions: [X]

### Key Decision Themes
- **Technology Choices**: [Summary of tech decisions]
- **Business Strategy**: [Summary of business decisions]
- **User Experience**: [Summary of UX decisions]
- **Process & Quality**: [Summary of process decisions]

---
*This log is updated whenever significant decisions are made and reviewed regularly for continued relevance.*
```

---

## 📋 Usage Guidelines

### For Agents:
1. **Always read mission.md first** when starting any phase or major task
2. **Update roadmap.md** after completing each story or major milestone
3. **Document decisions in decisions.md** when making significant choices
4. **Keep context files concise** - detailed information goes in other documents
5. **Update timestamps** whenever making changes

### For Context Management:
- **mission.md**: High-level project context and current status
- **roadmap.md**: Detailed progress tracking and sprint management
- **decisions.md**: Historical record of important choices and rationale

### Quality Standards:
- **Concise**: Context files should be quick to read and understand
- **Current**: Always reflect the actual current state
- **Actionable**: Include next steps and current focus areas
- **Referenced**: Link to detailed documents when appropriate
