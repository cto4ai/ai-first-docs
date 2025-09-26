# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is an **AI-first documentation repository** implementing a paradigm shift where documentation is primarily accessed and maintained through AI tools rather than traditional human navigation. The core strategy is documented in `.github/DOCUMENTATION/ai-first-documentation-strategy.md`.

## Key Architecture Decision

This repository is preparing to implement Model Context Protocol (MCP) integration to enable AI-native documentation workflows. The implementation will follow one of these paths:

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
├── policies/                   # Company policies (AI-editable with constraints)
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
AI write permissions will be configured in `.github/ai-permissions.yaml` (to be created) following the patterns documented in the strategy guide.

## Workflow Integration

### Branch Strategy
- `doc/*` - Documentation changes
- `fix/*` - Corrections and fixes
- `feature/*` - New documentation sections

### AI Edit Workflows
1. **Immediate Update** - For low-risk content (statistics, examples)
2. **Reviewed Update** - For policy changes requiring human approval
3. **Autonomous Zones** - Specific paths where AI can commit directly

## MCP Implementation Notes

When implementing MCP integration:

1. **Phase 1**: Read-only AI access via existing MCP servers
2. **Phase 2**: Assisted updates with human review
3. **Phase 3**: Autonomous zones for specific content types
4. **Phase 4**: Self-maintaining documentation with AI proactive updates

The repository structure and validation workflows are already designed to support AI-assisted editing through MCP-enabled tools.

## Validation & Quality Control

All content changes (human or AI-generated) must pass:
- Markdown linting (`.markdownlint.json`)
- Spell checking (`cspell.json`)
- Link validation
- GitHub Actions workflows (`.github/workflows/validate.yml`)

Pre-commit validation prevents issues and maintains quality regardless of contribution source.