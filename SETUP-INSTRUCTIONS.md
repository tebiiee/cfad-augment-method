# Augment Develop Method - Setup Instructions

## 🎯 Quick Setup for New Projects

### **What You Need to Copy**
Only **2 items** need to be copied to your new project:

1. **`.augment-template/`** directory → rename to `.augment/`
2. **`methodology.md`** file → copy to project root

### **Step-by-Step Setup**

#### **1. Download/Clone This Repository**
```bash
git clone https://github.com/tebiiee/cfad-augment-method.git
# OR download ZIP and extract
```

#### **2. Copy to Your New Project**
```bash
# Navigate to your new project directory
cd /path/to/your/new/project

# Copy the template (replace [path] with actual path to downloaded repo)
cp -r [path]/cfad-augment-method/.augment-template .augment
cp [path]/cfad-augment-method/methodology.md .
```

**Example:**
```bash
# If you cloned to ~/Downloads/
cp -r ~/Downloads/cfad-augment-method/.augment-template .augment
cp ~/Downloads/cfad-augment-method/methodology.md .
```

#### **3. Prepare Your Project Input**
```bash
mkdir -p docs/project-input
# Add your files:
# - idea.md (main project concept)
# - inspiration/ (screenshots, competitor examples)
# - requirements/ (detailed specifications)
# - assets/ (mockups, design files)
```

#### **4. Start Augment Code Session**
```
"Apply this methodology: ./methodology.md for building [your project description]

Repository: https://github.com/username/project-name.git"
```

## 🔍 What the Agent Will Do

### **Phase 1: Overview & Setup**
- Read ALL files in `/docs/project-input/`
- Archive inputs to `/docs/archived/[timestamp]/` (MANDATORY)
- Create `.augment/context/` files
- Populate `.augment/rules/` with project-specific content
- Select appropriate workflow (project-setup for new projects)

### **Phase 2: Research & Analysis**
- Comprehensive research based on your inputs
- Create research artifacts in `/docs/research/`
- Generate project blueprint

### **Phase 3: Planning**
- Create hyper-detailed stories
- Organize in `/docs/stories/sprint-1/`, `/docs/stories/sprint-2/`, etc.
- Set up verification structure

### **Phase 4: Implementation**
- Story-by-story development with UI-first approach
- Commits per completed story + verification
- User approval for each story

## ⚠️ Critical Rules

### **For Users:**
- ✅ Place ALL project materials in `/docs/project-input/`
- ✅ Use subdirectories for organization (inspiration/, requirements/, assets/)
- ✅ Provide GitHub repository URL
- ❌ Never modify `.augment/` files manually

### **For AI Agents:**
- ✅ MUST declare role: `🎭 **I am acting as [Role]** for [task]`
- ✅ MUST read ALL files in `/docs/project-input/` before starting
- ✅ MUST archive inputs to `/docs/archived/[timestamp]/`
- ✅ MUST make commits at phase transitions and story completions
- ❌ NEVER create or modify files in `/docs/project-input/`

## 📋 Directory Structure After Setup

```
your-project/
├── methodology.md                    # Copied from repo
├── .augment/                        # Copied from .augment-template/
│   ├── agents/                      # Agent role definitions
│   ├── methodology/                 # Core methodology files
│   ├── templates/                   # Document templates
│   ├── workflows/                   # Workflow definitions
│   ├── rules/                       # Populated by agent
│   └── context/                     # Created by agent
├── docs/
│   ├── project-input/               # Your input files (READ-ONLY for agents)
│   ├── archived/                    # Archived inputs (created by agent)
│   ├── research/                    # Research artifacts (created by agent)
│   ├── stories/sprint-1/            # Stories (created by agent)
│   └── verification/sprint-1/       # Verification docs (created by agent)
```

## 🎭 Agent Role Declarations

Every agent interaction must start with:
```markdown
🎭 **I am acting as [Agent Role]** for [specific task]
```

**Available roles:**
- **Project Manager**: Coordination, planning, user communication
- **Product Manager**: Requirements, user research, feature definition
- **Architect**: Technical architecture, system design
- **Designer**: UI/UX design, user experience
- **Developer**: Implementation, coding, technical work
- **QA**: Testing, validation, quality assurance
- **DevOps**: Infrastructure, deployment, CI/CD

## 🔄 Workflow Selection

- **New Project** → `project-setup` (4 phases)
- **Add Feature** → `new-feature` (4 phases)
- **Fix Bug** → `bug-fix` (3 phases)
- **Refactor Code** → `refactor` (3 phases)
- **UI/UX Work** → `ui-work` (3 phases)

## 📊 Hierarchy & Task Management

```
WORKFLOW > PHASE > STEP > TASK > SUB-TASK
```

- **Methodology TASK** = **Augment Code TASK** (1:1 mapping)
- **Story Implementation** = **Single Augment Task**
- **Complex Stories** = **Task with Sub-tasks**

## 🚨 Troubleshooting

### **Agent doesn't archive inputs**
- Check that agent reads this: "MUST archive inputs to `/docs/archived/[timestamp]/`"
- Verify agent declares role before starting

### **Agent creates files in project-input**
- Remind agent: "project-input is READ-ONLY for agents"
- Check agent follows methodology.md rules

### **Wrong workflow selected**
- For new projects, always use `project-setup`
- Check workflow-selection.md for criteria

---

**This setup ensures clean, consistent project initialization without confusion.**
