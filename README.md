# Docbot - Technical Documentation Agents

A suite of intelligent documentation agents for Claude Code that automatically document your codebase. These agents are invoked automatically when you request documentation for frontend or backend code.

## 📦 Installation

Copy the docbot agent files to your Claude Code agents directory:

```bash
# Clone the repository
git clone git@github.com:avidity/docbot.git
cd docbot

# Install to Claude Code agents directory
cp docbot*.md ~/.claude/agents/

# Or create a symlink to keep them updated
ln -s $(pwd)/docbot*.md ~/.claude/agents/
```

### Files Included

- `docbot-frontend.md` - Frontend/UI component documentation specialist
- `docbot-backend.md` - Backend code and API documentation specialist
- `example-info-for-claude-md.md` - Template for project-specific documentation guidelines

---

## Overview

Docbot provides specialized agents that automatically handle documentation for:
- **Frontend**: Components (React, Vue, Angular), hooks, state management, UI libraries
- **Backend**: Functions, classes, modules, APIs, server-side code (Python, Ruby, Go, Java, C#, etc.)

All documentation follows a **standard technical format** focused on developers..

## How It Works

Docbot uses Claude Code's agent system. When you request documentation, Claude automatically invokes the appropriate specialized agent:

**For frontend code:**
```
Document the UserProfile component in src/components/UserProfile.tsx
```
→ Claude automatically uses `docbot-frontend` agent

**For backend code:**
```
Document the payment webhook handler in src/api/webhooks.py
```
→ Claude automatically uses `docbot-backend` agent

No slash commands needed—just describe what you want documented!

## Documentation Standard

All documentation includes:
- Detailed overview with context
- All parameters/options with types and defaults
- Multiple usage examples
- Error handling basics
- Links to related code
- **Frontend**: Accessibility features (keyboard navigation, ARIA, screen readers)
- **Backend**: Side effects, thread safety, performance considerations

Focus: **Functionality, behavior, integration, and technical implementation**

## Agent Workflow

Both agents follow a consistent workflow:

1. **Analyze**: Reads code to understand what needs documenting
2. **Check Existing**: Searches for existing documentation
   - If found: Asks if you want to update or create new
   - If creating new: Suggests alternative names
3. **Ask (if needed)**: Only asks clarifying questions when necessary
   - Where to save documentation?
   - Include diagrams? Analyze git diffs?
4. **Research**: Gathers context from codebase
5. **Draft**: Creates standard technical documentation
6. **Present**: Shows draft and waits for approval
7. **Write**: Saves to files after approval

## Example Usage

Simply ask Claude to document your code:

```
Document the LoginForm component in src/components/LoginForm.tsx
```

```
Document the authentication middleware in src/middleware/auth.js
```

### Update Existing Docs

```
Update the API documentation in docs/api.md with the new authentication endpoints
```

### Document Multiple Files

```
Document all components in src/components/
```

### Create README

```
Create a README for this project
```

## Best Practices

### Be Specific

✅ Good: "Document the authentication flow in src/auth/AuthService.ts"
❌ Vague: "Document the auth stuff"

### Provide Context

Include helpful details in your request:
- "Document this API with cURL examples"
- "Focus on error handling"
- "Include integration examples"
- "Add accessibility documentation"

### Review Before Approval

- Check accuracy of the generated documentation
- Request changes if needed
- Approve only when satisfied

### Keep Docs Updated

```
Update the README with the new installation steps
```

## Troubleshooting

**Agent isn't finding files**
- Provide full file paths from project root
- Use glob patterns: `src/components/**/*.tsx`
- Example: "Document all TypeScript files in src/api/"

**Documentation already exists**
- The agent will ask if you want to update or create new
- Choose "Update existing" to modify current docs
- Choose "Create new" to get alternative filename suggestions

**Need different format**
- Request specific changes before approval
- Be explicit about what you want different
- Example: "Add more examples" or "Make it more concise"

**Too many clarifying questions**
- Be more specific in your initial request
- Include location in your prompt: "Document X in docs/components/"
- Specify format: "Add inline JSDoc comments" vs "Create a separate markdown file"

## Customization

Edit the agent files to customize behavior:
- Documentation templates and structure
- Style and tone
- Included/excluded sections
- Examples format
- Agent invocation criteria

```bash
# Edit frontend agent
vim ~/.claude/agents/docbot-frontend.md

# Edit backend agent
vim ~/.claude/agents/docbot-backend.md
```

## Project-Specific Guidelines

Use the `example-info-for-claude-md.md` template to create a `CLAUDE.md` file in your project root. This helps the agents understand your project's:
- Documentation style preferences
- Code conventions
- Project structure
- Language-specific requirements

```bash
# Copy template to your project
cp example-info-for-claude-md.md /your/project/CLAUDE.md

# Edit with your project details
vim /your/project/CLAUDE.md
```

The agents will automatically read and follow guidelines from `CLAUDE.md` when documenting your code.

**Ready to document?**

Just ask Claude to document your code—the agents handle the rest!

Happy documenting! 🤖
