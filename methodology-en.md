# Development Methodology for AI Agents in Augment Code

## 1. Strict Execution Protocol

### 1.1. STEP 1: MANDATORY Initial Analysis

**ALWAYS execute in this order**:

1. **Consult `/docs/project-input/`** - Read ALL files
2. **Detect project state**:
   - Does `/docs/current-sprint/` exist? → Project in progress
   - Code exists without methodology? → Existing project
   - Nothing exists? → New project
3. **Create task list** immediately
4. **DO NOT proceed** until completing analysis

### 1.2. STANDARD Directory Structure

**MANDATORY in ALL projects**:
```
/docs/
  /project-input/        # User input (don't touch)
  /processed-input/      # Processed inputs by sprint
    /sprint-01/          # Processed inputs from sprint 1
    /sprint-02/          # Processed inputs from sprint 2
  /sprint-01/            # First completed sprint
  /sprint-02/            # Second completed sprint
  /current-sprint/       # Current sprint in progress
    /planning/           # Planning documents
    /stories/            # Hyper-detailed stories
    /verification/       # Story verifications
    /implementation/     # Code and technical documentation
  /archive/              # Old sprints
/.augment/rules/         # Augment Code rules
```

### 1.3. STRICT Transition Rules

**NEVER advance to next phase without**:
- ✅ All current phase documents complete
- ✅ Documents organized in correct directories
- ✅ Task list updated with correct states
- ✅ Explicit user approval to advance

### 1.4. STANDARD Nomenclature

**Documents (ALWAYS use these names)**:
- `project_context.md` - Project analysis and context
- `planning_doc.md` - Requirements + architecture + stories
- `story-[ID]-[short-name].md` - Hyper-detailed story
- `verify-[ID]-[short-name].md` - Story verification
- `sprint-summary.md` - Completed sprint summary

## 2. Adaptive Flows by Project Type

### 2.1. New Project Flow
**Detection**: No previous methodological documents
**Process**: Complete analysis → Planning → Implementation → Deployment

### 2.2. Project in Progress Flow
**Detection**: Pending hyper-detailed stories
**Process**: Continue with next story → Implementation → QA

### 2.3. New Sprint Flow
**Detection**: All stories complete
**Process**: Change analysis → New stories → Implementation

### 2.4. Flow by Complexity
**Simple**: Skip extensive documentation, combined roles, direct to implementation
**Complex**: Complete process with all roles and detailed documentation

### 2.5. Flow by Work Type
**New feature**: Standard process
**Refactor**: More existing code analysis, less design
**Bugfix**: Accelerated process, direct to implementation

## 3. Fluid Role System

### 3.1. Combinable Roles
Roles can be naturally combined:

- **Code Analyst + Rules Generator**: Analysis and rules in one session
- **Requirements + Architecture**: For simple projects
- **Developer + QA**: For minor changes

### 3.2. Core Roles
**Code Analyst**: Exhaustive analysis of existing code, patterns, dependencies
**Rules Generator**: Create/update `.augment/rules/` dynamically
**Planner**: Requirements, architecture, stories (combined roles)
**Developer**: Implementation based on hyper-detailed stories
**QA**: Validation against acceptance criteria

### 3.3. Consolidated Artifacts

- `project_context.md`: Overview + combined code analysis
- `planning_doc.md`: Requirements + architecture + stories
- `implementation_guide.md`: Consolidated hyper-detailed stories
- `.augment/rules/`: Project-specific dynamic rules

## 4. Practical Context Management with Augment Code Tools

### 4.1. Retrieval Tools

**`codebase-retrieval`**: To understand current code, find existing patterns
- Use at start of each work session
- Ask for specific symbols before editing
- Request detailed information about classes, methods, properties involved

**`git-commit-retrieval`**: To see how similar changes were made before
- Search for similar implementations in history
- Understand project change patterns
- Learn from previous technical decisions

### 4.2. Editing Tools

**`str-replace-editor`**: ALWAYS do retrieval first, edit conservatively
- Never edit without understanding complete context
- Respect existing patterns and conventions
- Make incremental and verifiable changes

### 4.3. Context7 for Official Documentation

**ALWAYS available to consult official documentation**

