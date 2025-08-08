# Augment Develop Method: Dynamic Rules Creation Protocol

## 🎯 Purpose
Protocol for creating project-specific rules during Phase 1 research, building upon the minimal essential rules that apply to all projects.

---

## 📋 Core Rules (Always Present)

### Universal Rules (Never Change)
These rules are fundamental to Augment Develop Method methodology and apply to ALL projects:

#### **File Organization**
- Stories: Always in `/docs/current-sprint/stories/`
- Verification: Always in `/docs/current-sprint/verification/`
- Research: Always in `/docs/research/`
- Context: Always in `.augment/context/`

#### **Quality Gates**
- ✅ Tests before implementation (when applicable)
- ✅ Green CI/CD pipeline before proceeding
- ✅ Code review using appropriate agent role
- ✅ Documentation updates

#### **Commit Standards**
- Format: `type: description`
- Types: `feat`, `fix`, `refactor`, `test`, `docs`, `chore`, `ci`
- One commit per deliverable/task

#### **Task Management**
- Real-time task state updates
- Dependencies checked before starting
- Blockers documented and escalated

---

## 🔧 Dynamic Rules Creation Process

### Phase 1: Rules Analysis & Creation
During technical feasibility research, the Architect agent should:

#### **Step 1: Analyze Project Requirements**
```markdown
## Rules Analysis Checklist:
- [ ] Review existing codebase patterns (if any)
- [ ] Analyze chosen technology stack
- [ ] Identify project-specific constraints
- [ ] Review team preferences from project inputs
- [ ] Consider industry standards for project type
- [ ] Assess security and compliance requirements
```

#### **Step 2: Technology Stack Rules**
```markdown
## Tech Stack Specific Rules:
- **Framework Rules**: Next.js, React, Vue specific patterns
- **Database Rules**: Prisma, Convex, Supabase specific patterns
- **Styling Rules**: Tailwind, CSS Modules, Styled Components
- **Testing Rules**: Jest, Playwright, Vitest configurations
- **Deployment Rules**: Vercel, Docker, AWS specific requirements
```

#### **Step 3: Project-Specific Rules**
```markdown
## Custom Rules Categories:

### Code Organization Rules
- **Component Structure**: How to organize React components
- **File Naming**: Conventions for files and directories
- **Import Order**: How to order imports in files
- **Folder Structure**: Project-specific folder organization

### Development Rules
- **Environment Setup**: Required tools and configurations
- **Development Workflow**: Branch naming, PR process
- **Code Review**: Specific review criteria for this project
- **Testing Strategy**: Unit, integration, E2E test requirements

### Business Rules
- **Feature Flags**: How to implement feature toggles
- **Analytics**: Required tracking and metrics
- **Performance**: Specific performance requirements
- **Accessibility**: WCAG compliance level required
- **Security**: Authentication, authorization patterns
```

---

## 📝 Rules Creation Templates

### Template: tech-stack-rules.md
```markdown
# Project-Specific Tech Stack Rules

**Generated**: [Date]
**Based on**: Technical feasibility research
**Stack**: [Primary technologies identified]

## Framework Rules
### [Framework Name] Specific
- **Component Patterns**: [Preferred patterns]
- **State Management**: [Redux, Zustand, Context, etc.]
- **Routing**: [App Router, Pages Router, etc.]
- **API Patterns**: [REST, GraphQL, tRPC, etc.]

## Database Rules
### [Database Name] Specific
- **Schema Patterns**: [How to structure schemas]
- **Query Patterns**: [Preferred query methods]
- **Migration Strategy**: [How to handle schema changes]
- **Data Validation**: [Validation patterns]

## Styling Rules
### [Styling Solution] Specific
- **Component Styling**: [How to style components]
- **Theme Management**: [Color schemes, typography]
- **Responsive Design**: [Breakpoint strategy]
- **Design System**: [Component library approach]

## Testing Rules
### [Testing Framework] Specific
- **Unit Test Patterns**: [How to structure unit tests]
- **Integration Patterns**: [API and component integration]
- **E2E Patterns**: [User flow testing with Playwright]
- **Mock Strategies**: [How to mock dependencies]
```

### Template: project-conventions.md
```markdown
# Project-Specific Conventions

**Generated**: [Date]
**Based on**: Project requirements and team preferences

## Naming Conventions
### Files and Directories
- **Components**: [PascalCase, kebab-case, etc.]
- **Pages**: [Naming pattern for pages/routes]
- **Utilities**: [Helper function naming]
- **Types**: [TypeScript type naming]

### Code Conventions
- **Variables**: [camelCase, snake_case preferences]
- **Constants**: [UPPER_CASE, camelCase]
- **Functions**: [Naming patterns for different function types]
- **Classes**: [Class naming and structure]

## Code Organization
### Component Structure
```
components/
  ui/           # Reusable UI components
  features/     # Feature-specific components
  layout/       # Layout components
  forms/        # Form components
