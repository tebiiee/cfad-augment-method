# Workflow Selection Guide

## 🎯 Purpose
This guide helps AI agents select the correct workflow based on the user's request and project context.

## 🔍 Workflow Selection Decision Tree

### **1. Analyze User Request**

#### **Keywords that indicate NEW PROJECT (use project-setup):**
- "new project", "start from scratch", "build a new app"
- "create a [type] application"
- Provides repository URL for empty/new repo
- No existing codebase mentioned
- Mentions project concept/idea phase

#### **Keywords that indicate EXISTING PROJECT:**
- "add feature", "implement [feature]", "extend the app"
- "fix bug", "resolve issue", "debug problem"
- "refactor code", "improve performance", "optimize"
- "update UI", "redesign interface", "improve UX"
- Mentions existing codebase or features

### **2. Select Appropriate Workflow**

#### **🆕 NEW PROJECT → project-setup (4 phases)**
```
Use when:
- Starting completely new project
- User provides project concept + repository URL
- No existing codebase or minimal code
- Need comprehensive research and planning

Example prompts:
- "build a new e-commerce app"
- "create a task management system"
- "start a new project for [concept]"
```

#### **✨ NEW FEATURE → new-feature (4 phases)**
```
Use when:
- Adding functionality to existing project
- Project has established codebase
- Need feature analysis and planning
- Working within existing architecture

Example prompts:
- "add user authentication"
- "implement payment system"
- "create admin dashboard"
```

#### **🐛 BUG FIX → bug-fix (3 phases)**
```
Use when:
- Fixing specific issues or bugs
- Debugging existing functionality
- Resolving performance problems
- Correcting broken features

Example prompts:
- "fix login issue"
- "resolve payment bug"
- "debug performance problem"
```

#### **🔧 CODE IMPROVEMENT → refactor (3 phases)**
```
Use when:
- Improving code quality
- Optimizing performance
- Restructuring codebase
- Updating dependencies

Example prompts:
- "refactor authentication code"
- "optimize database queries"
- "improve code structure"
```

#### **🎨 UI/UX WORK → ui-work (3 phases)**
```
Use when:
- Redesigning interface
- Improving user experience
- Updating visual design
- Implementing design system

Example prompts:
- "redesign the dashboard"
- "improve mobile UI"
- "update design system"
```

## 🚨 Critical Selection Rules

### **Default for Ambiguous Cases:**
- **If unclear**: Ask user to clarify project type
- **If new project mentioned**: Use `project-setup`
- **If repository URL provided for new project**: Use `project-setup`

### **Mandatory Checks:**
1. **Read user prompt carefully** for context clues
2. **Check if repository exists** and has existing code
3. **Ask for clarification** if workflow choice is unclear
4. **Always declare agent role** before starting work

## 📋 Workflow Quick Reference

| Workflow | Phases | Use Case | Duration |
|----------|--------|----------|----------|
| **project-setup** | 4 | New projects from scratch | 1-2 weeks |
| **new-feature** | 4 | Add features to existing projects | 3-7 days |
| **bug-fix** | 3 | Fix issues and bugs | 1-3 days |
| **refactor** | 3 | Improve existing code | 2-5 days |
| **ui-work** | 3 | UI/UX improvements | 1-2 weeks |

## 🎭 Agent Role Declaration

**MANDATORY for every interaction:**
```markdown
🎭 **I am acting as [Agent Role]** for [specific task/phase]
```

**Available roles:**
- **Project Manager**: Coordination, planning, user communication
- **Product Manager**: Requirements, user research, feature definition
- **Architect**: Technical architecture, system design
- **Designer**: UI/UX design, user experience
- **Developer**: Implementation, coding, technical work
- **QA**: Testing, validation, quality assurance
- **DevOps**: Infrastructure, deployment, CI/CD

---

**Remember**: When in doubt about workflow selection, ask the user for clarification rather than making assumptions.