**Use in Phase 1 - Analysis**:
- Consult documentation of detected tech stack
- Verify framework best practices
- Understand patterns recommended by official documentation

**Use in Phase 2 - Planning**:
- Consult official architecture guides
- Verify available APIs and methods
- Confirm recommended design patterns

**Use in Phase 3 - Error Resolution**:
- Consult documentation when build errors occur
- Verify correct API syntax
- Search for official solutions to common problems

**Useful query examples**:
- "Next.js App Router best practices"
- "Tailwind CSS responsive design patterns"
- "Convex database schema design"
- "Vercel deployment configuration"

### 4.4. Sequential Thinking for Complex Analysis

**ALWAYS available for structured thinking and complex problem solving**

**When to use Sequential Thinking**:
- **Important architectural decisions** (stack, patterns, structure)
- **Complex existing project analysis** (legacy code, unclear architecture)
- **Complex error debugging** (multiple systems, dependencies)
- **Complex feature planning** (multiple interdependent stories)
- **Conflict resolution** (contradictory requirements, technical limitations)

**Use in Phase 1 - Complex Analysis**:
- Analyze complex existing architecture
- Decide tech stack when unclear
- Evaluate multiple MCP options
- Plan legacy code migration

**Use in Phase 2 - Architectural Planning**:
- Design architecture for complex systems
- Break down complex features into stories
- Resolve dependencies between components
- Evaluate design trade-offs

**Use in Phase 3 - Problem Resolution**:
- Multi-system error debugging
- Complex performance problems
- CI/CD integration conflicts
- Workflow optimization

**Sequential Thinking Process**:
1. **Define the problem** clearly
2. **Break down** into sub-problems
3. **Analyze options** for each sub-problem
4. **Evaluate trade-offs** and dependencies
5. **Select optimal approach**
6. **Document reasoning** for transparency

### 4.5. Integrated Task Management

**From the start**: Use task management as integral part of the process
- Create tasks for each methodological phase
- Update states in real time
- Maintain progress visibility for user

### 4.6. Intelligent MCPs by Context

**Core MCPs (always available)**:
- File system, Git, Memory, Time
- **Context7**: Official documentation consultation
- **Sequential Thinking**: Complex problem structured analysis
- PDF tools, Calculator, Web scraping

**MCPs by Tech Stack** (detect and suggest automatically):
- **Convex**: Search for Convex MCP if project uses it
- **Supabase**: Supabase MCP for projects requiring it
- **PostgreSQL/MySQL**: Database MCPs according to detected stack
- **Redis**: If cache/state usage detected

**Mandatory QA MCPs** (according to complexity):
- **GitHub Actions MCP**: For automatic CI/CD (ALWAYS if GitHub repository)
- **Playwright**: For E2E testing (ALWAYS available in Augment Code)
- **Testing tools**: According to detected framework

**Intelligent MCP Process**:
1. **Detect stack** in `/docs/project-input/` or existing code
2. **Automatic MCPs** (without asking permission):
   - GitHub Actions (if repository exists)
   - Playwright (always available)
   - Context7 (always available for documentation)
   - Sequential Thinking (always available for complex analysis)
3. **Suggested MCPs** (request approval):
   - Database MCPs according to detected stack
   - Cloud MCPs according to deployment target
   - Integration MCPs according to mentioned APIs
4. **Automatically configure** approved MCPs

### 4.7. Criteria for Using Sequential Thinking

**ALWAYS use when**:
- **Multiple valid options** (stack, architecture, patterns)
- **Complex dependencies** between components/systems
- **Significant trade-offs** in technical decisions
- **Errors affecting multiple systems**
- **Contradictory or ambiguous** requirements

**DO NOT use for**:
- **Simple and direct tasks** (implement clear story)
- **Already defined processes** in methodology
- **Obvious decisions** (use TypeScript with Next.js)
- **Simple errors** (typos, linting)

## 5. Project Methodology: CFAD (Context-First Agentic Development)

Adaptive methodology that integrates proactive context management with flexible flows according to project type.

### 5.1. Phases with STRICT Completeness Criteria

## **PHASE 1: ANALYSIS AND CONTEXT**

### Start Criteria:
- ✅ Task list created
- ✅ `/docs/project-input/` completely consulted

