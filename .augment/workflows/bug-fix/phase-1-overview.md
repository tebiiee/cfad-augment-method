# Augment Develop Method: Bug Fix Workflow

## 🎯 Workflow Purpose
Systematic bug investigation, root cause analysis, and resolution with comprehensive testing and user validation.

## 📋 Workflow Structure

### **Total Phases**: 2 phases
### **Estimated Time**: 1-5 days (depends on bug complexity)
### **Agent Flow**: Project Manager → Developer/QA → Project Manager

```
Phase 1: Investigation → Phase 2: Resolution
     ↓                        ↓
Root Cause Analysis → Fix Implementation & Testing
```

---

## 🔄 **Phase Navigation**

### **📍 Start Here**: Phase 1 - Bug Investigation
**File**: `phase-1-investigation.md`
**Purpose**: Comprehensive bug analysis and root cause identification
**Duration**: ~1-2 days
**Agent**: Project Manager, Developer, QA

### **➡️ Phase 2**: Bug Resolution & Validation
**File**: `phase-2-resolution.md`
**Purpose**: Fix implementation with comprehensive testing and validation
**Duration**: ~1-3 days (depends on complexity)
**Agents**: Developer, QA, Project Manager

---

## 📋 **Key Deliverables by Phase**

### **Phase 1 Output**:
- ✅ Complete bug analysis and reproduction steps
- ✅ Root cause identification and impact assessment
- ✅ Fix strategy and implementation plan
- ✅ User approval for resolution approach

### **Phase 2 Output**:
- ✅ **Bug fix implemented** with comprehensive testing
- ✅ Complete verification documentation
- ✅ Regression testing passed
- ✅ User approval for fix completion

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
- **Phase 1**: Bug reproduced, root cause identified, fix strategy approved
- **Phase 2**: Fix implemented, all tests passing, regression verified, user approved

### **User Approval Points**
- **End of Phase 1**: Bug analysis and proposed fix strategy
- **End of Phase 2**: Complete bug fix and verification

---

## 🔍 **Bug Classification**

### **Critical Bugs**:
- System crashes or data loss
- Security vulnerabilities
- Complete feature failures
- **Timeline**: Immediate resolution required

### **High Priority Bugs**:
- Major functionality impaired
- Significant user experience issues
- Performance degradation
- **Timeline**: 1-2 days resolution

### **Medium Priority Bugs**:
- Minor functionality issues
- UI/UX inconsistencies
- Non-critical performance issues
- **Timeline**: 3-5 days resolution

### **Low Priority Bugs**:
- Cosmetic issues
- Edge case scenarios
- Minor improvements
- **Timeline**: Next sprint or maintenance cycle

---

## 🚀 **Getting Started**

### **Prerequisites**
- [ ] Bug report with clear description
- [ ] Access to affected system/environment
- [ ] Reproduction steps (if available)

### **Start the Workflow**
1. **Begin with**: `phase-1-investigation.md`
2. **Follow the phase sequence**: 1 → 2
3. **Complete each phase fully** before proceeding
4. **Get user approval** at designated checkpoints

---

## ➡️ **Next Action**

**Start with**: `phase-1-investigation.md`
**Purpose**: Comprehensive bug investigation and root cause analysis
**Duration**: ~1-2 days
**Agent**: Project Manager

---

**Workflow Index Complete** ✅
**Ready to Begin** 🚀
