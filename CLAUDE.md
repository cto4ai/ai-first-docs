# CLAUDE.md

This file provides guidance to **Claude Code** (claude.ai/code) when working with code in this workspace.

## Workspace Configuration

**Note**: This CLAUDE.md covers the entire workspace containing two repositories.

This is a dual-repository workspace containing:

- **ai-first-docs** (current): The AI-first documentation template repository
  - Template structure and examples
  - CI/CD workflows and validation
  - Documentation strategy and setup guides

- **ai-first-docs-mcp**: MCP (Model Context Protocol) configurations and tools
  - Claude Desktop project configurations
  - GitHub MCP setup files
  - Integration examples and tools

Both repositories work together to provide a complete AI-first documentation solution.

## AI Integration Architecture

This repository uses a **dual AI configuration** approach:

- **`CLAUDE.md`** (this file): Configuration for **Claude Code** integration
  - Technical editing workflows
  - Development and validation processes
  - Repository structure and command reference
  - Best practices for code-assisted documentation work

- **`.claude/DOCUMENT_ASSISTANT.md`**: Instructions for **Claude Desktop Projects**
  - Business user editing workflows
  - Artifact-based visual document editing
  - Organization-specific assistant behavior
  - Non-technical user guidance

Both configurations work together to provide comprehensive AI-first documentation support for different user types and workflows.

## Repository Purpose

This is an **AI-first documentation template** implementing a paradigm shift where documentation is primarily accessed and maintained through AI tools rather than traditional human navigation. The core strategy is documented in `.github/DOCUMENTATION/ai-first-documentation-strategy.md`.

## Key Architecture Decision

This repository implements AI-first documentation workflows through Model Context Protocol (MCP) integration. The implementation follows one of these paths:

- **Option A**: Use existing MCP servers (`@modelcontextprotocol/server-filesystem`, `@modelcontextprotocol/server-github`)
- **Option B**: Build custom MCP server for specialized functionality
- **Hybrid**: Start with existing MCPs, add custom validation layers

See `.github/DOCUMENTATION/ai-first-documentation-strategy.md` for detailed comparison and decision framework.

## Essential Commands

### Development & Validation
```bash
# Install dependencies
npm install

# Run all validation checks
npm run validate

# Individual validation commands
npm run lint        # Markdown linting with markdownlint-cli2
npm run spell       # Spell check with cspell
npm run links       # Link validation with markdown-link-check

# Repository initialization (interactive setup)
npm run init

# Test repository setup
npm run test:setup
```

### Build Commands
```bash
# Build PDF documentation
npm run build:pdf

# Build static HTML site (MkDocs)
npm run build:html

# Serve documentation locally
npm run serve
```

## Directory Structure

```
docs/                           # Main documentation content
├── policies/                   # Organization policies (AI-editable with constraints)
├── procedures/                 # Standard operating procedures
├── architecture/               # Technical documentation
├── guides/                     # How-to guides and tutorials
├── references/                 # API docs and reference materials
└── templates/                  # Document templates with AI instructions

.github/DOCUMENTATION/          # Meta-documentation (critical reading)
├── ai-first-documentation-strategy.md    # Core AI-first paradigm explanation
└── setup-guide.md             # Repository setup and configuration

scripts/                        # Utility scripts
└── init-repo.js               # Interactive repository personalization
```

## AI-First Features

### Semantic Markers for AI Interaction
Content includes special markers to guide AI behavior:
- `<!-- AI-CONTEXT: ... -->` - Provides context for AI processing
- `<!-- AI-READONLY -->` - Sections AI should never modify
- `<!-- AI-UPDATEABLE: type=statistics -->` - Content AI can update
- `<!-- AI-EXAMPLE: -->` - Examples AI can regenerate

### Metadata-Rich Frontmatter
Documents include AI-specific metadata:
```yaml
---
id: POL-SEC-001
ai_editable: true
ai_instructions: |
  - Update statistics quarterly
  - Never modify regulatory sections
ai_edit_constraints:
  - preserve_sections: [3, 4.2, 7]
  - require_human_approval: true
---
```

### Permission Model
AI write permissions are configured in `.github/ai-permissions.yaml` following the patterns documented in the strategy guide.

## Template Usage

This is a template repository designed to be:
1. **Used as a GitHub template** to create organization-specific documentation repositories
2. **Customized** with organization details, terminology, and workflows
3. **Extended** with additional content types and validation rules

### Template Customization Process
When creating a new repository from this template:
- Replace placeholder variables with organization-specific values
- Customize AI instructions in `.claude/DOCUMENT_ASSISTANT.md`
- Update validation rules and workflows
- Add organization-specific document templates

## Workflow Integration

### Branch Strategy
- `doc/*` - Documentation changes
- `fix/*` - Corrections and fixes
- `feature/*` - New documentation sections

### AI Edit Workflows
1. **Immediate Update** - For low-risk content (statistics, examples)
2. **Reviewed Update** - For policy changes requiring human approval
3. **Autonomous Zones** - Specific paths where AI can commit directly

## MCP Integration

### Current Setup
Template repository with example MCP configurations in the companion `ai-first-docs-mcp` repository.

### MCP Implementation Notes

When implementing MCP integration:

1. **Phase 1**: Read-only AI access via existing MCP servers
2. **Phase 2**: Assisted updates with human review
3. **Phase 3**: Autonomous zones for specific content types
4. **Phase 4**: Self-maintaining documentation with AI proactive updates

The repository structure and validation workflows are designed to support AI-assisted editing through MCP-enabled tools.

### GitHub Integration
- **Template Repository**: cto4ai/ai-first-docs
- **MCP Configuration**: See companion repository `ai-first-docs-mcp` for setup examples
- **Artifact Integration**: Enabled for visual document editing

## Validation & Quality Control

All content changes (human or AI-generated) must pass:
- Markdown linting (`.markdownlint.json`)
- Spell checking (`cspell.json`)
- Link validation
- GitHub Actions workflows (`.github/workflows/validate.yml`)

Pre-commit validation prevents issues and maintains quality regardless of contribution source.

## AI Assistant Instructions

### Working with Template Content
When editing documents in this repository:

1. **Maintain Template Integrity**
   - Preserve placeholder patterns for future customization
   - Keep example content clearly marked as examples
   - Maintain documentation strategy consistency

2. **Handle Template Variables**
   - Be aware of `{{PLACEHOLDER}}` patterns
   - Understand template vs. final repository differences
   - Preserve customization instructions

3. **Documentation Guidelines**
   - Focus on template usability and clarity
   - Include comprehensive examples and explanations
   - Maintain consistency with AI-first documentation principles

### Document Types and Handling

#### Template Files
- **Examples**: Clearly marked and easily removable/customizable
- **Instructions**: Comprehensive setup and usage guidance
- **Placeholders**: Consistent variable naming and replacement patterns

#### Strategy Documentation
- **Core Concepts**: Maintain consistency with AI-first principles
- **Implementation Guides**: Practical, actionable instructions
- **Best Practices**: Based on real-world usage and feedback

#### Configuration Files
- **AI Instructions**: Template-ready with customization points
- **Validation Rules**: Comprehensive but customizable
- **Workflows**: Production-ready CI/CD patterns