### MANDATORY Tasks:
1. **Search for GitHub URL** in `/docs/project-input/` (for automatic commits)
2. **Configure GitHub Actions MCP** automatically if repository exists
3. **Detect existing workflows** in `.github/workflows/`
4. **Consult Context7** for official documentation of detected stack
5. **Use Sequential Thinking** if analysis is complex (unclear architecture, multiple options)
6. Existing code analysis (if applicable)
7. Tech stack detection
8. Generate `.augment/rules/`
9. Contextual MCP configuration

### Completeness Criteria:
- ✅ `project_context.md` created in `/docs/current-sprint/planning/`
- ✅ `.augment/rules/` configured
- ✅ **GitHub Actions MCP configured** (if repository exists)
- ✅ **CI/CD workflows analyzed** and documented
- ✅ Contextual MCPs implemented
- ✅ Task list updated
- ✅ **AUTOMATIC COMMIT**: "feat: complete phase 1 - project analysis and setup"
- ✅ **GREEN CI/CD PIPELINE** ✅ (mandatory before advancing)
- ✅ **EXPLICIT USER APPROVAL**

### **DO NOT PROCEED TO PHASE 2 WITHOUT COMPLETING ALL ABOVE**

---

## **PHASE 2: COMPLETE PLANNING**

### Start Criteria:
- ✅ Phase 1 100% complete
- ✅ Explicit approval received

### MANDATORY Tasks:
1. **Consult Context7** for architecture guides and best practices
2. **Use Sequential Thinking** for complex architectural decisions
3. Define functional and non-functional requirements
4. Design technical architecture
5. **Verify APIs and patterns** with official documentation via Context7
6. **Apply Sequential Thinking** to break down complex features into stories
7. Create ALL hyper-detailed stories
8. Configure QA tools
9. Organize files in standard structure

### Completeness Criteria:
- ✅ `planning_doc.md` complete in `/docs/current-sprint/planning/`
- ✅ ALL stories in `/docs/current-sprint/stories/`
- ✅ **CI/CD workflows configured** according to tech stack
- ✅ **Vercel-GitHub integration verified**
- ✅ QA tools configured (Playwright + GitHub Actions)
- ✅ Directory structure organized
- ✅ **MOVE INPUTS**: `/docs/project-input/` → `/docs/processed-input/sprint-[X]/`
- ✅ **AUTOMATIC COMMIT**: "feat: complete phase 2 - planning and stories for sprint [X]"
- ✅ **GREEN CI/CD PIPELINE** ✅ (mandatory before advancing)
- ✅ **EXPLICIT USER APPROVAL**

### **DO NOT PROCEED TO PHASE 3 WITHOUT COMPLETING ALL ABOVE**

---

## **PHASE 3: ITERATIVE IMPLEMENTATION**

### Start Criteria:
- ✅ Phase 2 100% complete
- ✅ All hyper-detailed stories created
- ✅ Explicit approval received

### Development Protocol by Complexity:

**SIMPLE PROJECTS** (1-5 stories):
- Develop 2-3 stories in parallel
- Integrated QA by batch
- Single branch: `main` or `develop`

**COMPLEX PROJECTS** (6+ stories):
- Develop 1 story at a time
- Individual QA per story
- Branch per sprint: `sprint-2`, `sprint-3`, etc.

### MANDATORY Cycle per Story:
1. **Developer**: Implement story
2. **QA**: Verify acceptance criteria
3. **Create**: `verify-[ID]-[name].md`
4. **Update**: Task list with COMPLETE state
5. **Only then**: Proceed to next story

### Sprint Completeness Criteria:
- ✅ ALL stories implemented
- ✅ ALL verifications created
- ✅ **Tests passing** (unit + integration + **E2E with Playwright**)
- ✅ **Green CI/CD pipeline** in GitHub Actions ✅
- ✅ **Successful Vercel deployment** (preview and/or production)
- ✅ **Post-deployment smoke tests** passing
- ✅ Technical documentation updated
- ✅ **COMMIT PER STORY**: "feat: implement story [ID] - [name]"
- ✅ **FINAL COMMIT**: "feat: complete sprint [X] - all stories implemented"
- ✅ **FINAL GREEN PIPELINE** ✅ (mandatory before finishing)
- ✅ **EXPLICIT USER APPROVAL**

