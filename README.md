# Docbot - Technical Documentation Specialist

A streamlined documentation agent for creating consistent, technical documentation for your codebase.

## 📦 Installation

Copy the docbot files to your Claude Code commands directory:

```bash
# Clone the repository
git clone git@github.com:avidity/docbot.git
cd docbot

# Install to Claude Code
cp docbot*.md ~/.claude/commands/

# Start using
/docbot
```

### Files Included

- `docbot.md` - Main documentation agent
- `docbot-frontend.md` - Frontend/UI component specialist

---

## Overview

Docbot helps you create technical documentation for:
- Components (React, Vue, Angular)
- Functions and methods
- APIs and endpoints
- Architecture and system design
- README files and project setup
- Database schemas

All documentation follows a **standard technical format** focused on developers, written in British English.

## Quick Start

Invoke docbot:

```
/docbot
```

You'll see:
```
🤖 Ready to document. What would you like me to document?
```

Then tell docbot what you need:

```
> Document the UserProfile component in src/components/UserProfile.tsx
```

Docbot will:
1. Analyze your code
2. Check if documentation already exists (and ask if you want to update or create new)
3. Ask clarifying questions only when needed (e.g., where to save the file)
4. Create a documentation draft
5. Wait for your approval before writing files

## Specialized Agent

### `/docbot-frontend` - Frontend Documentation Specialist

Use for frontend-specific documentation:
- React, Vue, Angular components
- Props, events, and hooks
- State management
- Component integration

**Example:**
```
/docbot-frontend
> Document the Button component with all props and usage examples
```

## Documentation Standard

All documentation includes:
- Detailed overview with context
- All parameters/options with types and defaults
- Multiple usage examples
- Error handling basics
- Links to related code

**Excluded by default** (unless explicitly requested):
- Performance tips and optimization
- Common pitfalls
- Test examples
- Future enhancements

**Never documented** (unless explicitly requested):
- Styling (CSS, colors, fonts, spacing)
- Visual appearance and design
- Theme configuration

Focus: **Functionality, behavior, integration, and technical implementation**

## Workflow

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

### Document a Component

```
/docbot
> Document the LoginForm component
```

### Update Existing Docs

```
/docbot
> Update the API documentation in docs/api.md with the new authentication endpoints
```

### Create README

```
/docbot
> Create a README for this project
```

### Frontend-Specific

```
/docbot-frontend
> Document all components in src/components/
```

## Best Practices

### Be Specific

✅ Good: "Document the authentication flow in src/auth/AuthService.ts"
❌ Vague: "Document the auth stuff"

### Provide Context

- "Document this API with cURL examples"
- "Focus on error handling"
- "Include integration examples"

### Review Before Approval

- Check accuracy
- Request changes if needed
- Approve only when satisfied

### Keep Docs Updated

```
/docbot
> Update the README with the new installation steps
```

## Troubleshooting

**Docbot isn't finding files**
- Provide full file paths from project root
- Use glob patterns: `src/components/**/*.tsx`

**Documentation exists already**
- Docbot will ask if you want to update or create new
- Choose "Update existing" to modify current docs
- Choose "Create new" to get alternative filename suggestions

**Need different format**
- Request specific changes before approval
- Be explicit about what you want different

**Docbot asks too many questions**
- Be more specific in your initial request
- Include location in your prompt: "Document X in docs/components/"

## Customization

Edit the agent files to customize:
- Documentation templates
- Style and tone
- Excluded sections
- Examples format

```bash
# Edit main agent
vim ~/.claude/commands/docbot.md

# Edit frontend specialist
vim ~/.claude/commands/docbot-frontend.md
```

## Support

- Open an issue in this repository
- Share feedback and suggestions
- Request new features

---

**Ready to document?**

```
/docbot
```

Happy documenting! 🤖
