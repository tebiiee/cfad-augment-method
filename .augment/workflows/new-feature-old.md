# CFAD 2.0: New Feature Workflow

## 🎯 Purpose
Workflow for adding new features to existing projects. Assumes project is already set up with established architecture, development tools, and team processes.

## 🔄 Workflow Overview

```
Requirements → Architecture → Implementation → Testing → Deployment
     ↓              ↓              ↓           ↓          ↓
  Architect     Architect     Developer      QA      Coordinator
```

## 📋 Phase-by-Phase Process

### **PHASE 1: FEATURE RESEARCH & ANALYSIS**
**Coordinated by**: Project Manager (`.augment/agents/project-manager.md`)
**Agents**: Product Manager, Designer (if UI changes), Architect

#### Step 1: Context & Requirements Analysis (Project Manager)
```markdown
## Context Loading & Setup:
- [ ] Read `.augment/context/mission.md` for project alignment
- [ ] Read `.augment/context/roadmap.md` for current sprint status
- [ ] Read story requirements in `/docs/current-sprint/stories/story-[ID].md`
- [ ] Create `/docs/research/feature-[ID]-research/` directory
- [ ] Set up Git branch for feature development
- [ ] Initialize feature research documentation
```

#### Step 2: Feature Research (Product Manager)
```markdown
## Feature Analysis & Research:
- [ ] Understand user needs and business value
- [ ] Research how competitors implement similar features
- [ ] Analyze user feedback and requests related to this feature
- [ ] Identify functional and non-functional requirements
- [ ] Clarify acceptance criteria with stakeholders
- [ ] Document assumptions and constraints
- [ ] Create `/docs/research/feature-[ID]-research/feature-analysis.md`
- [ ] **COMMIT**: "docs: add feature [ID] analysis and research"
```

#### Step 2: Integration Analysis
```markdown
## Integration Analysis:
- [ ] Review existing architecture and established patterns
- [ ] Identify integration points with current features
- [ ] Assess impact on existing system components
- [ ] Consider data flow and state management implications
- [ ] Evaluate performance impact on existing features
- [ ] Check security implications and existing auth patterns
```

#### Step 3: Feature Design
```markdown
## Feature Design Tasks:
- [ ] Use Sequential Thinking for complex feature decisions
- [ ] Design feature components following existing patterns
- [ ] Plan database schema changes (if needed) using existing models
- [ ] Design API endpoints following established conventions
- [ ] Plan error handling consistent with existing patterns
- [ ] Ensure feature fits within existing security model
- [ ] Consider feature flags for gradual rollout
```

#### Step 4: Implementation Planning
```markdown
## Implementation Planning:
- [ ] Break feature into implementable tasks
- [ ] Identify task dependencies and critical path
- [ ] Estimate complexity and effort for each task
- [ ] Plan testing strategy (unit, integration, E2E)
- [ ] Define clear acceptance criteria for each task
- [ ] Document any migration or deployment considerations
```

**Deliverables**:
- Updated story with technical specifications
- Task breakdown in story file
- Feature design that integrates with existing architecture
- Updated decisions in `.augment/context/decisions.md` (if needed)
- Updated roadmap in `.augment/context/roadmap.md`

---

### **PHASE 2: IMPLEMENTATION**
**Agent Role**: Developer (`.augment/agents/developer.md`)

#### Step 1: Pre-Implementation Setup
```markdown
## Setup Checklist:
- [ ] Review technical specifications and acceptance criteria
- [ ] Understand existing code patterns using codebase-retrieval
- [ ] Review existing similar features for consistency
- [ ] Create feature branch from main/develop
- [ ] Verify existing CI/CD pipeline is working
- [ ] Ensure local development environment is up-to-date
```

#### Step 2: Test-Driven Development (Recommended)
```markdown
## TDD Process:
1. **Red**: Write failing test for next piece of functionality
2. **Green**: Write minimal code to make test pass
3. **Refactor**: Improve code while keeping tests green
4. **Repeat**: Continue until feature is complete

## Test Types to Consider:
- [ ] Unit tests for business logic
- [ ] Integration tests for component interactions
- [ ] API tests for endpoints
- [ ] Component tests for UI elements
```

#### Step 3: Implementation
```markdown
## Implementation Guidelines:
- [ ] Follow established code style guidelines in `.augment/rules/code-style.md`
- [ ] Apply project best practices from `.augment/rules/best-practices.md`
- [ ] Use existing tech stack patterns from `.augment/rules/tech-stack.md`
- [ ] Reuse existing components and utilities where possible
- [ ] Implement error handling consistent with existing patterns
- [ ] Add proper logging following existing conventions
- [ ] Ensure accessibility compliance with existing standards
- [ ] Follow existing state management patterns
```

#### Step 4: Code Quality Assurance
```markdown
## Quality Checks:
- [ ] All tests pass (unit, integration)
- [ ] Code follows style guidelines
- [ ] No linting errors or warnings
- [ ] TypeScript compilation successful
- [ ] Performance is acceptable
- [ ] Security considerations addressed
- [ ] Documentation updated (if needed)
```

