# .augment-template Directory

## 🎯 Purpose
This directory contains the **base template** for new projects using Augment Develop Method. It includes only the essential files that should be copied to new projects, without any project-specific content that would confuse the AI agent.

## 📋 What's Included

### ✅ Template Files (Copy these to new projects)
- **`agents/`** - Agent role definitions and responsibilities
- **`methodology/`** - Core methodology protocols and dynamic rules
- **`templates/`** - Document templates for research, stories, verification
- **`workflows/`** - Complete workflow definitions for all work types
- **`rules/`** - Base rule files (empty, to be populated by agent)

### ❌ NOT Included (Agent will create these)
- **`context/`** - Project-specific context files (mission, roadmap, decisions)
- **Populated rule files** - Tech stack, code style, best practices with actual content

## 🚀 How to Use for New Projects

### Step 1: Copy Template
```bash
# In your new project directory
# Replace [path-to-methodology-repo] with actual path where you downloaded/cloned this repo
cp -r [path-to-methodology-repo]/.augment-template .augment
```

### Step 2: Copy Methodology
```bash
# Replace [path-to-methodology-repo] with actual path where you downloaded/cloned this repo
cp [path-to-methodology-repo]/methodology.md .
```

**Example paths:**
- Local clone: `cp -r ~/Downloads/cfad-augment-method/.augment-template .augment`
- Different location: `cp -r /Users/yourname/projects/cfad-augment-method/.augment-template .augment`

### Step 3: Prepare Project Input
```bash
mkdir -p docs/project-input
# Add your project requirements, ideas, inspiration files here
```

### Step 4: Start Augment Code Session
```
"Apply this methodology: ./methodology.md for building [your project description]"
```

## 🔄 What the Agent Will Create

During Phase 1 (Overview & Setup), the agent will create:
- `.augment/context/mission.md` - Project mission and context
- `.augment/context/roadmap.md` - Project roadmap and progress
- `.augment/context/decisions.md` - Architectural decisions log
- Populate `.augment/rules/` files with project-specific content
- Create project-specific dynamic rules

## ⚠️ Important Notes

### For Project Creators:
- **NEVER modify** files in `.augment-template/` - these are universal
- **ONLY place input files** in `docs/project-input/` - agent reads these but never modifies
- **Let the agent create** all context and rule files during setup

### For AI Agents:
- **READ-ONLY**: Never create or modify files in `docs/project-input/`
- **MUST CREATE**: All files in `.augment/context/` during Phase 1
- **MUST POPULATE**: All rule files in `.augment/rules/` during Phase 1
- **ALWAYS DECLARE**: Your agent role before each interaction

## 📁 Directory Structure After Setup

```
project/
├── methodology.md                    # Copied from template
├── .augment/                        # Copied from .augment-template/
│   ├── agents/                      # ✅ Template (unchanged)
│   ├── methodology/                 # ✅ Template (unchanged)
│   ├── templates/                   # ✅ Template (unchanged)
│   ├── workflows/                   # ✅ Template (unchanged)
│   ├── rules/                       # 🔄 Populated by agent
│   └── context/                     # 🆕 Created by agent
├── docs/
│   ├── project-input/               # 📥 User input (READ-ONLY for agents)
│   ├── research/                    # 🆕 Created by agent
│   ├── stories/sprint-1/            # 🆕 Created by agent
│   └── verification/sprint-1/       # 🆕 Created by agent
```

---

**This template ensures clean project setup without pre-existing content that could confuse the AI agent.**
