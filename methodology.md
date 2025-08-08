# Augment Develop Method
## Comprehensive Development Methodology for Modern Software Development

### 🚀 What's New in Augment Develop Method

**Augment Develop Method** is a comprehensive development methodology with **4-phase UI-first approach**, modular architecture, specialized agent roles, and intelligent workflow selection inspired by Claude Code Agents and Agent OS best practices.

### ✨ Key Enhancements

- **🎨 UI-First Development**: Visual foundation → Interactive UI → Backend integration
- **🧩 Modular Architecture**: Small, focused files with cascading references
- **🤖 Specialized Agent Roles**: Product Manager, Designer, Architect, Developer, QA, Project Manager, DevOps (conditional)
- **🔄 Intelligent Workflows**: Automatic workflow selection by task type
- **📚 Layered Context**: Standards → Product → Specs architecture
- **🎯 Smart Context Loading**: Load only what's needed for current task

## 📁 Project Structure

```
/docs/                          # Project documentation structure
  /project-input/               # 📥 User inputs (READ-ONLY for agents - ideas, notes, screenshots, etc.)
  /archived/                    # Archived project inputs by timestamp
    /2024-01-15-143022/         # Example: archived inputs from specific session
  /research/                    # Phase 2: Research artifacts (for project-setup workflow)
    existing-code-analysis.md   # Analysis of existing codebase
    market-analysis.md          # Market research and competition
    product-definition.md       # Product strategy and features
    design-research.md          # Design patterns and UX research
    technical-feasibility.md    # Technical analysis and architecture
    business-viability.md       # Business model and financial analysis
    project-blueprint.md        # Master synthesis document (Phase 1 output)
  /stories/                     # Phase 2: Hyper-detailed stories by sprint
    /sprint-1/                  # MVP stories (ready for implementation)
      story-001-user-auth.md    # Example: User authentication story
      story-002-dashboard.md    # Example: Dashboard implementation story
    /sprint-2/                  # Post-MVP stories (ready for future development)
      story-004-profiles.md     # Example: User profiles story
    /sprint-3/                  # Future features (if applicable)
  /verification/                # Phase 3: Story completion verification
    /sprint-1/                  # Verification documents for Sprint 1
      verify-001-user-auth.md   # Verification for user auth story
      verify-002-dashboard.md   # Verification for dashboard story
    /sprint-2/                  # Verification documents for Sprint 2
  /sprint-summaries/            # Sprint completion summaries
    sprint-1-summary.md         # Sprint 1 completion summary
    sprint-2-summary.md         # Sprint 2 completion summary

/.augment/                      # NEW: Modular methodology files
  /rules/                       # Technical rules and standards
    main.md                     # Main rules (orchestrates others)
    tech-stack.md              # Technology stack preferences
    code-style.md              # Code style guidelines
    best-practices.md          # Development best practices
  /agents/                      # Specialized agent roles
    product-manager.md         # Product vision and requirements
    designer.md                # UI/UX design and user experience
    architect.md               # Design and architecture decisions
    developer.md               # Implementation and coding (+ basic DevOps)
    devops.md                  # Advanced infrastructure (conditional)
    qa.md                      # Testing and validation
    project-manager.md         # Project orchestration and management
  /workflows/                   # Task-specific workflows (standardized by phases)
    project-setup/             # Complete project setup (4-phase UI-first)
    new-feature/               # Complete feature development (3-phase UI-first)
    bug-fix/                   # Bug investigation and fixing (2-phase)
    refactor/                  # Code refactoring process (3-phase)
    ui-work/                   # UI/UX implementation (3-phase design-first)
  /methodology/                 # Detailed methodology protocols
    protocols.md               # Tool usage, quality gates, task management
    dynamic-rules.md           # Project-specific rules creation
  /templates/                   # Templates for consistent documentation
    research-artifacts.md      # All templates: research, stories, verification, summaries
    context-files.md           # Templates for context files (mission, roadmap, decisions)
  /context/                     # Project context and decisions (created from templates)
    mission.md                 # Project mission and current status
    roadmap.md                 # Sprint progress and timeline
    decisions.md               # All major decisions with rationale
```

## 🎯 How to Use Augment Develop Method

### Step 1: Specify Your Work Type
Tell the agent what you want to do:
```
"Let's start a new project" → project-setup/ (4-phase UI-first)
"Let's add new features to this project" → new-feature/ (3-phase UI-first)
"Let's fix some bugs" → bug-fix/ (2-phase systematic)
"Let's optimize the code" → refactor/ (3-phase safe)
"Let's improve the UI/UX" → ui-work/ (3-phase design-first)
```

