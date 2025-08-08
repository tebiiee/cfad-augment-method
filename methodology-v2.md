# CFAD 2.0: Context-First Agentic Development
## Enhanced Modular Methodology for Augment Code

### 🚀 What's New in CFAD 2.0

**CFAD 2.0** evolves the proven methodology with **4-phase UI-first approach**, modular architecture, specialized agent roles, and intelligent workflow selection inspired by Claude Code Agents and Agent OS best practices.

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
  /project-input/               # User inputs (ideas, notes, screenshots, etc.)
  /archived/                    # Archived project inputs by timestamp
    /2024-01-15-143022/         # Example: archived inputs from specific session
  /research/                    # Phase 1: Research artifacts
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
  /current-sprint/              # Symlink or reference to active sprint
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

## 🎯 How to Use CFAD 2.0

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

| Work Type | Workflow File | Agent Flow | Description |
|-----------|---------------|------------|-------------|
| **New Project** | `project-setup/` | PM → Designer → Architect → Developer → QA | Complete project setup with 4-phase UI-first approach |
| **New Features** | `new-feature/` | PM → Designer → Architect → Developer → QA | Add functionality with 3-phase UI-first approach |
| **Bug Fixes** | `bug-fix/` | PM → Developer → QA | Investigation and resolution with 2-phase systematic approach |
| **Code Optimization** | `refactor/` | PM → Architect → Developer → QA | Safe code improvement with 3-phase approach |
| **UI/UX Work** | `ui-work/` | Designer → Developer → QA | Interface implementation with 3-phase design-first approach |

**Note**: DevOps agent activates automatically for complex projects requiring advanced infrastructure (Docker, Kubernetes, IaC).

## 🔄 Enhanced Multi-Phase Process

### **PHASE 1: INTELLIGENT ANALYSIS** ⏱️ ~10-15 minutes

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

### **PHASE 2: SPEC-DRIVEN PLANNING** ⏱️ ~20-30 minutes

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

### **PHASE 3: WORKFLOW-DRIVEN IMPLEMENTATION** ⏱️ Variable

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
# Example: Phase 2 start (after research)
1. Load: .augment/context/mission.md (project vision - UPDATED with research)
2. Load: /docs/research/product-definition.md (research output - INPUT for this phase)
3. Load: .augment/workflows/project-setup/phase-2-research.md (current workflow phase)
4. Load: .augment/agents/architect.md (role for current phase)
5. Skip: Individual research files (use synthesized product-definition.md instead)
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
CFAD 2.0 creates project-specific rules during Phase 1 research:

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

CFAD 2.0 leverages Augment Code's native task management:
- **Automatic Task Creation**: From story breakdown
- **Real-time Progress**: Task state updates during implementation
- **Dependency Tracking**: Automatic dependency resolution
- **Parallel Execution**: Independent tasks run simultaneously

## 🔧 Tool Integration

### Core Tools (Always Available)
- **Context7**: Official documentation consultation
- **Sequential Thinking**: Complex problem analysis
- **Playwright**: E2E testing and visual validation
- **GitHub Actions**: Automated CI/CD

### Smart MCP Configuration
- **Auto-Detection**: Based on project stack and requirements
- **Contextual Suggestions**: Relevant MCPs for current work
- **Seamless Integration**: Automatic setup and configuration

## 📋 Templates and Documentation

### Available Templates
CFAD 2.0 provides comprehensive templates for consistent documentation:

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
- **All Templates**: `.augment/templates/research-artifacts.md`
- **Context Templates**: `.augment/templates/context-files.md`
- **Usage Guidelines**: Each template includes detailed usage instructions

### Documentation Standards
- **Consistency**: All documents follow standardized templates
- **Completeness**: Templates ensure no critical information is missed
- **Traceability**: Clear links between phases and deliverables
- **Maintainability**: Easy to update and keep current

## 🎯 Getting Started

1. **Initialize Project**: Place `methodology-v2.md` in your project root
2. **Start Session**: `"Apply CFAD 2.0 methodology: ./methodology-v2.md"`
3. **Follow Guidance**: Agent will create `.augment/` structure automatically
4. **Trust the Process**: Let the methodology guide the implementation

---

**Next**: The agent will automatically create the complete `.augment/` structure and guide you through the enhanced multi-phase process with UI-first approach.

**For detailed workflow information**, see the specific files in `.augment/workflows/` after initialization.
