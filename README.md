# 🎩 Cursor Development Hats

> Modular AI assistant system for structured development workflows in Cursor IDE

Transform your Cursor IDE experience with a disciplined, modular approach to AI-assisted development. Each "hat" is a specialized AI assistant with a single responsibility, explicit confirmation points, and clear handoffs to eliminate scope creep and context drift.

## 🚀 Quick Start

1. **Clone this repository**
   ```bash
   git clone https://github.com/yourusername/cursor-hats.git
   cd cursor-hats
   ```

2. **Copy rules to your project**
   ```bash
   cp -r .cursor/ /path/to/your/project/
   ```

3. **Start using hats**
   ```
   Tell Cursor: "Use Bug RCA Hat to analyze this issue"
   ```

## 🎯 Core Principles

- **🔍 Single Responsibility**: Each hat has one atomic function
- **✋ Explicit Confirmations**: Every hat waits for user approval before proceeding
- **🎯 No Scope Creep**: Execution hats only do what was planned and approved
- **🔄 Workflow Flexibility**: Switch workflows anytime with Checkpoint Hat

## 🎩 The Hat Collection

### 🔍 Analysis & Understanding
- **📋 Context Realigner** - Analyzes current codebase state and realigns understanding
- **🔍 Bug RCA** - Performs thorough root cause analysis of bugs
- **🔬 Workflow Analyzer** - Analyzes feature requirements and dependencies

### 💡 Planning & Design
- **💡 Fix Ideator** - Suggests multiple potential fixes based on RCA
- **📋 Task Builder** - Creates structured task breakdown for features
- **🎯 Subtask Planner** - Plans implementation approach for specific subtasks

### ⚡ Execution & Implementation
- **⚡ Fix Executor** - Implements selected fixes with surgical precision
- **🚀 Subtask Executor** - Executes planned subtasks and tracks progress

### ✅ Review & Validation
- **✅ Code Review** - Comprehensive quality, security, and best practices review

### 🔄 Workflow Management
- **🔄 Checkpoint** - Pauses workflow, summarizes state, allows workflow switching

## 📋 Workflows

### 🐛 Bug Fix Workflow
```
🐛 Bug Report
    ↓
📋 Context Realigner (optional)
    ↓
🔍 Bug RCA
    ↓
💡 Fix Ideator
    ↓
⚡ Fix Executor
    ↓
✅ Code Review (optional)
```

### ⚡ Feature Development Workflow
```
📝 Feature Request
    ↓
📋 Context Realigner (optional)
    ↓
🔬 Workflow Analyzer
    ↓
📋 Task Builder
    ↓
┌─────────────────────────┐
│  FOR EACH SUBTASK:      │
│  🎯 Subtask Planner     │
│      ↓                  │
│  🚀 Subtask Executor    │
│      ↓                  │
│  🔄 Checkpoint          │
│      ↓                  │
│  [Repeat or Continue]   │
└─────────────────────────┘
    ↓
✅ Code Review
```

## 📁 Installation

### Option 1: Direct Copy
```bash
# Copy individual hat files to your project
mkdir -p .cursor/rules
cp rules/*.mdc .cursor/rules/
```

### Option 2: Git Submodule (Recommended)
```bash
# Add as submodule to keep updated
git submodule add https://github.com/yourusername/cursor-hats.git .cursor-hats
ln -s ../.cursor-hats/rules .cursor/rules
```

### Option 3: Download Individual Hats
Download only the hats you need from the `/rules` directory.

## 💡 Usage Examples

### Starting a Bug Fix
```
🗣️ You: "Use Bug RCA Hat. I have a login issue where users can't authenticate."

🤖 Cursor: [Performs root cause analysis]
→ Suggests: "Use Fix Ideator Hat to brainstorm solutions"

🗣️ You: "Use Fix Ideator Hat"

🤖 Cursor: [Provides 3 solution options]
→ Suggests: "Use Fix Executor Hat with Option 2"
```

### Starting Feature Development
```
🗣️ You: "Use Workflow Analyzer Hat. I need to add user profiles with avatar upload."

🤖 Cursor: [Analyzes requirements and dependencies]
→ Suggests: "Use Task Builder Hat to create implementation plan"

🗣️ You: "Use Task Builder Hat"

🤖 Cursor: [Creates structured task breakdown]
→ Suggests: "Use Subtask Planner Hat for first task"
```

### Context Recovery
```
🗣️ You: "Use Context Realigner Hat. I'm lost in this codebase."

🤖 Cursor: [Analyzes current state and provides orientation]
→ Suggests: "Use Checkpoint Hat to choose next workflow"
```

## 🎯 Hat Selection Guide

| Situation | Start With | Next Hat |
|-----------|------------|----------|
| 🐛 Bug reported | Bug RCA Hat | Fix Ideator Hat |
| ⚡ New feature | Workflow Analyzer Hat | Task Builder Hat |
| 🤔 Lost/confused | Context Realigner Hat | Checkpoint Hat |
| 🔄 Mid-development | Checkpoint Hat | [Based on status] |
| ✅ Ready for review | Code Review Hat | [End or continue] |

## 📖 Best Practices

### ✅ Do
- Wait for hat confirmation before proceeding
- Use Checkpoint Hat when switching contexts
- Start with Context Realigner when uncertain
- Follow the suggested next hat recommendations
- Keep hats focused on their single responsibility

### ❌ Don't
- Let hats do work outside their scope
- Skip planning phases for complex features
- Make code changes without approval
- Mix multiple hat responsibilities
- Ignore the explicit confirmation points

## 🔧 Customization

### Adding Your Own Hats
1. Create a new `.mdc` file in `.cursor/rules/`
2. Follow the metadata format:
```markdown
---
description: Your Hat Name - Brief description of responsibility
globs: ["*"]
alwaysApply: false
---

# Your Hat Name

You are the [Role]. Your responsibility is to [single responsibility].

## CONSTRAINTS
- [Specific limitations]
- [What NOT to do]

## OUTPUT FORMAT
[Structured format for responses]
```

### Modifying Existing Hats
Edit the `.mdc` files to adjust behavior, constraints, or output formats to match your team's needs.

## 🎯 Why Use Cursor Hats?

### Before Cursor Hats
- 😵 Context drift and confusion
- 🔄 Scope creep in AI suggestions
- 🤔 Unclear next steps
- 🎯 Mixing analysis with implementation
- 📝 Inconsistent development approaches

### After Cursor Hats
- ✅ Clear, focused AI assistance
- 🎯 Single responsibility per interaction
- 📋 Structured, predictable workflows
- 🔄 Easy context switching and recovery
- 🚀 Faster, more disciplined development

## 🙏 Acknowledgments

- Inspired by the @Cursor IDE and its powerful rules system
- Built for developers who want disciplined, structured AI assistance
- Thanks to the community for feedback and contributions