### Step 2: Automatic Input Processing
The agent will automatically:
1. **Read Project Inputs**: Process all files in `/docs/project-input/`
2. **Archive Inputs**: Move them to `/docs/archived/[timestamp]/` for future reference
3. **Select Workflow**: Choose appropriate workflow from `.augment/workflows/`
4. **Begin Methodology**: Start the enhanced multi-phase process (2-4 phases depending on workflow)

### Workflow Selection Process

1. **User Specifies Work Type**: You tell the agent what kind of work to do
2. **Input Processing**: Agent reads and archives project inputs
3. **Workflow Selection**: Agent selects appropriate workflow file
4. **Role Assignment**: Agent assumes correct role from `.augment/agents/`
5. **Rule Application**: Agent applies standards from `.augment/rules/`
6. **Context Maintenance**: Agent updates `.augment/context/` throughout

### Supported Work Types

| Work Type | Workflow File | Agent Flow | Description | When to Use |
|-----------|---------------|------------|-------------|-------------|
| **New Project** | `project-setup/` | PM → Designer → Architect → Developer → QA | Complete project setup with 4-phase UI-first approach (Overview → Research → Planning → Implementation) | Starting from scratch, new repository, project concept |
| **New Features** | `new-feature/` | PM → Designer → Architect → Developer → QA | Add functionality with 4-phase UI-first approach (Overview → Analysis → Planning → Implementation) | Existing project, adding features |
| **Bug Fixes** | `bug-fix/` | PM → Developer → QA | Investigation and resolution with 3-phase systematic approach (Overview → Investigation → Resolution) | Fixing issues, debugging problems |
| **Code Optimization** | `refactor/` | PM → Architect → Developer → QA | Safe code improvement with 3-phase approach (Overview → Analysis → Implementation) | Improving code quality, performance |
| **UI/UX Work** | `ui-work/` | Designer → Developer → QA | Interface implementation with 3-phase design-first approach (Overview → Design → Implementation) | Redesigning interface, UX improvements |

### **🔍 Workflow Selection Guide**
- **See**: `.augment/workflows/workflow-selection.md` for detailed selection criteria
- **Default for new projects**: Always use `project-setup` workflow
- **When unclear**: Ask user to clarify project type and requirements

**Note**: DevOps agent activates automatically for complex projects requiring advanced infrastructure (Docker, Kubernetes, IaC).

## 📋 Methodology Hierarchy & Structure

### **Work Structure Hierarchy**
```
WORKFLOW (e.g., project-setup, new-feature, bug-fix)
├── PHASE 1: Overview & Setup
├── PHASE 2: Research/Analysis
├── PHASE 3: Planning/Implementation
└── PHASE 4: Implementation (project-setup only)
    ├── STEP 1: Environment Setup
    ├── STEP 2: Story Development Cycle
    └── STEP 3: Quality Validation
        ├── TASK: Write Tests
        ├── TASK: Run CI/CD
        └── TASK: User Approval
            ├── SUB-TASK: Demo Preparation
            └── SUB-TASK: Documentation Review
```

### **Critical Rules for AI Agents**

#### **🚫 NEVER DO:**
- ❌ Create or modify files in `/docs/project-input/` (READ-ONLY)
- ❌ Skip agent role declaration before interactions
- ❌ Advance phases without completing all mandatory steps
- ❌ Commit broken code or skip CI/CD validation
- ❌ Start work without reading project-input files first

#### **✅ ALWAYS DO:**
- ✅ Declare agent role: `🎭 **I am acting as [Role]** for [task]`
- ✅ Read ALL files in `/docs/project-input/` before starting research
- ✅ Create mandatory commits at phase transitions
- ✅ Update `.augment/context/` files as work progresses
- ✅ Follow UI-first approach for all development work

#### **📥 Project Input Rules**
- **For Users**: Place ALL project requirements, ideas, inspiration, screenshots, competitor examples in `/docs/project-input/`
- **For Agents**: READ and ANALYZE all project-input files, but NEVER create or modify them
- **Structure**: Use subdirectories like `inspiration/`, `requirements/`, `assets/` for organization

## 🔄 Enhanced Multi-Phase Process

### **PHASE 1: OVERVIEW & SETUP** ⏱️ ~10-15 minutes

**Auto-Detection & Setup**:
- ✅ Detect project type and existing state
- ✅ Configure `.augment/` structure automatically
- ✅ Set up appropriate MCPs based on detected stack
- ✅ Initialize context files with project analysis

**Context Establishment**:
- ✅ Create `.augment/context/mission.md` with project goals
- ✅ Generate `.augment/rules/` based on detected patterns
- ✅ Configure GitHub Actions and CI/CD automatically
- ✅ Set up QA tools (Playwright, testing frameworks)

### **PHASE 2: RESEARCH & ANALYSIS** ⏱️ ~20-30 minutes

**Research Activities** (varies by workflow):
- ✅ Market research and competitive analysis (project-setup)
- ✅ Technical feasibility and architecture analysis
- ✅ User research and requirements gathering
- ✅ Existing code analysis and pattern identification
- ✅ Technology stack evaluation and selection

