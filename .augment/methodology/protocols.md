# CFAD 2.0: Methodology Protocols

## 🎯 Purpose
Detailed protocols that support workflows with specific procedures for tools, quality gates, task management, and completion criteria.

---

## 🔧 Augment Code Tools Integration

### Core Tools (Always Available)
- **Context7**: Official documentation consultation
- **Sequential Thinking**: Complex problem structured analysis  
- **Codebase Retrieval**: Understanding existing code patterns
- **Git Commit Retrieval**: Learning from project history
- **Task Management**: Native Augment Code task tracking

### Tool Usage by Phase

#### **Phase 1: Research**
```markdown
## Required Tools:
- **Sequential Thinking**: For complex market/technical analysis
- **Web Search**: For competitive research and market analysis
- **Context7**: For tech stack documentation and best practices
- **Codebase Retrieval**: For existing code analysis
- **Git Commit Retrieval**: For project history understanding

## Tool Usage Protocol:
1. **Start each research step** with Sequential Thinking if complex
2. **Use Web Search** for market and competitive research
3. **Consult Context7** for technical documentation
4. **Use Codebase Retrieval** before analyzing existing code
5. **Check Git history** with Git Commit Retrieval for context
```

#### **Phase 2: Architecture & Planning**
```markdown
## Required Tools:
- **Sequential Thinking**: For architectural decisions and trade-offs
- **Context7**: For framework architecture guides
- **Codebase Retrieval**: For understanding existing patterns
- **Git Commit Retrieval**: For similar architectural decisions

## Tool Usage Protocol:
1. **Use Sequential Thinking** for complex architectural decisions
2. **Consult Context7** for official architecture patterns
3. **Retrieve existing code** patterns before designing new ones
4. **Check commit history** for previous architectural decisions
```

#### **Phase 3: Implementation**
```markdown
## Required Tools:
- **Codebase Retrieval**: Before editing any code
- **Context7**: For API documentation and implementation guides
- **Git Commit Retrieval**: For similar implementation patterns
- **Playwright**: For E2E testing

## Tool Usage Protocol:
1. **Always use Codebase Retrieval** before editing code
2. **Consult Context7** for API documentation
3. **Check Git history** for similar implementations
4. **Use Playwright** for testing user flows
```

---

## 📋 Task Management Protocol

### Task Creation Strategy
```markdown
## Task Granularity:
- **One task per research type** (market, product, design, technical, business)
- **One task per major deliverable** (document, commit, approval)
- **One task per user story** (in implementation phase)
- **One task per quality gate** (approval, CI/CD check)

## Task Naming Convention:
- Research: "Research: [Type] - [Brief Description]"
- Documentation: "Document: [Artifact Name]"
- Development: "Implement: Story [ID] - [Name]"
- Quality: "QA: [Validation Type]"
- Approval: "Approval: [Phase/Deliverable]"
```

### Task State Management
```markdown
## Task States:
- **NOT_STARTED**: Task identified but not begun
- **IN_PROGRESS**: Currently working on task
- **COMPLETE**: Task finished and deliverable ready
- **CANCELLED**: Task no longer relevant

## State Transition Protocol:
1. **Create tasks** at start of each phase
2. **Update to IN_PROGRESS** when starting work
3. **Update to COMPLETE** when deliverable is ready
4. **Batch updates** when transitioning between agents
```

### Agent Task Handoffs
```markdown
## Task Handoff Protocol:
1. **Complete current agent tasks** before handoff
2. **Update task states** to COMPLETE
3. **Create new tasks** for next agent
4. **Document handoff** in task descriptions
5. **Next agent updates** their tasks to IN_PROGRESS
```

---

## ✅ Quality Gates & Completion Criteria

