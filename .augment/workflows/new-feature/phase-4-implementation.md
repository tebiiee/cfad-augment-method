# Augment Develop Method: New Feature - Phase 3: Implementation & Validation

## 🎯 Phase Purpose
Story-by-story feature implementation with UI-first approach (if applicable), comprehensive testing, and user approval for feature completion.

## 📍 Phase Navigation
- **Previous**: Phase 2 - UI-First Planning (`phase-2-planning.md`) ✅
- **Current**: Phase 3 - Implementation & Validation 🔄
- **Next**: Feature Complete (Integrated with System)

---

## 🎭 Phase Coordination

### **Coordinated by**: Project Manager
### **Story Cycle Agents**: Developer → QA → Project Manager
### **Duration**: Variable (depends on feature scope)
### **Input**: Complete feature plan with hyper-detailed stories
### **Output**: Fully functional feature integrated with existing system + complete verification documentation

## 🎨 Implementation Strategy

### **UI-First Implementation (if feature involves UI)**:
- **Phase A**: UI Foundation - Components, layouts, navigation
- **Phase B**: Interactive Features - Forms, state management, validation
- **Phase C**: Backend Integration - APIs, data persistence, authentication

### **Backend-First Implementation (if no UI changes)**:
- **Phase A**: Backend Foundation - Data models, business logic, APIs
- **Phase B**: Integration & Testing - System integration, performance, monitoring

---

## 📋 Step-by-Step Process

### **Step 1: Feature Implementation Setup (Project Manager)**

```markdown
🎭 **I am acting as Project Manager** for feature implementation setup

## Feature Implementation Initialization:
- [ ] Read `.augment/context/mission.md` for project alignment
- [ ] Read `.augment/context/roadmap.md` for current status
- [ ] Create `/docs/features/feature-[ID]-[name]/verification/` directory
- [ ] Load all stories from `/docs/features/feature-[ID]-[name]/stories/`
- [ ] Organize stories by dependencies and implementation phases
- [ ] Verify development environment is ready for feature development
- [ ] Set up feature branch workflow: `feature/[ID]-[name]`

## Implementation Strategy Setup:
- [ ] Plan story execution sequence based on dependencies
- [ ] Identify parallel development opportunities
- [ ] Set up feature-specific testing environment
- [ ] Prepare integration testing with existing system
- [ ] Document feature implementation approach

## Task Management:
- [ ] Create task: "Setup: Initialize feature implementation environment"
- [ ] Create task: "Planning: Organize story execution sequence"
- [ ] Create task for EACH story: "Develop: Story [ID] - [Name]"
- [ ] Update tasks to IN_PROGRESS as development begins

## Quality Gate:
- [ ] **COMMIT**: "feat: initialize feature [ID] implementation - [feature name]"
- [ ] Verify all stories are loaded and understood
- [ ] Verify development environment is ready
- [ ] Verify integration approach is clear
```

### **Step 2: Story-by-Story Development Cycle (Developer → QA → Project Manager)**

```markdown
## 🔄 FOR EACH STORY in execution order:

🎭 **Role transitions for each story**: Developer → QA → Project Manager

### Feature Story Development (Developer)
🎭 **I am acting as Developer** for Feature Story [ID] implementation

- [ ] Use Codebase Retrieval to understand existing patterns and integration points
- [ ] Create feature story branch: `feature/story-[ID]-[name]`
- [ ] Read story file completely: `/docs/features/feature-[ID]-[name]/stories/story-[ID]-[name].md`
- [ ] Implement appropriate TDD approach based on story type:
  - **UI Stories**: UI-first TDD (visual → interaction → integration)
  - **Backend Stories**: Traditional TDD (unit → integration → E2E)
- [ ] Follow project-specific rules, conventions, and architecture guidelines
- [ ] Use Context7 for framework documentation when needed
- [ ] Focus implementation on story requirements and acceptance criteria
- [ ] Ensure integration with existing system components
- [ ] Make intermediate commits for risky changes or major milestones
- [ ] Use Augment Code checkpoints for complex implementations

### TDD Implementation Process:
1. **Red Phase**: Write tests first (appropriate to story type)
2. **Green Phase**: Implement minimum code to make tests pass
3. **Refactor Phase**: Improve code quality and maintainability
4. **Integration**: Ensure feature integrates with existing system
5. **Validation**: Verify story meets all acceptance criteria

### Story Validation (QA)
🎭 **I am acting as QA** for Feature Story [ID] validation and verification

- [ ] Run all tests for the story (unit, integration, E2E as appropriate)
- [ ] Execute story-specific test scenarios
- [ ] Verify all acceptance criteria are met
- [ ] Test integration with existing system components
- [ ] Test edge cases and error scenarios
- [ ] Validate performance requirements (if applicable)
- [ ] Check accessibility compliance (if UI story)
- [ ] Verify security requirements (if applicable)
- [ ] Test cross-browser compatibility (if UI story)
- [ ] Verify CI/CD pipeline is green

### Story Verification Documentation (QA)
- [ ] Create `/docs/features/feature-[ID]-[name]/verification/verify-[ID]-[name].md`
- [ ] Document implementation summary and modified files
- [ ] Record test execution results
- [ ] Document integration testing results
- [ ] Note any issues encountered and resolutions
- [ ] Validate story completion against Definition of Done
- [ ] Include screenshots or recordings (if UI story)

### Story Completion (Project Manager)
🎭 **I am acting as Project Manager** for Story [ID] completion and user approval coordination

- [ ] Review story verification documentation
- [ ] Verify story meets all acceptance criteria
- [ ] Test story functionality in staging environment
- [ ] Coordinate user approval for story completion

## User Approval Process (per story):
**What to Present:**
- Working story functionality in staging environment
- Story verification documentation
- Integration testing results
- Any changes or deviations from original plan

**Approval Criteria:**
- Story functionality works as specified
- All acceptance criteria are met
- Integration with existing system is seamless
- Quality standards are maintained
- No breaking changes introduced

**If Not Approved:**
- Request specific feedback on story concerns
- Identify exact functionality needing revision
- Create focused iteration plan for story improvements
- Re-submit revised story within 1-2 days
- Document changes and rationale

- [ ] **STORY ITERATION**: If not approved, iterate based on specific feedback (max 2 times)
- [ ] **STORY APPROVAL**: Mark story complete only after explicit user approval

## Task Management (per story):
- [ ] Update story task to COMPLETE when:
  ✅ All tests written and passing
  ✅ Verification document complete
  ✅ User approval received
  ✅ Story merged to feature branch
- [ ] Create next story task as IN_PROGRESS only after previous story approved
- [ ] Track overall feature progress with approved stories

## Quality Gates per Story (MUST pass before user approval):
- ✅ All tests written and passing (appropriate to story type)
- ✅ All acceptance criteria met and validated
- ✅ Code follows project conventions and standards
- ✅ CI/CD pipeline green for story branch
- ✅ Verification document complete and accurate
- ✅ Integration with existing system verified
- ✅ Feature branch ready for merge
- ✅ No breaking changes to existing functionality
```