**Analysis Outputs**:
- ✅ Project blueprint with comprehensive research findings
- ✅ Technical architecture recommendations
- ✅ User personas and requirements documentation
- ✅ Technology decisions with rationale

### **PHASE 3: PLANNING & STORY CREATION** ⏱️ ~30-45 minutes

**Enhanced Planning Process**:
- ✅ Create hyper-detailed stories with acceptance criteria
- ✅ Design technical specifications with API contracts
- ✅ Break down into granular, trackable tasks
- ✅ Establish verification criteria for each story
- ✅ Update `.augment/context/roadmap.md` with sprint plan

**Quality Gates**:
- ✅ All stories have clear acceptance criteria
- ✅ Technical specs include API design and database changes
- ✅ Task dependencies are clearly mapped
- ✅ CI/CD pipeline is green before proceeding

### **PHASE 4: IMPLEMENTATION** ⏱️ Variable (project-setup only)

**Intelligent Implementation**:
- ✅ Auto-select appropriate workflow based on task type
- ✅ Follow role-specific guidelines for each phase
- ✅ Implement with TDD when appropriate
- ✅ Use visual feedback loops for UI work
- ✅ Maintain continuous integration and testing

**Progress Tracking**:
- ✅ Update task states in real-time
- ✅ Document decisions in `.augment/context/decisions.md`
- ✅ Maintain green CI/CD pipeline throughout
- ✅ Verify each story against acceptance criteria

**Note**: For workflows other than project-setup, implementation happens in Phase 3.

## 🧠 Smart Context Management

### Context Strategy & Usage
```markdown
## Context Files Purpose:
- `.augment/context/mission.md` - Project vision, goals, constraints (ALWAYS read at phase start)
- `.augment/context/roadmap.md` - Current progress, sprint status, next steps
- `.augment/context/decisions.md` - Key architectural and business decisions

## When to Read Context:
- **Phase Start**: Always read mission.md for project alignment
- **Agent Handoff**: Read relevant context for continuity
- **Decision Making**: Check decisions.md for previous choices
- **Sprint Planning**: Read roadmap.md for current state

## When to Update Context:
- **After Research**: Update mission.md with new insights
- **After Decisions**: Document in decisions.md with rationale
- **Sprint Changes**: Update roadmap.md with progress
- **Major Milestones**: Refresh all context files
```

### Cascading Context Loading
```markdown
# Example: Phase 3 start (after research completed)
1. Load: .augment/context/mission.md (project vision - UPDATED with research)
2. Load: /docs/research/project-blueprint.md (research output - INPUT for this phase)
3. Load: .augment/workflows/project-setup/phase-3-planning.md (current workflow phase)
4. Load: .augment/agents/architect.md (role for current phase)
5. Skip: Individual research files (use synthesized project-blueprint.md instead)
```

### Context Optimization
- **Summarized Context**: Context files are executive summaries, not detailed docs
- **Research Artifacts**: Detailed research in `/docs/research/` used as phase inputs
- **Git Context Lineage**: Use commit history to understand evolution
- **Memory Persistence**: Use Agent Memories for session continuity
- **Conditional Loading**: Only load files relevant to current task

## 🚀 Advanced Features

### Multi-Agent Coordination
- **Product Manager Agent**: Product vision, requirements, and user research
- **Designer Agent**: UI/UX design, wireframes, and user experience
- **Architect Agent**: Technical decisions, architecture, and code analysis
- **Developer Agent**: Implementation with TDD, basic DevOps, and best practices
- **DevOps Agent**: Advanced infrastructure, containers, and cloud operations (conditional)
- **QA Agent**: Testing, validation, and quality assurance
- **Project Manager Agent**: Project orchestration, timeline management, and coordination

### Intelligent Workflow Selection
- **Auto-Detection**: Analyze task description to select optimal workflow
- **Context-Aware**: Consider project state and complexity
- **Adaptive**: Adjust workflow based on feedback and results

### Conditional DevOps Activation
The DevOps agent automatically activates when projects require advanced infrastructure:

#### ✅ **Activate DevOps for:**
- Docker containers or Kubernetes manifests
- Infrastructure as Code (Terraform, CloudFormation)
- Microservices architecture
- Multi-environment complexity (staging, testing, production)
- Advanced monitoring and alerting requirements
- Multi-cloud deployment strategies
- Performance optimization critical requirements

#### ❌ **Keep DevOps inactive for:**
- Vercel/Netlify deployments
- Basic GitHub Actions CI/CD
- Managed databases (Supabase, PlanetScale)
- Single environment projects
- MVP or prototype development

### Dynamic Rules Creation
Augment Develop Method creates project-specific rules during the research phase:

