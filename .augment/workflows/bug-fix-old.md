# CFAD 2.0: Bug Fix Workflow

## 🎯 Purpose
Streamlined workflow for investigating, fixing, and validating bug reports efficiently while preventing regression.

## 🔄 Workflow Overview

```
Bug Report → Investigation → Root Cause → Fix → Validation → Prevention
     ↓            ↓             ↓         ↓        ↓           ↓
Coordinator   Developer     Developer  Developer   QA      Developer
```

## 📋 Phase-by-Phase Process

### **PHASE 1: BUG TRIAGE & INVESTIGATION**
**Agent Role**: Developer (`.augment/agents/developer.md`)

#### Step 1: Bug Analysis
```markdown
## Bug Triage Checklist:
- [ ] Read bug report thoroughly
- [ ] Classify severity (Critical, High, Medium, Low)
- [ ] Classify priority (P1, P2, P3, P4)
- [ ] Identify affected components and users
- [ ] Determine if it's a regression or existing issue
- [ ] Check for duplicate reports
```

#### Step 2: Reproduction
```markdown
## Reproduction Steps:
- [ ] Follow exact steps from bug report
- [ ] Try to reproduce in different environments
- [ ] Document reproduction steps if different from report
- [ ] Capture screenshots, logs, or error messages
- [ ] Identify minimum steps to reproduce
- [ ] Note any environmental factors
```

#### Step 3: Initial Investigation
```markdown
## Investigation Tasks:
- [ ] Use codebase-retrieval to understand affected code
- [ ] Use git-commit-retrieval to check recent changes
- [ ] Review related code and dependencies
- [ ] Check logs and error tracking systems
- [ ] Identify potential root causes
- [ ] Estimate fix complexity
```

**Deliverables**:
- Confirmed reproduction steps
- Initial root cause hypothesis
- Severity and priority classification
- Estimated fix effort

---

### **PHASE 2: ROOT CAUSE ANALYSIS**
**Agent Role**: Developer (`.augment/agents/developer.md`)

#### Step 1: Deep Investigation
```markdown
## Root Cause Analysis:
- [ ] Trace code execution path
- [ ] Identify where the bug occurs
- [ ] Understand why the bug occurs
- [ ] Check for similar issues in codebase
- [ ] Review related test coverage
- [ ] Identify contributing factors
```

#### Step 2: Impact Assessment
```markdown
## Impact Analysis:
- [ ] Determine scope of affected functionality
- [ ] Identify affected user segments
- [ ] Assess data integrity implications
- [ ] Check for security implications
- [ ] Evaluate performance impact
- [ ] Consider business impact
```

#### Step 3: Solution Planning
```markdown
## Solution Design:
- [ ] Design fix approach
- [ ] Consider alternative solutions
- [ ] Evaluate fix complexity and risk
- [ ] Plan testing strategy
- [ ] Identify potential side effects
- [ ] Plan rollback strategy if needed
```

**Deliverables**:
- Root cause analysis document
- Proposed solution with rationale
- Risk assessment
- Testing plan

---

### **PHASE 3: IMPLEMENTATION & TESTING**
**Agent Role**: Developer (`.augment/agents/developer.md`)

#### Step 1: Test Creation (Test-First Approach)
```markdown
## Test-First Implementation:
- [ ] Write failing test that reproduces the bug
- [ ] Ensure test fails for the right reason
- [ ] Write additional edge case tests
- [ ] Verify test coverage for affected code
- [ ] Run test suite to confirm failure
```

#### Step 2: Bug Fix Implementation
```markdown
## Fix Implementation:
- [ ] Implement minimal fix to make tests pass
- [ ] Follow code style guidelines
- [ ] Ensure fix doesn't break existing functionality
- [ ] Add proper error handling
- [ ] Update documentation if needed
- [ ] Add logging for debugging if appropriate
```

#### Step 3: Validation
```markdown
## Fix Validation:
- [ ] Verify original bug is fixed
- [ ] Run full test suite
- [ ] Test edge cases and related functionality
- [ ] Verify no new issues introduced
- [ ] Test in different environments
- [ ] Validate performance impact
```

**Deliverables**:
- Bug fix implementation
- Comprehensive test coverage
- Validation that bug is resolved
- No regression in existing functionality

---

### **PHASE 4: QUALITY ASSURANCE**
**Agent Role**: QA (`.augment/agents/qa.md`)

#### Step 1: Fix Verification
```markdown
## QA Verification:
- [ ] Verify bug is fixed using original reproduction steps
- [ ] Test edge cases and variations
- [ ] Verify fix works across different browsers/devices
- [ ] Test related functionality for regression
- [ ] Validate user experience improvements
```

#### Step 2: Regression Testing
```markdown
## Regression Testing:
- [ ] Run automated regression test suite
- [ ] Test related features manually
- [ ] Verify integration points still work
- [ ] Check for performance regressions
- [ ] Validate security hasn't been compromised
```

#### Step 3: Acceptance Testing
```markdown
## Acceptance Criteria:
- [ ] Original issue is resolved
- [ ] No new bugs introduced
- [ ] Performance is maintained or improved
- [ ] User experience is improved
- [ ] All tests pass
- [ ] Documentation is updated
```