### **Step 3: Feature Completion & Integration (Project Manager)**

```markdown
🎭 **I am acting as Project Manager** for feature completion and final integration

## Feature Final Validation:
- [ ] Verify ALL stories in feature are complete and approved
- [ ] Verify ALL verification files exist and are complete
- [ ] Run complete test suite for entire feature
- [ ] Test complete feature functionality end-to-end
- [ ] Verify feature integration with existing system
- [ ] Validate feature against original requirements from Phase 1
- [ ] Check performance and security compliance
- [ ] Test feature in production-like environment

## Feature Integration:
- [ ] Merge feature branch to main/development branch
- [ ] Deploy feature to staging environment
- [ ] Run full regression test suite
- [ ] Verify no breaking changes to existing functionality
- [ ] Test feature with real user data (if applicable)
- [ ] Validate feature performance under load

## Feature Summary Creation:
- [ ] Create `/docs/features/feature-[ID]-[name]/feature-summary.md`
- [ ] Document all completed stories and their impact
- [ ] Record any technical decisions made during implementation
- [ ] Note any deviations from original plan and rationale
- [ ] Document lessons learned and improvements for future features
- [ ] Record final metrics (test coverage, performance, etc.)

## Context Updates:
- [ ] Update `.augment/context/roadmap.md` with feature completion
- [ ] Update `.augment/context/decisions.md` with implementation decisions
- [ ] Document feature in project context for future reference

## Final User Approval Process:
**What to Present:**
- Complete feature functionality in staging environment
- All story verification documentation
- Feature summary and implementation report
- Performance and integration testing results
- Deployment plan and rollback procedures

**Approval Criteria:**
- All feature stories completed and approved individually
- Feature delivers promised functionality and value
- All quality standards met consistently
- Integration with existing system is seamless
- Ready for production deployment

**If Not Approved:**
- Identify specific feature-level concerns
- Create comprehensive improvement plan
- Address systemic issues across stories
- Re-validate complete feature functionality
- Re-submit for final approval

- [ ] **FEATURE ITERATION**: If not approved, iterate based on feedback (max 2 times)
- [ ] **FEATURE MILESTONE**: Feature ready for production deployment

## Task Management:
- [ ] Create task: "Integration: Complete feature integration and testing"
- [ ] Create task: "Summary: Create feature completion documentation"
- [ ] Create task: "Approval: Present complete feature for final approval"
- [ ] Mark all feature tasks as COMPLETE when:
  ✅ Feature integration complete
  ✅ All testing passed
  ✅ Documentation complete
  ✅ User approval received

## Quality Gate:
- [ ] **COMMIT**: "feat: complete feature [ID] implementation - ready for production"
- [ ] Verify feature is fully functional and integrated
- [ ] Verify ready for production deployment
```

---

## 📋 Phase 3 Deliverables

### **Functional Feature**
- ✅ **Fully functional feature** integrated with existing system
- ✅ **All feature stories implemented** and individually approved
- ✅ **All tests passing** with comprehensive coverage
- ✅ **Production-ready code** following project standards

### **Verification Documentation**
- ✅ **Complete verification documentation** for all stories
- ✅ **Feature summary** documenting implementation and lessons learned
- ✅ **Integration testing results** and system compatibility validation

### **Project Integration**
- ✅ **Updated context files** reflecting feature completion
- ✅ **All feature story tasks marked COMPLETE**
- ✅ **User approval** for complete feature functionality
- ✅ **Feature ready for production deployment**

### **Quality Gates Passed**
- ✅ **All feature stories implemented and verified**
- ✅ **Complete test coverage with all tests passing**
- ✅ **Feature integration verified with existing system**
- ✅ **Performance and security requirements met**
- ✅ **CI/CD pipeline green and deployment ready**

---

## ➡️ **Feature Complete**

**Status**: ✅ FEATURE IMPLEMENTED AND INTEGRATED
**Next Steps**: Production deployment or next feature development
**Documentation**: Complete in `/docs/features/feature-[ID]-[name]/`
**User Approval**: ✅ APPROVED for production use