#### **Universal Rules (Never Change):**
- File organization standards
- Quality gates and commit conventions
- Task management protocols
- Basic code review requirements

#### **Project-Specific Rules (Created in Phase 1):**
- **Tech Stack Rules**: Framework-specific patterns and conventions
- **Project Conventions**: Naming, file structure, import organization
- **Quality Standards**: Performance, accessibility, security requirements
- **Development Workflow**: Branch strategy, PR process, deployment rules

#### **Rules Creation Process:**
1. **Phase 1 Step 6**: Architect analyzes project requirements
2. **Template Usage**: Uses `.augment/methodology/dynamic-rules.md` templates
3. **Rule Generation**: Creates project-tech-stack.md, project-conventions.md, project-quality.md
4. **Integration**: Updates main.md to reference new project-specific rules
5. **Validation**: Ensures rules align with chosen technology stack and project needs

### Enhanced Quality Assurance
- **Automated Testing**: TDD with comprehensive test coverage
- **Visual Validation**: Screenshot comparison for UI work
- **Performance Monitoring**: Automated performance testing
- **Security Scanning**: Integrated security checks

## 📋 Task Management Integration

Augment Develop Method leverages Augment Code's native task management:
- **Automatic Task Creation**: From story breakdown
- **Real-time Progress**: Task state updates during implementation
- **Dependency Tracking**: Automatic dependency resolution
- **Parallel Execution**: Independent tasks run simultaneously

## 🔧 Tool Integration

### Core Tools (Always Available)
- **Context7**: Official documentation consultation
- **Sequential Thinking**: Complex problem analysis
- **Web Search**: Market research and competitive analysis
- **Playwright**: E2E testing and visual validation
- **GitHub Actions**: Automated CI/CD

### Smart MCP Configuration
- **Auto-Detection**: Based on project stack and requirements
- **Contextual Suggestions**: Relevant MCPs for current work
- **Seamless Integration**: Automatic setup and configuration

## 📋 Templates and Documentation

### Available Templates
Augment Develop Method provides comprehensive templates for consistent documentation:

#### **Research & Planning Templates:**
- **Research Artifacts**: Market analysis, product definition, technical feasibility
- **Project Blueprint**: Master synthesis document from Phase 1
- **Hyper-Detailed Stories**: Complete story template with TDD specifications
- **Context Files**: Mission, roadmap, and decisions templates

#### **Implementation Templates:**
- **Verification Documents**: Story completion validation and testing results
- **Sprint Summaries**: Sprint completion reports with metrics and lessons learned
- **Dynamic Rules**: Project-specific rules and conventions

#### **Template Locations:**
- **Research Templates**: `.augment/templates/{existing-code-analysis.md, market-analysis.md, product-definition.md, design-research.md, technical-feasibility.md, business-viability.md, project-blueprint.md}`
- **Story Templates**: `.augment/templates/{story-template.md, ui-first-story-template.md, verification-template.md}`
- **Context Templates**: `.augment/templates/context-files.md`
- **Usage Guidelines**: Each template includes detailed usage instructions

### Documentation Standards
- **Consistency**: All documents follow standardized templates
- **Completeness**: Templates ensure no critical information is missed
- **Traceability**: Clear links between phases and deliverables
- **Maintainability**: Easy to update and keep current

## 🎯 Getting Started

### **For New Projects (Recommended Setup)**

#### **Step 1: Copy Template Structure**
```bash
# Copy the clean template (without project-specific content)
cp -r /path/to/cfad-augment-method/.augment-template .augment
cp /path/to/cfad-augment-method/methodology.md .
```

#### **Step 2: Prepare Project Input**
```bash
mkdir -p docs/project-input
# Add your project files:
# - idea.md (main concept)
# - inspiration/ (screenshots, examples)
# - requirements/ (detailed specs)
# - assets/ (mockups, designs)
```

#### **Step 3: Start Augment Code Session**
```
"Apply this methodology: ./methodology.md for building [your project description]

Repository: https://github.com/username/project-name.git"
```

### **What Happens During Setup**
- **Phase 1**: Agent creates `.augment/context/` files and populates `.augment/rules/`
- **Agent reads**: ALL files in `docs/project-input/` for project understanding
- **Agent creates**: Project-specific rules, context, and dynamic guidelines
- **Agent sets up**: Repository connection, CI/CD, and development environment

### **Legacy Setup (Not Recommended)**
1. **Initialize Project**: Place `methodology.md` in your project root
2. **Start Session**: `"Apply Augment Develop Method: ./methodology.md"`
3. **Follow Guidance**: Agent will create `.augment/` structure automatically
4. **Trust the Process**: Let the methodology guide the implementation

---

**Next**: The agent will automatically create the complete `.augment/` structure and guide you through the enhanced multi-phase process with UI-first approach.

**For detailed workflow information**, see the specific files in `.augment/workflows/` after initialization.