### Phase Completion Requirements
```markdown
## Phase 1: Research Completion
- ✅ All research artifacts created and committed
- ✅ Context files updated with research insights
- ✅ Project-specific rules defined
- ✅ Git repository properly configured
- ✅ All research tasks marked COMPLETE
- ✅ User approval for research findings

## Phase 2: Architecture Completion  
- ✅ Technical architecture documented
- ✅ All user stories created with acceptance criteria
- ✅ Development environment configured
- ✅ CI/CD pipeline green
- ✅ All planning tasks marked COMPLETE
- ✅ User approval for architecture and stories

## Phase 3: Implementation Completion
- ✅ All user stories implemented
- ✅ All tests passing (unit, integration, E2E)
- ✅ CI/CD pipeline green
- ✅ Documentation updated
- ✅ All implementation tasks marked COMPLETE
- ✅ User approval for final deliverable
```

### Quality Gate Enforcement
```markdown
## Before Phase Transition:
1. **Verify all completion criteria** are met
2. **Run automated checks** (tests, linting, build)
3. **Request user approval** explicitly
4. **Document any exceptions** or deviations
5. **Only proceed** after explicit approval

## If Quality Gate Fails:
1. **Identify specific issues** that need resolution
2. **Create tasks** to address issues
3. **Fix issues** and re-run checks
4. **Request approval** again
5. **Maximum 3 iterations** per phase
```

---

## 🔄 Commit Strategy & Git Workflow

### Commit Convention
```markdown
## Commit Message Format:
[type]: [description]

## Types:
- **docs**: Documentation and research artifacts
- **feat**: New features and functionality  
- **fix**: Bug fixes and corrections
- **refactor**: Code improvements without feature changes
- **test**: Adding or updating tests
- **ci**: CI/CD configuration changes
- **chore**: Maintenance tasks

## Examples:
- "docs: add market research and competitive analysis"
- "docs: create technical feasibility assessment"
- "feat: implement user authentication system"
- "docs: update context with research findings"
```

### Commit Frequency
```markdown
## Research Phase Commits:
- **One commit per research artifact** completed
- **One commit for context updates** after research synthesis
- **One commit for rules creation/updates**

## Development Phase Commits:
- **One commit per user story** implemented
- **One commit per major feature** completed
- **One commit for documentation** updates

## Commit Timing:
- **Immediately after** completing each deliverable
- **Before requesting** user approval
- **After user approval** for phase completion
```

### Branch Strategy
```markdown
## Branch Management:
- **main/develop**: Primary development branch
- **feature/[story-id]**: Individual feature branches (if complex)
- **research/[phase]**: Research branches (if needed)

## Branch Protocol:
1. **Create branch** for complex features
2. **Work in branch** until feature complete
3. **Merge to main** after approval
4. **Delete feature branch** after merge
```

---

## 🔄 Mini-Iteration Protocol

### When Mini-Iterations Trigger
```markdown
## Triggers:
- **User rejects** phase deliverable
- **Quality gate fails** and requires rework
- **Feedback indicates** significant changes needed
- **Technical issues** prevent completion

## Mini-Iteration Process:
1. **Request specific feedback** from user
2. **Identify exact changes** needed
3. **Create tasks** for required changes
4. **Implement changes** efficiently
5. **Re-submit for approval**
6. **Maximum 3 iterations** per phase
```

### Mini-Iteration Management
```markdown
## Iteration Tracking:
- **Document iteration number** in task descriptions
- **Track changes made** in each iteration
- **Maintain change log** for transparency
- **Escalate to user** if 3 iterations exceeded

## Iteration Quality:
- **Focus on specific feedback** only
- **Don't over-engineer** solutions
- **Maintain existing quality** standards
- **Document rationale** for changes
```

---

## 📊 Progress Tracking & Reporting

### Progress Metrics
```markdown
## Phase Progress:
- **Tasks Completed**: X/Y tasks complete
- **Quality Gates**: Passed/Failed status
- **User Approvals**: Pending/Approved status
- **Commit History**: Number of commits per phase

## Agent Performance:
- **Task Completion Rate**: Tasks completed per agent
- **Quality Score**: Quality gates passed
- **Handoff Efficiency**: Smooth agent transitions
```

