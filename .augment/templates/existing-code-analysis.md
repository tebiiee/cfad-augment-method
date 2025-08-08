# Template: existing-code-analysis.md

```markdown
# Existing Code & Assets Analysis

**Date**: [YYYY-MM-DD]
**Project**: [Project Name]
**Analyst**: [Developer Agent]

## 🎯 Analysis Purpose
Document existing codebase patterns, dependencies, and reusable assets to inform development decisions and maintain consistency.

---

## 📊 Codebase Overview

### Repository Structure
```
[Project Root]/
├── [folder1]/
│   ├── [subfolder]/
│   └── [files]
├── [folder2]/
└── [configuration files]
```

### Technology Stack Detected
- **Frontend**: [Framework/Library versions]
- **Backend**: [Framework/Language versions]
- **Database**: [Database type and version]
- **Build Tools**: [Build system and tools]
- **Testing**: [Testing frameworks]
- **Deployment**: [Deployment platform/tools]

### Dependencies Analysis
- **Production Dependencies**: [X packages]
- **Development Dependencies**: [X packages]
- **Outdated Dependencies**: [List any outdated packages]
- **Security Vulnerabilities**: [Any security issues found]

---

## 🏗️ Architecture Analysis

### Code Organization Patterns
- **File Structure**: [How files are organized]
- **Naming Conventions**: [Current naming patterns]
- **Import/Export Patterns**: [How modules are structured]
- **Configuration Management**: [How config is handled]

### Design Patterns Used
- **State Management**: [Redux, Context, etc.]
- **Component Patterns**: [HOCs, Hooks, etc.]
- **API Patterns**: [REST, GraphQL, etc.]
- **Error Handling**: [How errors are managed]

### Code Quality Assessment
- **Code Style**: [Consistent/Inconsistent, linting setup]
- **Documentation**: [Level of code documentation]
- **Test Coverage**: [Current test coverage percentage]
- **Performance**: [Any performance considerations]

---

## 🔧 Development Environment

### Setup Requirements
- **Node Version**: [Required Node.js version]
- **Package Manager**: [npm, yarn, pnpm]
- **Environment Variables**: [Required env vars]
- **External Services**: [APIs, databases, etc.]

### Development Tools
- **IDE Configuration**: [VSCode settings, extensions]
- **Linting**: [ESLint, Prettier configuration]
- **Testing**: [Jest, Cypress, etc. setup]
- **Build Process**: [How to build the project]

### Local Development
- **Installation Steps**: [How to set up locally]
- **Development Server**: [How to start dev server]
- **Database Setup**: [Local database requirements]
- **Common Issues**: [Known setup problems and solutions]

---

## 🎨 UI/UX Analysis

### Design System
- **Component Library**: [Existing component library]
- **Styling Approach**: [CSS, Styled Components, etc.]
- **Design Tokens**: [Colors, typography, spacing]
- **Responsive Strategy**: [How responsiveness is handled]

### User Interface Patterns
- **Navigation**: [How navigation is implemented]
- **Forms**: [Form handling patterns]
- **Data Display**: [Tables, lists, cards patterns]
- **Interactions**: [Modals, dropdowns, etc.]

---

## 📈 Performance & Optimization

### Current Performance
- **Bundle Size**: [Current bundle size]
- **Load Times**: [Page load performance]
- **Runtime Performance**: [Any performance bottlenecks]
- **SEO Considerations**: [SEO setup and optimization]

### Optimization Opportunities
- **Code Splitting**: [Current code splitting strategy]
- **Lazy Loading**: [What's being lazy loaded]
- **Caching**: [Caching strategies in place]
- **Image Optimization**: [How images are handled]

---

## 🔄 Reusable Assets

### Components
- **Reusable Components**: [List of components that can be reused]
- **Component Documentation**: [How components are documented]
- **Component Testing**: [How components are tested]

### Utilities & Helpers
- **Utility Functions**: [Reusable utility functions]
- **Custom Hooks**: [React hooks that can be reused]
- **API Helpers**: [API utility functions]
- **Validation Schemas**: [Form validation schemas]

### Configuration
- **Build Configuration**: [Webpack, Vite, etc. config]
- **Environment Configuration**: [Environment-specific configs]
- **Testing Configuration**: [Test setup and configuration]

---

## 🚨 Technical Debt & Issues

### Code Quality Issues
- **Inconsistencies**: [Code style or pattern inconsistencies]
- **Deprecated Code**: [Outdated patterns or dependencies]
- **Performance Issues**: [Known performance problems]
- **Security Concerns**: [Security vulnerabilities or concerns]

### Maintenance Needs
- **Dependency Updates**: [Dependencies that need updating]
- **Refactoring Opportunities**: [Code that could be improved]
- **Documentation Gaps**: [Missing or outdated documentation]
- **Test Coverage Gaps**: [Areas lacking test coverage]

---

## 📋 Development Recommendations

### Immediate Actions
- **Priority 1**: [Most urgent improvements needed]
- **Priority 2**: [Important but not urgent improvements]
- **Priority 3**: [Nice-to-have improvements]

### Development Standards
- **Code Style**: [Recommended coding standards]
- **Testing Strategy**: [Recommended testing approach]
- **Documentation**: [Documentation standards to follow]
- **Performance**: [Performance standards to maintain]

### Integration Considerations
- **New Feature Integration**: [How new features should integrate]
- **Backward Compatibility**: [Compatibility considerations]
- **Migration Strategy**: [If major changes are needed]

---

## 🎯 Next Steps

### For New Development
- **Patterns to Follow**: [Established patterns to continue using]
- **Patterns to Avoid**: [Patterns that should be deprecated]
- **New Patterns**: [New patterns to introduce]

### For Team Onboarding
- **Key Files**: [Important files for new developers to understand]
- **Learning Resources**: [Documentation or resources for the stack]
- **Common Pitfalls**: [Things new developers should watch out for]

### For Deployment
- **Build Process**: [How the project is built for production]
- **Environment Setup**: [Production environment requirements]
- **Monitoring**: [How the application is monitored]
- **Rollback Strategy**: [How to rollback if issues occur]

---

**Analysis Complete**: [Date]
**Next Review**: [Recommended date for next analysis]
**For Questions**: Contact [Developer Agent] or refer to project documentation
```
