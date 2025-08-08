# Augment Develop Method: New Feature - Phase 1: Feature Analysis

## 🎯 Phase Purpose
Comprehensive feature research, requirements analysis, and integration planning to establish solid foundation for feature development.

## 📍 Phase Navigation
- **Previous**: Overview (`overview.md`) ✅
- **Current**: Phase 1 - Feature Analysis 🔄
- **Next**: Phase 2 - UI-First Planning (`phase-2-planning.md`)

---

## 🎭 Phase Coordination

### **Coordinated by**: Project Manager
### **Primary Agents**: Project Manager, Product Manager, Designer (if UI changes)
### **Duration**: ~2-3 days
### **Input**: Feature request or story requirements
### **Output**: Complete feature analysis and requirements documentation

---

## 📋 Step-by-Step Process

### **Step 1: Context Loading & Setup (Project Manager)**

```markdown
🎭 **I am acting as Project Manager** for feature analysis setup

## Context Loading & Setup:
- [ ] Read `.augment/context/mission.md` for project alignment
- [ ] Read `.augment/context/roadmap.md` for current sprint status
- [ ] Read existing feature request or story requirements
- [ ] Use Codebase Retrieval to understand current system architecture
- [ ] Create `/docs/features/feature-[ID]-[name]/` directory
- [ ] Set up Git branch for feature development: `feature/analysis-[ID]-[name]`
- [ ] Initialize feature analysis documentation structure

## Task Management:
- [ ] Create task: "Analysis: Feature [ID] requirements and research"
- [ ] Create task: "Analysis: Integration analysis with existing system"
- [ ] Mark tasks as IN_PROGRESS when starting analysis

## Quality Gate:
- [ ] **COMMIT**: "feat: initialize feature [ID] analysis - [feature name]"
- [ ] Verify all context loaded and understood
- [ ] Verify feature requirements are clear
```

### **Step 2: Feature Requirements Analysis (Product Manager)**

```markdown
🎭 **I am acting as Product Manager** for feature requirements analysis

## Feature Analysis & Research:
- [ ] Use Sequential Thinking for complex feature analysis decisions
- [ ] Understand user needs and business value proposition
- [ ] Research how competitors implement similar features
- [ ] Analyze user feedback and requests related to this feature
- [ ] Identify functional and non-functional requirements
- [ ] Clarify acceptance criteria with stakeholders
- [ ] Document assumptions and constraints
- [ ] Define success metrics and KPIs for the feature
- [ ] Assess feature priority and business impact

## User Research:
- [ ] Identify target user personas for this feature
- [ ] Understand user workflows and pain points
- [ ] Define user journey for the new feature
- [ ] Identify edge cases and error scenarios
- [ ] Document user feedback and validation requirements

## Business Analysis:
- [ ] Assess business value and ROI potential
- [ ] Identify risks and mitigation strategies
- [ ] Define feature scope and boundaries
- [ ] Plan feature rollout and adoption strategy
- [ ] Document compliance and legal considerations

## Documentation:
- [ ] Create `/docs/features/feature-[ID]-[name]/requirements.md`
- [ ] Document all functional requirements
- [ ] Document all non-functional requirements
- [ ] Document user stories and acceptance criteria
- [ ] Document business justification and metrics

## Task Management:
- [ ] Create task: "Research: User needs and competitive analysis"
- [ ] Create task: "Document: Feature requirements specification"
- [ ] Mark tasks as COMPLETE when:
  ✅ All requirements documented and validated
  ✅ User research complete
  ✅ Business analysis complete
  ✅ Stakeholder alignment achieved

## Quality Gate:
- [ ] **COMMIT**: "docs: add feature [ID] requirements and analysis"
- [ ] Verify all requirements are clear and testable
- [ ] Verify business value is well-defined
- [ ] Verify user needs are thoroughly understood
```

### **Step 3: Integration Analysis (Architect)**

```markdown
🎭 **I am acting as Architect** for integration analysis

## System Integration Analysis:
- [ ] Use Codebase Retrieval to understand existing architecture patterns
- [ ] Review existing architecture and established patterns
- [ ] Identify integration points with current features
- [ ] Assess impact on existing system components
- [ ] Consider data flow and state management implications
- [ ] Analyze database schema changes required
- [ ] Identify API endpoints that need modification or creation
- [ ] Assess performance implications of the new feature

## Technical Feasibility:
- [ ] Evaluate technical complexity and implementation effort
- [ ] Identify potential technical risks and challenges
- [ ] Assess compatibility with current tech stack
- [ ] Consider scalability implications
- [ ] Evaluate security considerations
- [ ] Assess testing requirements and strategies

## Dependency Analysis:
- [ ] Identify dependencies on existing features
- [ ] Identify dependencies on external services
- [ ] Map feature dependencies and prerequisites
- [ ] Assess impact on CI/CD pipeline
- [ ] Consider deployment and rollback strategies

## Documentation:
- [ ] Create `/docs/features/feature-[ID]-[name]/integration-analysis.md`
- [ ] Document all integration points
- [ ] Document technical risks and mitigation strategies
- [ ] Document performance and scalability considerations
- [ ] Document security and compliance requirements

## Task Management:
- [ ] Create task: "Architecture: Integration analysis and technical feasibility"
- [ ] Create task: "Architecture: Dependency mapping and risk assessment"
- [ ] Mark tasks as COMPLETE when:
  ✅ Integration analysis complete
  ✅ Technical feasibility confirmed
  ✅ Dependencies mapped
  ✅ Risks identified and mitigated

## Quality Gate:
- [ ] **COMMIT**: "docs: add feature [ID] integration analysis and technical assessment"
- [ ] Verify integration approach is sound
- [ ] Verify technical feasibility is confirmed
- [ ] Verify all dependencies are identified
```