### Status Reporting
```markdown
## Regular Updates:
- **Task status updates** in real-time
- **Phase progress reports** at major milestones
- **Issue escalation** when blockers occur
- **User communication** for approvals needed

## Reporting Format:
- **Current Phase**: [Phase name and progress]
- **Active Tasks**: [Tasks currently in progress]
- **Completed Deliverables**: [Recent completions]
- **Next Steps**: [Upcoming tasks and approvals needed]
- **Blockers**: [Any issues preventing progress]
```

---

## 🎭 Agent Role Declaration Protocol

### Role Declaration Requirements
Every agent interaction must clearly declare the active role to maintain transparency and context.

#### **When to Declare Role:**
```markdown
## MANDATORY Role Declaration:
1. **At start of each phase** - Declare coordinating role
2. **At start of each step** - Declare executing role
3. **When changing roles** - Announce transition
4. **When resuming work** - Restate current role
5. **When user asks questions** - Clarify which role is responding
```

#### **How to Declare Role:**
```markdown
## Role Declaration Format:
🎭 **I am acting as [Agent Role]** for [specific task/phase]

## Examples:
🎭 **I am acting as Project Manager** for Phase 1 coordination and setup
🎭 **I am acting as Product Manager** for market research and competitive analysis
🎭 **I am acting as Architect** for technical architecture design
🎭 **I am acting as Developer** for Story 001 implementation
🎭 **I am acting as QA** for Story 001 validation and verification
```

#### **Role Transition Protocol:**
```markdown
## When Changing Roles:
1. **Complete current role tasks** - Finish current step completely
2. **Update task states** - Mark current tasks as COMPLETE
3. **Announce transition** - "🎭 **Transitioning from [Current Role] to [New Role]**"
4. **Declare new role** - "🎭 **I am now acting as [New Role]** for [next task]"
5. **Load new context** - Read relevant agent file and context
6. **Begin new role tasks** - Start with new role's responsibilities

## Example Transition:
🎭 **Completing Product Manager role** - Market research finished
🎭 **Transitioning from Product Manager to Designer**
🎭 **I am now acting as Designer** for design research and UX patterns
```

#### **Role Context Loading:**
```markdown
## Before Acting in Any Role:
1. **Read agent file** - `.augment/agents/[role].md`
2. **Read current context** - `.augment/context/mission.md` and `roadmap.md`
3. **Check current phase** - Understand what phase/step you're in
4. **Review previous work** - Understand what's been completed
5. **Load relevant tools** - Prepare tools needed for this role
```

#### **Multi-Agent Coordination:**
```markdown
## When Multiple Agents Collaborate:
🎭 **I am acting as Product Manager** working with Architect for story creation
🎭 **I am acting as Developer** implementing Story 001, will hand off to QA for validation
🎭 **I am acting as Project Manager** coordinating between Designer and Developer

## Handoff Documentation:
- **Current State**: What has been completed
- **Next Steps**: What the next agent needs to do
- **Context**: Any important decisions or findings
- **Files**: What files have been created or modified
```

---

## 🎯 Protocol Usage Guidelines

### For Agents:
1. **Reference protocols** before starting any phase
2. **Follow tool usage** guidelines consistently
3. **Create and manage tasks** according to protocol
4. **Enforce quality gates** strictly
5. **Communicate progress** transparently

### For Workflows:
1. **Reference protocols** in workflow steps
2. **Include quality gates** at appropriate points
3. **Specify tool usage** for complex steps
4. **Define task creation** requirements
5. **Include approval points** clearly

### For Users:
1. **Understand approval points** in advance
2. **Provide specific feedback** when needed
3. **Review deliverables** promptly
4. **Escalate issues** if iterations exceed limits
5. **Trust the process** and methodology
