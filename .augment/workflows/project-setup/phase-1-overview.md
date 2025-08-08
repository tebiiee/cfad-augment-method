# Augment Develop Method: Project Setup Workflow - Overview

## 🎯 Workflow Purpose
Complete workflow for setting up new projects from initial concept to fully configured development environment with Augment Develop Method integrated.

## 📋 Workflow Structure

### **Total Phases**: 4 phases
### **Estimated Time**: 2-4 hours total
### **Agent Flow**: Project Manager → Product Manager → Designer → Architect → Developer → QA

```
Input Processing → Research & Analysis → Architecture & Planning → Implementation
       ↓                    ↓                      ↓                    ↓
Project Manager → Multiple Agents → Project Manager → Developer/QA
```

---

## 🔄 Phase Navigation

### **📍 Current**: Phase 1 - Overview
**You are here** - Understanding the complete workflow structure

### **➡️ Next**: Phase 2 - Research & Analysis
**File**: `phase-2-research.md`
**Purpose**: Comprehensive research across all domains
**Agents**: Project Manager, Product Manager, Designer, Architect, Developer
**Duration**: ~60-90 minutes

### **🔮 Future Phases**:
- **Phase 3**: Architecture & Planning (`phase-3-planning.md`) - ~45-60 minutes
- **Phase 4**: Implementation (`phase-4-implementation.md`) - Variable duration

---

## 🎭 Agent Roles & Responsibilities

### **Phase 2: Research & Analysis**
- **Project Manager**: Coordination, repository setup, research synthesis
- **Product Manager**: Market research, product definition, business viability
- **Designer**: Design research, UX patterns, visual strategy
- **Architect**: Technical feasibility, architecture planning, rules creation
- **Developer**: Existing code analysis, environment assessment

### **Phase 3: Architecture & Planning**
- **Project Manager**: Phase coordination, story organization
- **Architect**: Technical architecture design
- **Product Manager + Architect**: Feature breakdown and story creation
- **QA + Architect**: Test-driven planning
- **Developer**: Environment setup and CI/CD configuration

### **Phase 4: Implementation**
- **Project Manager**: Sprint coordination, story-by-story management
- **Developer**: TDD implementation of features
- **QA**: Story validation and verification
- **Project Manager**: User approvals and context updates

---

## 📋 Key Deliverables by Phase

### **Phase 2 Outputs**:
- Complete research documentation in `/docs/research/`
- Project blueprint (master synthesis document)
- Project-specific rules in `.augment/rules/`
- Updated context files
- User approval for Phase 3 transition

### **Phase 3 Outputs**:
- Technical architecture documentation
- ALL hyper-detailed stories organized by sprint
- TDD specifications for every story
- Fully configured development environment
- Working CI/CD pipeline
- User approval for Phase 4 transition

### **Phase 4 Outputs**:
- Fully functional MVP
- Complete verification documentation
- Sprint summary with lessons learned
- Production-ready codebase
- User approval for MVP completion

---

## 🚨 Critical Success Factors

### **Quality Gates**
- **Phase 2**: All research complete, blueprint comprehensive, user approved
- **Phase 3**: All stories created, environment ready, pipeline green, user approved
- **Phase 4**: All stories implemented, tests passing, MVP validated, user approved

### **User Approval Points**
- **End of Phase 2**: Project blueprint and research findings
- **End of Phase 3**: All hyper-detailed stories and technical setup
- **Each Story in Phase 4**: Individual story completion
- **End of Phase 4**: Complete MVP functionality

### **Role Declaration Protocol**
Every agent interaction must start with:
```markdown
🎭 **I am acting as [Agent Role]** for [specific task/phase]
```

---

## 🔧 Tools & Resources

### **Always Available**
- **Context7**: Official documentation consultation
- **Sequential Thinking**: Complex problem analysis
- **Codebase Retrieval**: Understanding existing patterns
- **Git Commit Retrieval**: Project history analysis
- **Task Management**: Native Augment Code task management

### **Templates Used**
- **Phase 2**: existing-code-analysis.md, market-analysis.md, product-definition.md, project-blueprint.md
- **Phase 3**: story-template.md
- **Phase 4**: verification-template.md, sprint-summary.md

### **Context Files**
- **Mission**: `.augment/context/mission.md` (project vision and status)
- **Roadmap**: `.augment/context/roadmap.md` (progress and sprint status)
- **Decisions**: `.augment/context/decisions.md` (key decisions and rationale)

---

## 🚀 Getting Started

### **Prerequisites**
- [ ] GitHub repository URL available
- [ ] Project inputs in `/docs/project-input/`
- [ ] methodology-v2.md in project root

### **Phase 1 Completion & Confirmation**
- [ ] **COMMIT**: "workflow: confirm Phase 1 understanding - ready for research phase"
- [ ] **Confirmation**: Explicitly confirm understanding of workflow structure
- [ ] **Documentation**: Ensure all Phase 1 criteria are met

### **Phase 2 Preparation**
- [ ] **Role Declaration**: 🎭 **I am acting as Project Manager** for Phase 2 coordination
- [ ] **Read Context**: Load `.augment/context/mission.md` if exists
- [ ] **Load Workflow**: Continue to `phase-2-research.md`
- [ ] **Initialize Tasks**: Create task management for Phase 2

### **Success Criteria for Phase 1**
- [x] Workflow structure understood
- [x] Agent roles and responsibilities clear
- [x] Phase navigation plan established
- [x] Tools and resources identified
- [x] Ready to begin Phase 2

---

## ➡️ **Next Action**

**Continue to**: `phase-2-research.md`
**Role**: Project Manager (coordination) + Multiple Agents (execution)
**Purpose**: Comprehensive research and analysis across all domains
**Estimated Duration**: 60-90 minutes

---

**Phase 1 Complete** ✅
**Ready for Phase 2** 🚀