### **Step 4: UI/UX Impact Assessment (Designer)**

```markdown
🎭 **I am acting as Designer** for UI/UX impact assessment

## UI/UX Impact Analysis (if feature involves UI changes):
- [ ] Assess impact on existing user interface
- [ ] Identify new UI components or screens needed
- [ ] Evaluate consistency with existing design system
- [ ] Consider responsive design requirements
- [ ] Assess accessibility implications (WCAG compliance)
- [ ] Evaluate user experience flow changes
- [ ] Consider mobile and desktop experience differences

## Design Requirements:
- [ ] Define visual design requirements
- [ ] Identify interaction patterns needed
- [ ] Plan component library additions or modifications
- [ ] Consider animation and micro-interaction needs
- [ ] Plan user feedback and error handling UI
- [ ] Define loading states and empty states

## User Experience Planning:
- [ ] Map user journey for the new feature
- [ ] Identify potential UX friction points
- [ ] Plan user onboarding for new feature
- [ ] Consider feature discoverability
- [ ] Plan user education and help content

## Documentation:
- [ ] Create `/docs/features/feature-[ID]-[name]/ui-ux-requirements.md` (if applicable)
- [ ] Document UI/UX requirements and specifications
- [ ] Document design system impact
- [ ] Document user experience considerations
- [ ] Document accessibility requirements

## Task Management:
- [ ] Create task: "Design: UI/UX impact assessment and requirements"
- [ ] Create task: "Design: User experience flow planning"
- [ ] Mark tasks as COMPLETE when:
  ✅ UI/UX impact assessed
  ✅ Design requirements defined
  ✅ User experience planned
  ✅ Accessibility considered

## Quality Gate:
- [ ] **COMMIT**: "docs: add feature [ID] UI/UX requirements and impact assessment"
- [ ] Verify UI/UX requirements are comprehensive
- [ ] Verify design system impact is understood
- [ ] Verify user experience is well-planned
```

### **Step 5: Phase 1 Completion & User Approval (Project Manager)**

```markdown
🎭 **I am acting as Project Manager** for Phase 1 completion and user approval

## Phase 1 Final Validation:
- [ ] Review all analysis documentation for completeness
- [ ] Verify requirements are clear and testable
- [ ] Verify integration analysis is comprehensive
- [ ] Verify UI/UX requirements are defined (if applicable)
- [ ] Ensure all risks and dependencies are identified
- [ ] Validate feature scope and boundaries are clear

## Documentation Consolidation:
- [ ] Create `/docs/features/feature-[ID]-[name]/phase-1-summary.md`
- [ ] Consolidate all analysis findings
- [ ] Document key decisions and rationale
- [ ] Summarize risks and mitigation strategies
- [ ] Prepare executive summary for stakeholders

## Context Updates:
- [ ] Update `.augment/context/roadmap.md` with feature analysis status
- [ ] Update `.augment/context/decisions.md` with key decisions made
- [ ] Document feature in project context for future reference

## Task Management:
- [ ] Create task: "Summary: Consolidate Phase 1 analysis and findings"
- [ ] Create task: "Approval: Present analysis for user approval"
- [ ] Mark Phase 1 tasks as COMPLETE when:
  ✅ All analysis complete and documented
  ✅ Documentation consolidated
  ✅ Context updated
  ✅ Ready for user approval

## User Approval Process:
**What to Present:**
- Complete feature requirements and analysis
- Integration analysis and technical feasibility
- UI/UX requirements (if applicable)
- Risk assessment and mitigation strategies
- Recommended implementation approach

**Approval Criteria:**
- Feature requirements are clear and complete
- Business value is well-justified
- Technical approach is sound and feasible
- Risks are identified and acceptable
- Resource requirements are understood

**If Not Approved:**
- Request specific feedback on analysis concerns
- Identify exact requirements or analysis needing revision
- Create focused iteration plan for analysis improvements
- Re-submit revised analysis within 1-2 days
- Document changes and rationale

- [ ] **ANALYSIS ITERATION**: If not approved, iterate based on specific feedback (max 2 times)
- [ ] **PHASE APPROVAL**: Only proceed to Phase 2 after explicit user approval

## Quality Gate:
- [ ] **COMMIT**: "docs: complete feature [ID] Phase 1 analysis - ready for planning"
- [ ] Verify all analysis is complete and approved
- [ ] Verify ready to proceed to Phase 2 planning
```

---

## 📋 Phase 1 Deliverables

### **Analysis Documentation**
- ✅ `/docs/features/feature-[ID]-[name]/requirements.md`
- ✅ `/docs/features/feature-[ID]-[name]/integration-analysis.md`
- ✅ `/docs/features/feature-[ID]-[name]/ui-ux-requirements.md` (if applicable)
- ✅ `/docs/features/feature-[ID]-[name]/phase-1-summary.md`

### **Project Context Updates**
- ✅ Updated `.augment/context/roadmap.md` with feature status
- ✅ Updated `.augment/context/decisions.md` with key decisions
- ✅ Feature analysis complete and documented

### **Quality Gates Passed**
- ✅ All requirements documented and validated
- ✅ Integration analysis complete and feasible
- ✅ UI/UX requirements defined (if applicable)
- ✅ Risks identified and mitigation planned
- ✅ User approval received for Phase 2 transition

---

## ➡️ **Next Phase**

**Continue to**: `phase-2-planning.md`
**Purpose**: UI-First Planning & Architecture - Convert analysis to implementable plan
**Duration**: ~2-3 days
**Input**: Complete feature analysis from Phase 1
**Output**: UI-first feature plan with hyper-detailed stories ready for implementation