### Branch Management:
**Sprint 1**: Work on `main` or `develop`
**Sprint 2+**:
1. Create branch `sprint-[number]`
2. Develop in the branch
3. PR when finishing sprint
4. Merge only with approval

### **DO NOT PROCEED TO NEXT SPRINT WITHOUT COMPLETING ALL ABOVE**

---

## **MINI-ITERATIONS PROTOCOL WITHIN PHASES**

### Mini-Iterations in Phase 1:
**If user does NOT approve `project_context.md` or rules**:
1. **Request specific feedback** from user
2. **Adjust documents** according to feedback
3. **Update** `project_context.md` and/or `.augment/rules/`
4. **Request approval again**
5. **Repeat until obtaining approval**

### Mini-Iterations in Phase 2:
**If user does NOT approve `planning_doc.md` or stories**:
1. **Request specific feedback** from user
2. **Adjust planning** according to feedback
3. **Modify stories** if necessary
4. **Update documents** in `/docs/current-sprint/`
5. **Request approval again**
6. **Repeat until obtaining approval**

### Mini-Iteration Rules:
- ✅ **Maximum 3 iterations** per phase (avoid infinite loops)
- ✅ **Specific feedback**: User must indicate what to change
- ✅ **Document changes**: Record modifications in task list
- ✅ **Maintain structure**: Don't change file organization

---

## **SPRINT TRANSITION PROTOCOL**

### When Finishing a Sprint:
1. **Move** `/docs/current-sprint/` → `/docs/sprint-[number]/`
2. **Create** `sprint-summary.md` with achievement summary
3. **Create** new `/docs/current-sprint/` for next sprint
4. **Update** task list with new sprint
5. **Create branch** `sprint-[number]` if complex project
6. **FINAL COMMIT**: "feat: finalize sprint [X] - ready for next sprint"
7. **Request approval** to start next sprint

### When Starting New Sprint:
1. **Consult** `/docs/project-input/` for new requirements
2. **Execute Phase 1** (change analysis)
3. **In Phase 2**: Move processed inputs to `/docs/processed-input/sprint-[X]/`
4. **Execute Phase 2** (new sprint planning)
5. **Follow strict protocol** like initial sprint

### Processed Input Management:
**IMPORTANT**: When finishing Phase 1 of any sprint:
- **Move** all content from `/docs/project-input/`
- **Destination**: `/docs/processed-input/sprint-[number]/`
- **Result**: `/docs/project-input/` remains clean for future inputs
- **Benefit**: Avoids confusion in future sprints with new agents

### Special Cases:
**Urgent bugfix**: Create branch `hotfix-[description]`, follow simplified Phase 3
**Refactor**: Follow Phase 1 and 3, skip Phase 2 if no new features
**Minor feature**: Evaluate if requires complete sprint or can be added to current

---

## 6. Hyper-Detailed Story Management

### 6.1. File Structure
**One story = One file**: `/stories/story-[ID]-[name].md`
**One verification = One file**: `/verification/verify-[ID]-[name].md`

### 6.2. Hyper-Detailed Story Template

```markdown
### Story: [Title]

**ID:** STORY-[number]
**Status:** [PENDING/IN_PROGRESS/COMPLETED]

**Description:** [What should be built - concise but complete]

**Acceptance Criteria:**
- [Criterion 1: "User MUST be able to [action] to [benefit]"]
- [Criterion 2...]

**Technical Context:**
- **Files:** `[specific paths to create/modify]`
- **Dependencies:** [Components, hooks, services to use]
- **Patterns:** [Specific design patterns]

**API (if applicable):**
- **Endpoint:** `[method] [path]`
- **Request/Response:** [Data structure]

**Deliverable:** Code + tests + JSDoc documentation
```

### 6.3. Verification Template (Simplified)

```markdown
### Verification: [Story Title]

**ID:** STORY-[number]
**Date:** [YYYY-MM-DD]
**Status:** [COMPLETED/FAILED]

**Implementation Summary:**
[2-3 lines describing what was implemented]

**Modified Files:**
- `[list of actually modified files]`

**Executed Tests:**
- [✓/✗] Unit tests
- [✓/✗] Integration tests
- [✓/✗] Acceptance criteria

**Notes:** [Any important observations]
```