**Deliverables**:
- QA validation report
- Regression test results
- Performance impact assessment
- Approval for deployment

---

### **PHASE 5: DEPLOYMENT & MONITORING**
**Agent Role**: Coordinator (`.augment/agents/coordinator.md`)

#### Step 1: Deployment Planning
```markdown
## Deployment Strategy:
- [ ] Plan deployment timing (consider user impact)
- [ ] Prepare rollback plan
- [ ] Set up monitoring for the fix
- [ ] Communicate fix to stakeholders
- [ ] Plan post-deployment validation
```

#### Step 2: Deployment Execution
```markdown
## Deployment Process:
- [ ] Deploy fix to staging environment
- [ ] Validate fix in staging
- [ ] Deploy to production
- [ ] Monitor deployment process
- [ ] Verify fix works in production
```

#### Step 3: Post-Deployment Monitoring
```markdown
## Monitoring Checklist:
- [ ] Monitor error rates and logs
- [ ] Check user feedback and reports
- [ ] Validate business metrics
- [ ] Monitor performance metrics
- [ ] Confirm no new issues reported
```

**Deliverables**:
- Successfully deployed fix
- Monitoring data showing resolution
- Stakeholder communication
- Lessons learned documentation

---

## 🚨 Severity-Based Workflows

### Critical Bugs (P1):
```markdown
## Critical Bug Process:
- **Timeline**: Fix within 2-4 hours
- **Process**: Skip non-essential steps, focus on immediate fix
- **Testing**: Minimal testing, deploy hotfix, comprehensive testing after
- **Communication**: Immediate stakeholder notification
- **Rollback**: Have immediate rollback plan ready
```

### High Priority Bugs (P2):
```markdown
## High Priority Process:
- **Timeline**: Fix within 1-2 days
- **Process**: Follow full workflow but expedited
- **Testing**: Comprehensive testing before deployment
- **Communication**: Regular stakeholder updates
- **Rollback**: Standard rollback procedures
```

### Medium/Low Priority Bugs (P3/P4):
```markdown
## Standard Process:
- **Timeline**: Fix in current or next sprint
- **Process**: Follow complete workflow
- **Testing**: Full testing and validation
- **Communication**: Standard sprint communication
- **Rollback**: Standard procedures
```

## 🔍 Investigation Techniques

### Code Analysis:
```markdown
## Code Investigation Tools:
- **Codebase Retrieval**: Understand current implementation
- **Git Commit Retrieval**: Check recent changes and history
- **Sequential Thinking**: For complex debugging scenarios
- **Context7**: For framework/library specific issues
```

### Debugging Strategies:
```markdown
## Debugging Approaches:
1. **Reproduce Consistently**: Ensure reliable reproduction
2. **Isolate Variables**: Change one thing at a time
3. **Binary Search**: Narrow down the problem area
4. **Rubber Duck**: Explain the problem to understand it better
5. **Fresh Eyes**: Get another perspective if stuck
```

## 🧪 Testing Strategies

### Bug-Specific Testing:
```markdown
## Test Types for Bug Fixes:
- **Reproduction Test**: Test that reproduces the original bug
- **Fix Validation Test**: Test that verifies the fix works
- **Edge Case Tests**: Test boundary conditions and edge cases
- **Regression Tests**: Ensure no existing functionality breaks
- **Integration Tests**: Verify system interactions still work
```

### Test Automation:
```markdown
## Automated Testing:
- [ ] Add unit tests for the bug scenario
- [ ] Add integration tests if multiple components involved
- [ ] Add E2E tests for user-facing bugs
- [ ] Update existing tests if they need modification
- [ ] Ensure CI/CD pipeline includes new tests
```

## 📊 Bug Prevention

### Root Cause Categories:
```markdown
## Common Root Causes:
- **Logic Errors**: Incorrect business logic implementation
- **Edge Cases**: Unhandled boundary conditions
- **Integration Issues**: Problems between components
- **Data Issues**: Invalid or unexpected data
- **Environment Issues**: Configuration or deployment problems
- **Race Conditions**: Timing-related issues
```

### Prevention Strategies:
```markdown
## Prevention Measures:
- [ ] Improve test coverage in affected areas
- [ ] Add validation for edge cases
- [ ] Improve error handling
- [ ] Add monitoring and alerting
- [ ] Update documentation
- [ ] Share learnings with team
```

## 📋 Quality Gates

### Investigation Complete:
- ✅ Bug reproduced consistently
- ✅ Root cause identified
- ✅ Solution approach defined
- ✅ Risk assessment completed

### Fix Complete:
- ✅ Bug fix implemented
- ✅ Tests written and passing
- ✅ No regression detected
- ✅ Code review completed

### QA Complete:
- ✅ Fix verified by QA
- ✅ Regression testing passed
- ✅ Performance validated
- ✅ Ready for deployment

### Deployment Complete:
- ✅ Fix deployed successfully
- ✅ Monitoring shows resolution
- ✅ No new issues detected
- ✅ Stakeholders notified

---

**Remember**: The goal is not just to fix the bug, but to understand why it happened and prevent similar issues in the future. Always think about the broader implications and learning opportunities.