```

### Import Order
1. React and framework imports
2. Third-party libraries
3. Internal utilities and hooks
4. Component imports
5. Type imports
6. Relative imports

## Development Workflow
### Branch Naming
- **Features**: `feature/[story-id]-[brief-description]`
- **Fixes**: `fix/[issue-id]-[brief-description]`
- **Refactor**: `refactor/[area]-[brief-description]`

### Commit Messages
- **Format**: `type(scope): description`
- **Scopes**: [Project-specific scopes like 'auth', 'ui', 'api']
- **Examples**: 
  - `feat(auth): implement user login flow`
  - `fix(ui): resolve button styling issue`
```

### Template: quality-standards.md
```markdown
# Project Quality Standards

**Generated**: [Date]
**Based on**: Project requirements and industry standards

## Code Quality
### Test Coverage
- **Minimum Coverage**: [80%, 90%, etc.]
- **Critical Paths**: [100% coverage required]
- **Test Types**: [Unit, integration, E2E requirements]

### Performance Standards
- **Page Load**: [< 3 seconds, etc.]
- **API Response**: [< 500ms, etc.]
- **Bundle Size**: [< 1MB, etc.]
- **Core Web Vitals**: [LCP, FID, CLS targets]

### Accessibility Standards
- **WCAG Level**: [AA, AAA]
- **Screen Reader**: [Required compatibility]
- **Keyboard Navigation**: [Full keyboard support]
- **Color Contrast**: [Minimum ratios]

## Security Standards
### Authentication
- **Method**: [JWT, OAuth, etc.]
- **Session Management**: [Timeout, refresh patterns]
- **Password Policy**: [Requirements]

### Data Protection
- **Encryption**: [At rest, in transit]
- **PII Handling**: [Data protection requirements]
- **Compliance**: [GDPR, CCPA, etc.]

## Documentation Standards
### Code Documentation
- **Function Documentation**: [JSDoc, TypeScript comments]
- **Component Documentation**: [Storybook, README]
- **API Documentation**: [OpenAPI, GraphQL schema]

### Process Documentation
- **Setup Instructions**: [Environment setup]
- **Deployment Guide**: [How to deploy]
- **Troubleshooting**: [Common issues and solutions]
```

---

## 🔄 Rules Integration Process

### During Phase 1 Research
```markdown
## Rules Creation Workflow:
1. **Analyze existing code** and patterns
2. **Research tech stack** best practices
3. **Identify project constraints** and requirements
4. **Create project-specific rules** using templates
5. **Validate rules** with existing code (if any)
6. **Document rules** in `.augment/rules/`
7. **Commit rules** with descriptive message
8. **Update main.md** to reference new rules
```

### Rules File Structure
```
.augment/rules/
├── main.md                    # Universal rules (never change)
├── tech-stack.md             # Minimal tech stack rules
├── code-style.md             # Basic code style rules
├── best-practices.md         # General best practices
├── project-tech-stack.md     # Project-specific tech rules
├── project-conventions.md    # Project-specific conventions
└── project-quality.md        # Project-specific quality standards
```

### Rules Validation
```markdown
## Validation Checklist:
- [ ] Rules don't contradict universal rules
- [ ] Rules are specific and actionable
- [ ] Rules align with project requirements
- [ ] Rules are consistent with chosen tech stack
- [ ] Rules include examples where helpful
- [ ] Rules are documented clearly
```

---

## 🎯 Rules Usage Guidelines

### For Agents
1. **Always read main.md** first for universal rules
2. **Load project-specific rules** based on current task
3. **Follow rules consistently** throughout development
4. **Suggest rule updates** when patterns emerge
5. **Document rule violations** and rationale

### For Rule Creation
1. **Build upon universal rules** - don't replace them
2. **Be specific and actionable** - avoid vague guidelines
3. **Include examples** for complex rules
4. **Consider maintainability** - rules should be sustainable
5. **Validate with existing code** - ensure consistency

### For Rule Evolution
1. **Update rules** when patterns change
2. **Document changes** in commit messages
3. **Communicate changes** to team
4. **Archive outdated rules** rather than deleting
5. **Review rules** periodically for relevance

---

## 📊 Rules Quality Metrics

### Rule Effectiveness
- **Consistency**: How consistently rules are followed
- **Clarity**: How well rules are understood
- **Completeness**: How well rules cover project needs
- **Maintainability**: How easy rules are to maintain

### Rule Evolution
- **Update Frequency**: How often rules need updates
- **Violation Rate**: How often rules are violated
- **Team Adoption**: How well team follows rules
- **Project Success**: How rules contribute to project success

---

**Remember**: Dynamic rules should enhance, not replace, the universal Augment Develop Method methodology. They provide project-specific guidance while maintaining methodological consistency.
