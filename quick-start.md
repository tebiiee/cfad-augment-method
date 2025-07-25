---
layout: default
title: "Quick Start Guide"
---

# 🚀 Quick Start Guide

Get up and running with CFAD methodology in 5 minutes.

## Prerequisites

- ✅ [Augment Code](https://augmentcode.com) installed and configured
- ✅ A project repository (GitHub recommended)
- ✅ Basic familiarity with AI agents

## Step 1: Download the Methodology

```bash
# Clone the repository
git clone https://github.com/tebiiee/cfad-augment-method.git

# Copy methodology to your project
cp cfad-augment-method/methodology-en.md /path/to/your/project/
```

## Step 2: Set Up Project Structure

Create the required directory structure in your project:

```bash
mkdir -p docs/project-input
mkdir -p docs/current-sprint/{planning,stories,verification,implementation}
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
"Apply this methodology: ./methodology-en.md for building [your project description]"
```

**Important**: Make sure the `methodology-en.md` file is open in your editor.

## Step 5: Let CFAD Guide You

The agent will follow the 3-phase process:

### 🔍 Phase 1: Analysis & Context ⏱️ ~10-15 minutes
- ✅ Analyze your project input
- ✅ Detect tech stack
- ✅ Configure GitHub Actions
- ✅ Set up MCPs

### 📋 Phase 2: Planning ⏱️ ~20-30 minutes  
- ✅ Define requirements
- ✅ Design architecture
- ✅ Create hyper-detailed stories
- ✅ Set up QA tools

### ⚡ Phase 3: Implementation ⏱️ Variable
- ✅ Implement stories one by one
- ✅ Run automated tests
- ✅ Verify with Playwright E2E
- ✅ Deploy to production

## 🎯 Success Tips

1. **Be Specific**: "Build an e-commerce platform with user auth, product catalog, and Stripe payments"
2. **Provide References**: Include screenshots, competitor examples, or API documentation
3. **Trust the Process**: Let the agent follow all phases - don't skip steps
4. **Review Carefully**: Take time to review and approve each phase
5. **Stay Engaged**: Provide feedback during mini-iterations

## Next Steps

- **[Read the Full Methodology](methodology-en.html)** - Understand all details
- **[View Examples](examples.html)** - See real project implementations  
- **[Join Discussions](https://github.com/tebiiee/cfad-augment-method/discussions)** - Get help

---

<div style="text-align: center; padding: 2rem; background: #f6f8fa; border-radius: 8px; margin: 2rem 0;">
  <h3>Ready to build something amazing?</h3>
  <p>Start your first CFAD project today!</p>
  <a href="methodology-en.html" style="background: #0366d6; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; display: inline-block;">Read Full Methodology →</a>
</div>