**Deliverables**:
- Feature implementation with comprehensive tests
- Updated documentation
- Clean commit history with descriptive messages
- Green CI/CD pipeline

---

### **PHASE 3: QUALITY ASSURANCE**
**Agent Role**: QA (`.augment/agents/qa.md`)

#### Step 1: Functional Testing
```markdown
## Functional Testing Checklist:
- [ ] Verify all acceptance criteria are met
- [ ] Test happy path scenarios
- [ ] Test edge cases and error conditions
- [ ] Verify integration with existing features
- [ ] Test user workflows end-to-end
- [ ] Validate data integrity and consistency
```

#### Step 2: Non-Functional Testing
```markdown
## Non-Functional Testing:
- [ ] Performance testing (load times, responsiveness)
- [ ] Security testing (input validation, authentication)
- [ ] Accessibility testing (WCAG compliance)
- [ ] Cross-browser compatibility testing
- [ ] Mobile responsiveness testing
- [ ] Usability testing
```

#### Step 3: Automated Testing
```markdown
## Automated Test Suite:
- [ ] Run full regression test suite
- [ ] Execute E2E tests with Playwright
- [ ] Perform automated accessibility audit
- [ ] Run performance benchmarks
- [ ] Execute security scans
- [ ] Validate API contracts
```

#### Step 4: Bug Reporting & Resolution
```markdown
## Bug Management:
- [ ] Document any issues found
- [ ] Classify bugs by severity and priority
- [ ] Work with Developer agent to resolve issues
- [ ] Verify bug fixes
- [ ] Update test cases to prevent regression
```

**Deliverables**:
- Comprehensive test results
- Bug reports and resolutions
- Updated automated test suite
- Quality metrics and performance data

---

### **PHASE 4: DEPLOYMENT & MONITORING**
**Agent Role**: Coordinator (`.augment/agents/coordinator.md`)

#### Step 1: Pre-Deployment Validation
```markdown
## Deployment Readiness:
- [ ] All acceptance criteria verified
- [ ] Quality gates satisfied
- [ ] Performance benchmarks met
- [ ] Security scans passed
- [ ] Documentation updated
- [ ] Rollback plan prepared
```

#### Step 2: Deployment Process
```markdown
## Deployment Steps:
- [ ] Merge feature branch to main
- [ ] Trigger production deployment
- [ ] Monitor deployment process
- [ ] Verify feature works in production
- [ ] Monitor error rates and performance
- [ ] Communicate deployment status
```

#### Step 3: Post-Deployment Monitoring
```markdown
## Monitoring Checklist:
- [ ] Monitor application performance
- [ ] Check error rates and logs
- [ ] Verify user analytics and usage
- [ ] Monitor business metrics
- [ ] Collect user feedback
- [ ] Document lessons learned
```

**Deliverables**:
- Successfully deployed feature
- Monitoring and alerting configured
- Post-deployment report
- Updated project documentation

---

## 🚨 Quality Gates

### Gate 1: Architecture Review
- ✅ Technical specifications complete and reviewed
- ✅ Architecture decisions documented
- ✅ Task breakdown granular and prioritized
- ✅ Dependencies identified and planned
- ✅ Acceptance criteria clear and testable

### Gate 2: Implementation Review
- ✅ All code implemented according to specifications
- ✅ Comprehensive test coverage
- ✅ Code quality standards met
- ✅ CI/CD pipeline green
- ✅ Performance requirements satisfied

### Gate 3: Quality Assurance
- ✅ All acceptance criteria verified
- ✅ Functional and non-functional testing complete
- ✅ No critical or high-priority bugs
- ✅ Automated tests updated
- ✅ Documentation current

### Gate 4: Deployment Readiness
- ✅ Production deployment successful
- ✅ Feature working as expected
- ✅ Monitoring and alerting active
- ✅ No critical issues detected
- ✅ Stakeholder approval received

## 🔄 Iterative Refinement

### Feedback Loops:
- **Daily**: Progress check and blocker resolution
- **Per Task**: Quality review and acceptance
- **Per Story**: Comprehensive testing and validation
- **Per Sprint**: Retrospective and process improvement

### Continuous Improvement:
- **Process**: Refine workflow based on experience
- **Quality**: Improve testing and validation processes
- **Efficiency**: Optimize development and deployment
- **Communication**: Enhance collaboration between agents

## 📊 Success Metrics

### Development Metrics:
- **Cycle Time**: Time from story start to deployment
- **Quality**: Defect escape rate and customer satisfaction
- **Velocity**: Story points completed per sprint
- **Predictability**: Actual vs. estimated completion

### Technical Metrics:
- **Test Coverage**: Percentage of code covered by tests
- **Performance**: Page load times and response times
- **Reliability**: Uptime and error rates
- **Security**: Vulnerability scan results

---

**Remember**: This workflow emphasizes quality at every step. Don't skip phases or quality gates - they exist to ensure reliable, maintainable software delivery.
