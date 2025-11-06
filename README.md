# Docbot - Technical Documentation Specialist

Welcome to Docbot! A comprehensive documentation agent system designed to help software engineering teams create and maintain high-quality project documentation.

## 📦 Installation

To use Docbot with Claude Code, follow these steps:

### Option 1: Copy Files Manually

1. Copy all the docbot command files to your Claude Code commands directory:
   ```bash
   cp docbot*.md ~/.claude/commands/
   ```

2. Restart Claude Code or reload the commands

3. Invoke docbot:
   ```
   /docbot
   ```

### Option 2: Clone and Install

1. Clone this repository:
   ```bash
   git clone git@github.com:avidity/docbot.git
   cd docbot
   ```

2. Copy files to Claude Code commands directory:
   ```bash
   cp docbot*.md ~/.claude/commands/
   ```

3. Start using docbot:
   ```
   /docbot
   ```

### Files Included

- `docbot.md` - Main coordinator agent
- `docbot-frontend.md` - Frontend/UI component documentation specialist
- `docbot-backend.md` - Backend/API/server-side documentation specialist
- `docbot-api.md` - REST/GraphQL API documentation specialist
- `docbot-architecture.md` - System architecture and design documentation specialist
- `docbot-database.md` - Database schema and query documentation specialist

---

## Overview

Docbot is a specialised agent system that helps you:
- Create comprehensive technical documentation for any codebase
- Document APIs, components, architecture, databases, and more
- Maintain consistent documentation standards across projects
- Onboard new team members faster
- Generate AI-agent-friendly documentation
- **Tailor documentation for different audiences** - technical teams, product teams, or customer success
- **Use simple multiple-choice questions** - just select options instead of typing out requirements

## Quick Start

### Using Docbot

Simply invoke the main docbot command:

```
/docbot
```

Docbot will then:
1. Present you with **multiple-choice questions** to clarify requirements (just click to select!)
   - What depth of documentation? (Quick Reference | Standard | Comprehensive)
   - Who is the audience? (Technical Team | Product Team | Customer Success | Mixed)
   - Where should it go? (README | docs/ folder | inline comments)
   - Any extras? (Include diagrams, analyse git diffs, etc.)
2. Analyse your codebase based on your selections
3. Create a documentation draft tailored to your audience
4. Wait for your approval before writing to files

### Example Usage

**Document a React component:**
```
/docbot
> I want to document the UserProfile component in src/components/UserProfile.tsx
```

**Document an API:**
```
/docbot
> Document the authentication API endpoints in src/routes/auth.ts
```

**Create a README:**
```
/docbot
> Create a comprehensive README for this project
```

## Specialised Agents

Docbot includes specialised sub-agents for specific documentation needs:

### 1. `/docbot-frontend` - Frontend Documentation Specialist

Specialises in:
- React, Vue, Angular, Web Components
- Component props, events, and styling
- State management (Redux, MobX, Pinia)
- Accessibility documentation
- Performance optimisation

**Example:**
```
/docbot-frontend
> Document the Button component with full accessibility notes
```

### 2. `/docbot-backend` - Backend Documentation Specialist

Specialises in:
- API endpoints and routes
- Business logic and services
- Data models and schemas
- Middleware and authentication
- Error handling and validation

**Example:**
```
/docbot-backend
> Document the OrderService class and its methods
```

### 3. `/docbot-api` - API Documentation Specialist

Specialises in:
- REST API endpoints
- GraphQL schemas
- OpenAPI/Swagger specifications
- Authentication and rate limiting
- Request/response examples in multiple languages

**Example:**
```
/docbot-api
> Create complete API documentation for all endpoints in src/routes/
```

### 4. `/docbot-architecture` - Architecture Documentation Specialist

Specialises in:
- System architecture diagrams
- Design decisions and trade-offs
- Data flow and component interactions
- Deployment and scaling strategies
- Security architecture

**Example:**
```
/docbot-architecture
> Document the overall system architecture including microservices
```

### 5. `/docbot-database` - Database Documentation Specialist

Specialises in:
- Database schemas and ER diagrams
- Table structures and relationships
- Indexes and query performance
- Migrations and data integrity
- Backup and recovery procedures

**Example:**
```
/docbot-database
> Document the users and orders tables with ER diagram
```

## Documentation Depth Levels

Docbot supports three depth levels:

### 1. Quick Reference (Minimal)
- Brief overview
- Essential parameters/options
- One simple example
- Use when: Creating quick reference docs or cheat sheets

### 2. Standard (Moderate)
- Detailed overview with context
- All parameters with types and defaults
- Multiple examples
- Error handling basics
- Use when: General documentation needs (most common)

### 3. Comprehensive (Extensive)
- In-depth explanation with "why" context
- All parameters with edge cases
- Multiple examples from simple to advanced
- Performance considerations
- Common pitfalls and solutions
- Use when: Critical systems, public APIs, complex features

## Target Audiences

Docbot can tailor documentation for different audiences:

- **Technical Team (Developers)**: Code-focused documentation with technical depth, implementation details, edge cases, and performance considerations. Perfect for developers who need to understand how things work under the hood.

- **Product Team**: High-level feature documentation focusing on what the system does, user flows, business logic, and feature capabilities. Minimal code, more diagrams and plain language explanations. Great for product managers who need to understand features without diving into implementation.

- **Customer Success/Support Team**: User-facing documentation explaining how features work, troubleshooting guides, common issues, and solutions. No code, plain language only. Perfect for support teams helping customers.

- **AI Agents**: Structured, precise, machine-readable format with complete specifications, type information, and exhaustive parameter documentation.

- **Mixed Audience**: Layered documentation with both technical and non-technical sections. Includes executive summary, plain language overview, and technical deep-dive sections. Best when multiple teams need to reference the same documentation.

