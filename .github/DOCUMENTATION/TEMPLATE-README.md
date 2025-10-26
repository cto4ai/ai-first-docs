# .github/DOCUMENTATION Directory

**For Template Developers**

This directory contains two types of documentation:

## Template Development Docs (NOT Copied to Generated Repos)

These files are for people maintaining the ai-first-docs template:

- **`V2.0-RESTRUCTURE-PLAN.md`** - v2.0 restructure planning and implementation notes
- **`future-features/`** - Planned features not yet implemented
- **`TEMPLATE-README.md`** - This file

These are automatically removed from generated repos by the init workflow.

## User-Facing Docs (Copied to Generated Repos)

These files are included in repositories created from this template:

- **`ai-first-strategy.md`** - Short explanation of AI-first documentation approach (v2.0 focused)
- **`claude-ecosystem-setup.md`** - Setup guide for MCP and Skills (when created)

## Init Workflow Behavior

The `.github/workflows/init-template.yml` workflow:

1. **Keeps:** User-facing docs (ai-first-strategy.md, etc.)
2. **Deletes:** Template dev docs (V2.0-RESTRUCTURE-PLAN.md, future-features/, this file)
3. **Deletes:** Issue/PR templates (not needed in generated repos)

## Adding New Docs

**For generated repos:** Create docs with clear, user-focused names. Init workflow will keep them.

**For template only:** Prefix with `TEMPLATE-` or add to list of files to delete in init workflow.