## 7. Intelligent Tech Stack Selection

### 7.1. Selection Process
1. **Review `/docs/project-input/`**: Look for user-specified stack
2. **If not specified**: Analyze requirements and suggest optimal stack
3. **Consider factors**:
   - Application type (web, mobile, desktop)
   - Project complexity
   - Performance requirements
   - Team experience
   - Development time

### 7.2. Contextual Suggestions
**Complex Web App**: Next.js + TypeScript + Tailwind + Shadcn + Convex
**Simple Web App**: Vite + React + TypeScript + Tailwind
**Mobile App**: React Native + Expo or Flutter (depending on context)
**Desktop App**: Electron + React or Tauri + React
**API/Backend**: Node.js + Express or Python + FastAPI

### 7.3. User Validation
- Present suggested stack with justification
- Request approval or modifications
- Document decisions in `project_context.md`

## 8. Integrated Task Management

### 8.1. Use from Start
- **First action**: Create task list after consulting `/docs/project-input/`
- **Structure by phases**: Specific tasks for each methodological phase
- **Real-time states**: NOT_STARTED → IN_PROGRESS → COMPLETE
- **Continuous visibility**: User sees progress at all times

### 8.2. Suggested Task Structure
**Phase 1**: Context analysis and rule generation
**Phase 2**: Integrated planning (requirements + architecture + stories)
**Phase 3**: Implementation (one task per hyper-detailed story)

### 8.3. Role Coordination

- Each role updates its corresponding tasks
- Smooth transitions between tasks
- Contextual feedback integrated in tasks

## 9. Integrated Automated QA

### 9.1. QA Tools by Complexity

**Simple Projects**:
- Basic unit testing
- Automatic linting

**Complex Projects**:
- **GitHub Actions**: Automatic validation on each commit
- **Playwright**: E2E tests for critical flows
- **Integration testing**: APIs and components
- **Code analysis**: SonarQube or similar

### 9.2. Flow Integration

**During Development**:
- Unit tests in each story
- Automatic linting on each save

**Pre-Deployment**:
- Automatic CI/CD pipeline
- E2E tests in staging
- Performance validation

**Post-Deployment**:
- Error monitoring
- Performance metrics
- Automatic alerts

### 9.3. Playwright Integration (MANDATORY)

**Playwright is globally available in Augment Code**

**When to use Playwright**:
- **Web projects** with user interface
- **Critical flows** requiring E2E validation
- **Complex forms** or multi-step interactions

**Workflow Integration**:

**Phase 2 - Planning**:
- Identify **critical flows** for E2E tests
- Document **Playwright scenarios** in `planning_doc.md`
- Create **E2E test skeletons** per story

**Phase 3 - Implementation**:
- **Per story**: Implement corresponding E2E tests
- **Execute Playwright** before marking story as complete
- **Include in verification**: E2E tests passing

**E2E Test Structure**:
```
/tests/
  /e2e/
    /[feature-name]/
      - [story-id]-[test-name].spec.ts
```

### 9.4. GitHub Actions Integration (MANDATORY if GitHub repository)

**Automatic GitHub MCP Configuration**:
- **Detect GitHub repository** in user inputs
- **Configure GitHub Actions MCP** automatically
- **Analyze existing workflows** in `.github/workflows/`
- **Document current CI/CD** in `project_context.md`

**Intelligent CI/CD Strategy**:

**Phase 1 - Detection and Analysis**:
- Detect existing workflows
- Analyze current CI/CD configuration
- Identify Vercel connection
- Document state in `project_context.md`

**Phase 2 - Configuration and Optimization**:
- Create/update workflows according to detected tech stack
- Configure workflow for: testing, linting, Playwright E2E
- Integrate with Vercel for preview deployments
- Define CI/CD strategy in `planning_doc.md`

**Phase 3 - Continuous Monitoring and Intelligent Blocking**:
- **Execute workflows** automatically after each commit
- **Block progress** if workflow fails
- **3 automatic attempts** for re-execution for temporary problems
- **Log analysis** and automatic fix suggestions
- **Only advance** when CI/CD is green ✅