## Best Practises

### When to Use Docbot

✅ **Good use cases:**
- Documenting new features or components
- Updating outdated documentation
- Creating project READMEs
- Documenting complex APIs or services
- Architecture decision records
- Onboarding documentation

❌ **Not ideal for:**
- Generating code (docbot focuses on documentation)
- Extremely trivial documentation (single-line comments)
- Documentation that requires business context you haven't provided

### Tips for Best Results

1. **Be Specific**: Tell docbot exactly what you want documented
   - Good: "Document the authentication flow in src/auth/AuthService.ts"
   - Less good: "Document the authentication stuff"

2. **Provide Context**: If you have specific requirements, mention them
   - "Document this API with examples in Python and JavaScript"
   - "Focus on security considerations"
   - "Include performance benchmarks"

3. **Review Before Approval**: Docbot will show you the draft before writing
   - Review for accuracy
   - Request changes if needed
   - Approve only when satisfied

4. **Keep Documentation Updated**: Use docbot to update docs when code changes
   - "Update the README with new installation steps"
   - "Update the API docs to reflect the new authentication flow"

## Workflow

Docbot follows a consistent workflow:

1. **Analyse**: Reads relevant code files to understand what needs documenting
2. **Ask**: Presents **multiple-choice questions** for easy selection - you just click options instead of typing answers! Questions include:
   - Documentation depth (Quick Reference, Standard, or Comprehensive)
   - Target audience (Technical Team, Product Team, Customer Success, or Mixed)
   - Documentation location (README, docs/ folder, inline comments, or new file)
   - Additional options (analyse git diffs, include diagrams, validate existing docs, etc.)
3. **Research**: Explores codebase to gather context
4. **Draft**: Creates comprehensive documentation tailored to your selected audience
5. **Present**: Shows you the draft with explanations
6. **Approve**: Waits for your approval before writing to files
7. **Write**: Writes documentation to specified files

**Easy Interaction**: Docbot uses multiple-choice questions so you can quickly select options instead of typing out responses. This makes the documentation process faster and more streamlined!

## Features

### Built-in Templates

Docbot includes templates for:
- API endpoints (REST, GraphQL)
- Functions and methods
- Components (React, Vue, Angular)
- Architecture documents
- README files
- Database schemas
- And more...

### Mermaid Diagrams

Docbot can create visual diagrams:
- Entity-Relationship diagrams
- Architecture diagrams
- Sequence diagrams
- State machines
- Data flow diagrams

### Multi-Language Examples

For APIs, docbot can provide examples in:
- JavaScript/TypeScript
- Python
- cURL
- Go
- Java
- And more...

### British English

All documentation is written in British English with professional, developer-friendly tone.

## Examples

### Example 1: Document a New Feature

```
/docbot
> I just added a new feature for exporting user data.
> Can you document it? Files are in src/features/export/

[Docbot presents multiple-choice questions:]
- Depth: Standard ✓
- Audience: Product Team ✓ (you select this to create non-technical docs)
- Include diagrams: Yes ✓

[Docbot creates documentation with plain language explanations,
 user flow diagrams, and feature capabilities - no code!]
```

### Example 2: Update API Documentation

```
/docbot-api
> The authentication API has changed.
> Update docs/api.md to reflect the new OAuth flow in src/auth/

[Docbot will analyse changes and update documentation]
```

### Example 3: Architecture Documentation

```
/docbot-architecture
> Create architecture documentation for the new microservices setup.
> Focus on the order processing service and payment integration.

[Docbot will create comprehensive architecture docs with diagrams]
```

### Example 4: Database Schema

```
/docbot-database
> Document the database schema with ER diagrams.
> Include the users, orders, and products tables.

[Docbot presents questions:]
- Audience: Mixed Audience ✓ (for both developers and product team)

[Docbot creates layered documentation with:
 - Executive summary for product team (what data we store and why)
 - ER diagrams for visual understanding
 - Technical schema details for developers
 - Index and performance information for technical team]
```

### Example 5: Feature Documentation for Support Team

```
/docbot
> Document the password reset feature for customer support team

[Docbot presents questions:]
- Audience: Customer Success ✓

[Docbot creates user-friendly troubleshooting guide:
 - How the password reset flow works (plain language)
 - Common issues customers face
 - Step-by-step troubleshooting guide
 - No technical jargon or code!]
```

## Troubleshooting

### Docbot isn't finding my files
- Make sure you provide the correct file paths
- Use relative paths from your project root
- Docbot can search the codebase if you're unsure of exact paths

### Documentation is too detailed/not detailed enough
- Specify the depth level when invoking docbot
- Request changes before approving the draft
- You can always ask docbot to regenerate with different depth

### Docbot is documenting the wrong thing
- Be more specific in your initial request
- Provide file paths when possible
- Answer the clarifying questions carefully

### Documentation needs updates after code changes
- Re-run docbot with "update" in your request
- Docbot can analyse git diffs to see what changed
- Show docbot the existing docs and ask for updates

## Integration Options

When you invoke docbot, it can offer to:
- Analyse git diffs to understand recent changes
- Validate existing documentation for completeness
- Check for related undocumented code
- Suggest documentation improvements

Just mention these options when using docbot!

## Contributing

If you'd like to contribute to Docbot:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes to the agent files
4. Test your changes with Claude Code
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Customisation

You can customise docbot for your team by:
- Editing the templates in the agent files
- Adding your own documentation standards
- Creating team-specific documentation patterns
- Adding new specialised sub-agents

## Support

If you need help or want to provide feedback:
- Open an issue in this repository
- Share examples of documentation you'd like to see
- Suggest new features or improvements

## Licence

[Add your licence here]

---

**Ready to create amazing documentation?**

Start with: `/docbot`

Happy documenting! 📚
