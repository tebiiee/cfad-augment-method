# Augment Develop Method: Main Rules & Orchestration

## 🎯 Purpose
This file orchestrates all technical rules and standards for the project. It serves as the entry point for understanding how to build software in this codebase.

## 📚 Rule Categories

### 1. Technical Standards
- **Tech Stack**: See `.augment/rules/tech-stack.md`
- **Code Style**: See `.augment/rules/code-style.md`
- **Best Practices**: See `.augment/rules/best-practices.md`

### 2. Project Context
- **Mission**: See `.augment/context/mission.md`
- **Roadmap**: See `.augment/context/roadmap.md`
- **Decisions**: See `.augment/context/decisions.md`

### 3. Dynamic Rules
- **Project-Specific Rules**: See `.augment/methodology/dynamic-rules.md`
- **Workflow Guidelines**: See `.augment/workflows/[workflow-type]/`

---

## 🚀 Quick Start for Agents

### Before Starting Any Work:
1. **Identify task type** (feature, bug, refactor, UI)
2. **Consult appropriate workflow** in `.augment/workflows/`
3. **Assume correct agent role** from `.augment/agents/`
4. **Apply technical rules** from this directory
5. **Update context** in `.augment/context/` as you work

### Universal Rules (Apply to ALL work):

#### File Organization
- **Stories**: Always in `/docs/stories/sprint-1/`, `/docs/stories/sprint-2/`, etc.
- **Verification**: Always in `/docs/verification/sprint-1/`, `/docs/verification/sprint-2/`, etc.
- **Research**: Always in `/docs/research/`
- **Context Updates**: Maintain `.augment/context/` files

#### Agent Role Declaration (MANDATORY)
```markdown
🎭 **I am acting as [Agent Role]** for [specific task/phase]
```

#### Quality Standards
- **Test Coverage**: Write tests for all new functionality
- **Documentation**: Document all architectural decisions
- **Code Review**: Self-review with appropriate agent role
- **CI/CD**: Maintain green pipeline at all times

---

## 📋 Workflow Selection Guide

### For New Projects:
- **Use**: `project-setup` workflow (4 phases)
- **Start with**: `.augment/workflows/project-setup/phase-1-overview.md`

### For Existing Projects:
- **New Features**: Use `new-feature` workflow (4 phases)
- **Bug Fixes**: Use `bug-fix` workflow (3 phases)
- **Code Refactoring**: Use `refactor` workflow (3 phases)
- **UI/UX Work**: Use `ui-work` workflow (3 phases)

---

## ⚠️ Critical Rules

### NEVER:
- ❌ Skip writing tests for new functionality
- ❌ Commit broken code
- ❌ Advance phases without completing all criteria
- ❌ Modify files outside current sprint directory during implementation
- ❌ Deploy without green CI/CD pipeline
- ❌ Create files in `/docs/project-input/` (READ-ONLY for agents)

### ALWAYS:
- ✅ Follow the appropriate workflow for task type
- ✅ Update task states in real-time
- ✅ Document architectural decisions
- ✅ Maintain clean commit history
- ✅ Verify against acceptance criteria
- ✅ Declare agent role before each interaction

## 📋 Phase Transition Rules

### Phase 1 → Phase 2:
- ✅ `.augment/` structure created
- ✅ Project context established
- ✅ MCPs configured
- ✅ CI/CD pipeline green

### Phase 2 → Phase 3:
- ✅ All stories have acceptance criteria
- ✅ Technical specs complete
- ✅ Task breakdown granular and ordered
- ✅ QA tools configured

### Story → Story (Phase 3):
- ✅ Previous story verified and complete
- ✅ All tests passing
- ✅ Code reviewed and committed
- ✅ Context files updated

## 🎯 Success Metrics

### Code Quality:
- **Test Coverage**: Aim for 80%+ on new code
- **CI/CD Health**: Green pipeline at all times
- **Code Review**: Self-review with appropriate agent role

### Process Quality:
- **Documentation**: All decisions documented
- **Task Tracking**: Real-time task state updates
- **Context Maintenance**: `.augment/context/` files current

---

**Note**: This file will be customized with project-specific rules during Phase 1 of project setup.
