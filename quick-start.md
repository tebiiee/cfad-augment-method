---
layout: default
title: "Quick Start Guide"
---

# 🚀 Quick Start Guide

Get up and running with Augment Develop Method in 5 minutes.

## Prerequisites

- ✅ [Augment Code](https://augmentcode.com) installed and configured
- ✅ A project repository (GitHub recommended)
- ✅ Basic familiarity with AI agents

## Step 1: Download the Methodology

```bash
# Clone the repository
git clone https://github.com/tebiiee/cfad-augment-method.git

# Copy methodology to your project
cp cfad-augment-method/methodology.md /path/to/your/project/
```

## Step 2: Set Up Project Structure

Create the required directory structure in your project:

```bash
mkdir -p docs/project-input
mkdir -p docs/{stories,verification}/sprint-1
mkdir -p .augment/rules
```

## Step 3: Prepare Your Project Input

Create your project requirements in `docs/project-input/idea.md`:

```markdown
## Description
[Describe what you want to build]

## Requirements
- [List your requirements]

## Tech Stack Preferences
- [Any specific technologies you want to use]

## GitHub Repository
https://github.com/yourusername/your-repo
```

## Step 4: Start Your Augment Code Session

Open Augment Code and start a new conversation:

```
"Apply this methodology: ./methodology.md for building [your project description]"
```

**Important**: Make sure the `methodology.md` file is open in your editor.

## Step 5: Let Augment Develop Method Guide You

The agent will follow a multi-phase process (3-4 phases depending on work type):

### 🔍 Phase 1: Overview & Setup ⏱️ ~10-15 minutes
- ✅ Understand project structure and workflow selection
- ✅ Set up agent roles and coordination
- ✅ Establish project context and navigation
- ✅ Configure development environment

### 📋 Phase 2: Research/Analysis ⏱️ ~20-30 minutes
- ✅ Analyze project requirements and existing code
- ✅ Research market and technical feasibility
- ✅ Define architecture and technology decisions
- ✅ Document findings and recommendations

### 🎯 Phase 3: Planning ⏱️ ~30-45 minutes (for project-setup)
- ✅ Create hyper-detailed stories with UI-first approach
- ✅ Design technical specifications and API contracts
- ✅ Set up testing strategy and QA tools
- ✅ Organize sprint structure and dependencies

### ⚡ Phase 4: Implementation ⏱️ Variable (for project-setup)
- ✅ Implement stories with UI-first prioritization
- ✅ Run automated tests and quality gates
- ✅ Verify with Playwright E2E testing
- ✅ Deploy to production with CI/CD

## 🎯 Success Tips

1. **Be Specific**: "Build an e-commerce platform with user auth, product catalog, and Stripe payments"
2. **Provide References**: Include screenshots, competitor examples, or API documentation
3. **Trust the Process**: Let the agent follow all phases - don't skip steps
4. **Review Carefully**: Take time to review and approve each phase
5. **Stay Engaged**: Provide feedback during mini-iterations

## Next Steps

- **[Read the Full Methodology](methodology.html)** - Understand all details
- **[GitHub Repository](https://github.com/tebiiee/cfad-augment-method)** - Source code and issues
- **[Join Discussions](https://github.com/tebiiee/cfad-augment-method/discussions)** - Get help

---

<div style="text-align: center; padding: 2rem; background: #f6f8fa; border-radius: 8px; margin: 2rem 0;">
  <h3>Ready to build something amazing?</h3>
  <p>Start your first Augment Develop Method project today!</p>
  <a href="methodology.html" style="background: #0366d6; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; display: inline-block;">Read Full Methodology →</a>
</div>
