# Augment Develop Method: New Feature Development - Phase 1: Overview

## 🎯 Phase Purpose
Understand the complete new feature development workflow structure, agent roles, and phase navigation before beginning feature analysis.

## 📍 Phase Navigation
- **Previous**: Workflow Selection ✅
- **Current**: Phase 1 - Overview 🔄
- **Next**: Phase 2 - Feature Analysis (`phase-2-analysis.md`)

---

## 📋 Workflow Structure

### **Total Phases**: 4 phases
### **Estimated Time**: 1-3 weeks (depends on feature complexity)
### **Agent Flow**: Project Manager → Product Manager/Designer/Architect → Developer/QA

```
Phase 1: Overview → Phase 2: Analysis → Phase 3: Planning → Phase 4: Implementation
     ↓                    ↓                    ↓                    ↓
Understanding → Requirements & Research → UI-First Planning → Story Development
```

---

## 🔄 **Phase Navigation**

### **📍 Start Here**: Phase 1 - Feature Analysis
**File**: `phase-1-analysis.md`
**Purpose**: Comprehensive feature research and requirements analysis
**Duration**: ~2-3 days
**Agent**: Project Manager, Product Manager, Designer (if UI changes)

### **➡️ Phase 2**: UI-First Planning & Architecture
**File**: `phase-2-planning.md`
**Purpose**: UI-first feature planning and technical architecture
**Duration**: ~2-3 days
**Agents**: Architect, Designer, Product Manager, QA

### **➡️ Phase 3**: Implementation & Validation
**File**: `phase-3-implementation.md`
**Purpose**: Story-by-story feature development with user approvals
**Duration**: Variable (depends on feature scope)
**Agents**: Developer, QA, Project Manager

---

## 📋 **Key Deliverables by Phase**

### **Phase 1 Output**:
- ✅ Complete feature analysis and requirements documentation
- ✅ Integration analysis with existing system
- ✅ User research and competitive analysis
- ✅ Feature specification document
- ✅ User approval for Phase 2 transition

### **Phase 2 Output**:
- ✅ UI/UX design for feature (if applicable)
- ✅ Technical architecture and integration plan
- ✅ Hyper-detailed feature stories with UI-first approach
- ✅ TDD specifications and testing strategy
- ✅ User approval for Phase 3 transition

### **Phase 3 Output**:
- ✅ **Fully functional feature** integrated with existing system
- ✅ Complete verification documentation
- ✅ Feature summary with lessons learned
- ✅ User approval for feature completion

---

## 🎭 **Agent Role Declaration Protocol**

### **MANDATORY for Every Interaction**:
```markdown
🎭 **I am acting as [Agent Role]** for [specific task/phase]
```

### **Role Transitions**:
```markdown
🎭 **Transitioning from [Current Role] to [New Role]**
🎭 **I am now acting as [New Role]** for [next task]
```

---

## 🚨 **Critical Success Factors**

### **Quality Gates**
- **Phase 1**: Feature requirements complete, integration analysis done, user approved
- **Phase 2**: UI design complete (if applicable), stories created, architecture ready, user approved
- **Phase 3**: Feature implemented, tests passing, integration verified, user approved

### **User Approval Points**
- **End of Phase 1**: Feature requirements and analysis
- **End of Phase 2**: Feature design and implementation plan
- **Feature Completion**: Individual feature functionality
- **End of Phase 3**: Complete feature integration

---

## 🎨 **UI-First Considerations**

### **When UI Changes Are Involved**:
- **Phase 2**: Include comprehensive UI/UX design
- **Phase 3**: Implement UI-first approach (visual → interactive → backend)
- **Testing**: Include visual regression and responsive design tests

### **When No UI Changes**:
- **Phase 2**: Focus on API design and data flow
- **Phase 3**: Standard backend-first implementation
- **Testing**: Focus on unit, integration, and API tests

---

## 🚀 **Getting Started**

### **Prerequisites**
- [ ] Existing project with established architecture
- [ ] Feature request or story defined
- [ ] Access to existing codebase and documentation

### **Start the Workflow**
1. **Complete Phase 1**: Understand workflow structure completely
2. **Commit Confirmation**: `git commit -m "workflow: confirm Phase 1 understanding - ready for feature analysis"`
3. **Follow the phase sequence**: 1 → 2 → 3 → 4
4. **Complete each phase fully** before proceeding
5. **Get user approval** at designated checkpoints

---

## ➡️ **Next Action**

**Start with**: `phase-1-analysis.md`
**Purpose**: Comprehensive feature analysis and requirements
**Duration**: ~2-3 days
**Agent**: Project Manager

---

**Workflow Index Complete** ✅
**Ready to Begin** 🚀