**Error Types and Automatic Actions**:
- **Linting/Format**: Auto-fix and new commit
- **Unit tests**: Report specific errors and block
- **Build errors**: Analyze logs + **consult Context7** for official solutions
- **API errors**: **Consult Context7** to verify correct syntax
- **Complex errors**: **Use Sequential Thinking** for structured debugging
- **Multi-system problems**: **Sequential Thinking** to analyze dependencies
- **Playwright E2E**: Execute against Vercel preview URL
- **Deployment**: Verify configuration + **consult Context7** for Vercel docs

**Dual Integration with Playwright**:
- **Local**: Playwright during development (immediate verification)
- **CI/CD**: Playwright in GitHub Actions against Vercel preview
- **Staging**: Complete E2E tests before merge
- **Production**: Smoke tests post-deployment

### 9.5. General Automatic Configuration

1. **Detect project complexity**
2. **Configure GitHub Actions MCP** if repository exists
3. **Configure Playwright** automatically for web projects
4. **Suggest appropriate additional QA tools**
5. **Request user approval**
6. **Automatically configure** MCPs and pipelines
7. **Document setup** in `project_context.md`

---

## **MANDATORY VERIFICATION CHECKLIST**

### Before Advancing from Phase 1 to Phase 2:
- [ ] `/docs/project-input/` completely consulted
- [ ] GitHub URL detected (if available)
- [ ] **GitHub Actions MCP configured** automatically
- [ ] **Existing workflows analyzed** and documented
- [ ] **Context7 consulted** for detected stack documentation
- [ ] **Sequential Thinking applied** if analysis is complex
- [ ] `project_context.md` created in `/docs/current-sprint/planning/`
- [ ] `.augment/rules/` configured
- [ ] Contextual MCPs implemented
- [ ] Task list updated
- [ ] **AUTOMATIC COMMIT**: "feat: complete phase 1 - project analysis and setup"
- [ ] **GREEN CI/CD PIPELINE** ✅ (mandatory)
- [ ] **EXPLICIT USER APPROVAL received** (with possible mini-iterations)

### Before Advancing from Phase 2 to Phase 3:
- [ ] **Context7 consulted** for architecture guides and APIs
- [ ] **Sequential Thinking applied** for complex architectural decisions
- [ ] `planning_doc.md` complete in `/docs/current-sprint/planning/`
- [ ] ALL stories created in `/docs/current-sprint/stories/`
- [ ] **Sequential Thinking used** to break down complex features
- [ ] **CI/CD workflows configured** according to tech stack
- [ ] **Vercel-GitHub integration verified**
- [ ] QA tools configured (Playwright + GitHub Actions)
- [ ] Directory structure organized
- [ ] **INPUTS MOVED**: `/docs/project-input/` → `/docs/processed-input/sprint-[X]/`
- [ ] **AUTOMATIC COMMIT**: "feat: complete phase 2 - planning and stories for sprint [X]"
- [ ] **GREEN CI/CD PIPELINE** ✅ (mandatory)
- [ ] **EXPLICIT USER APPROVAL received** (with possible mini-iterations)

### Before Finishing a Sprint:
- [ ] ALL stories implemented
- [ ] ALL verifications in `/docs/current-sprint/verification/`
- [ ] **Tests passing** (unit + integration + **E2E with Playwright**)
- [ ] **Green CI/CD pipeline** in GitHub Actions ✅
- [ ] **Successful Vercel deployment** (preview and/or production)
- [ ] **Post-deployment smoke tests** passing
- [ ] Technical documentation updated
- [ ] **COMMITS PER STORY**: "feat: implement story [ID] - [name]"
- [ ] **FINAL COMMIT**: "feat: complete sprint [X] - all stories implemented"
- [ ] **FINAL GREEN PIPELINE** ✅ (mandatory)
- [ ] **EXPLICIT USER APPROVAL received**

### Before Starting New Sprint:
- [ ] Previous sprint moved to `/docs/sprint-[number]/`
- [ ] `sprint-summary.md` created
- [ ] New `/docs/current-sprint/` created
- [ ] Branch `sprint-[number]` created (if applicable)
- [ ] **COMMIT**: "feat: finalize sprint [X] - ready for next sprint"
- [ ] **EXPLICIT USER APPROVAL received**

---

**GOLDEN RULE: NEVER advance without completing ALL checkboxes of the current phase. This methodology guarantees consistency, quality and traceability in all projects.**
