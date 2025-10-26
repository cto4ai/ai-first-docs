# {{COMPANY_NAME}} Documentation

AI-first documentation repository for {{COMPANY_NAME}}.

## Setup Complete

This repository is configured with:
- ✅ MCP docroot: `docs/`
- ✅ Claude Desktop + MCP ready
- ✅ github-business-docs skill compatible

## Prerequisites

**Required:**
- **Claude Desktop** (latest version)
- **github-repos-manager-mcp** v3.0+ (MCP server)

**Optional but Recommended:**
- **github-business-docs skill** (provides business-friendly workflows using MCP)

## Quick Start with Claude Desktop

### 1. Install MCP Server

Install and configure **github-repos-manager-mcp** v3.0+ in Claude Desktop.

See [github-repos-manager-mcp](https://github.com/cto4ai/github-repos-manager-mcp) for installation.

### 2. Install Skill (Optional)

Install **github-business-docs** skill from the claude-skills repository.

The skill provides business-friendly workflows on top of the MCP tools.

### 3. Start Working

```
You: "Get the catalog of documents in this repository"
Claude: [Uses MCP to show all files in docs/]

You: "Create a new remote work policy"
Claude: [Uses MCP/skill to create and commit file]
```

## Repository Structure

All documentation lives in `/docs`:

- `policies/` - Company policies and governance
- `procedures/` - Standard operating procedures and runbooks
- `guides/` - How-to documentation and tutorials
- `architecture/` - Technical documentation and system design
- `references/` - API docs, specifications, references
- `skills/` - Claude Skills documentation
- `cheatsheets/` - Quick reference guides
- `prompts/` - Reusable AI prompts
- `templates/` - Document templates

## Using Templates

See `docs/templates/` for basic document structures:
- `policy-template.md` - For company policies
- `procedure-template.md` - For SOPs and runbooks
- `guide-template.md` - For how-to guides

## Architecture

**Claude Desktop** (your interface)
  ↓
**github-business-docs skill** (optional, business-friendly layer)
  ↓
**github-repos-manager-mcp** (MCP server with 7 tools)
  ↓
**GitHub API** (OAuth user attribution)
  ↓
**This Repository** (source of truth)

## Ecosystem

**Current**: Claude Desktop with MCP + optional skill
**Note**: Requires Claude Desktop - the skill uses MCP tools

## Future Features

This repository is ready for future AI metadata enhancements.

See `.github/DOCUMENTATION/ai-first-strategy.md` for the approach and philosophy.

## Support

- **MCP Issues**: [github-repos-manager-mcp issues](https://github.com/cto4ai/github-repos-manager-mcp/issues)
- **Skill Issues**: [claude-skills issues](https://github.com/cto4ai/claude-skills/issues)
- **This Repository**: Create an issue

## License

MIT
