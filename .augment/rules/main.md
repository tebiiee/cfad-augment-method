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

### 3. Workflows Available
- **New Project**: See `.augment/workflows/project-setup.md`
- **New Feature**: See `.augment/workflows/new-feature.md`
- **Bug Fix**: See `.augment/workflows/bug-fix.md`
- **Refactoring**: See `.augment/workflows/refactor.md`
- **UI Work**: See `.augment/workflows/ui-work.md`

### 4. Agent Roles Available
- **Product Manager**: See `.augment/agents/product-manager.md`
- **Designer**: See `.augment/agents/designer.md`
- **Architect**: See `.augment/agents/architect.md`
- **Developer**: See `.augment/agents/developer.md`
- **DevOps**: See `.augment/agents/devops.md` (conditional)
- **QA**: See `.augment/agents/qa.md`
- **Project Manager**: See `.augment/agents/project-manager.md`

## 🚀 Quick Reference

### Before Starting Any Work:
1. **Identify task type** (feature, bug, refactor, UI)
2. **Consult appropriate workflow** in `.augment/workflows/`
3. **Assume correct agent role** from `.augment/agents/`
4. **Apply technical rules** from this directory
5. **Update context** in `.augment/context/` as you work

### Universal Rules (Apply to ALL work):

#### File Organization
- **Stories**: Always in `/docs/current-sprint/stories/`
- **Verification**: Always in `/docs/current-sprint/verification/`
- **Implementation**: Code + docs in `/docs/current-sprint/implementation/`
- **Context Updates**: Maintain `.augment/context/` files

#### Quality Gates
- ✅ **Tests First**: Write tests before implementation (when applicable)
- ✅ **Green CI/CD**: Pipeline must be green before proceeding
- ✅ **Code Review**: Self-review using appropriate agent role
- ✅ **Documentation**: Update relevant context files

#### Commit Standards
- **Format**: `type: description [story-id]`
- **Types**: `feat`, `fix`, `refactor`, `test`, `docs`, `style`
- **Examples**: 
  - `feat: implement user authentication [story-001]`
  - `fix: resolve login validation bug [story-003]`
  - `refactor: optimize database queries [story-005]`

#### Task Management
- **Update States**: Mark tasks as IN_PROGRESS → COMPLETE
- **Dependencies**: Check task dependencies before starting
- **Parallel Work**: Identify independent tasks for parallel execution
- **Blockers**: Document and escalate blockers immediately

## 🔄 Context Loading Strategy

### Smart Loading Rules:
1. **Always Load**: This file (main.md) + current workflow
2. **Conditionally Load**: 
   - Tech stack rules (if writing code)
   - Code style rules (if writing code)
   - Best practices (if making architectural decisions)
   - Project context (if planning or making decisions)

### Memory Management:
- **Use Agent Memories**: For session continuity
- **Clear Context**: Use `/clear` between major task switches
- **Focus**: Load only what's needed for current task

## 🛠️ Tool Integration

### Always Available:
- **Context7**: For official documentation
- **Sequential Thinking**: For complex analysis
- **Playwright**: For E2E testing
- **GitHub Actions**: For CI/CD

### Auto-Configure Based on Stack:
- **Database MCPs**: Based on detected database
- **Cloud MCPs**: Based on deployment target
- **Framework MCPs**: Based on detected frameworks

## 🚨 Critical Rules

### NEVER:
- ❌ Skip writing tests for new functionality
- ❌ Commit broken code
- ❌ Advance phases without completing all criteria
- ❌ Modify files outside current sprint directory during implementation
- ❌ Deploy without green CI/CD pipeline

### ALWAYS:
- ✅ Follow the appropriate workflow for task type
- ✅ Update task states in real-time
- ✅ Document architectural decisions
- ✅ Maintain clean commit history
- ✅ Verify against acceptance criteria

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

### Delivery Quality:
- **Acceptance Criteria**: All stories meet criteria
- **Performance**: No performance regressions
- **Security**: Security considerations addressed

---

**Remember**: This file orchestrates the entire methodology. When in doubt, start here and follow the references to specific files for detailed guidance.
