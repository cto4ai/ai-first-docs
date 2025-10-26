# AI-First Documentation Strategy

**v2.0** - Minimal, Claude Desktop Native

## The Core Idea

Documentation isn't something you navigate - it's something you query through AI, which reads, synthesizes, and updates it for you.

## Why AI-First?

Traditional documentation requires:
- Navigation systems (complex sites, menus, search)
- Build processes (static site generators)
- Manual updates (humans editing markdown)
- Finding things (browsing, clicking, searching)

**AI-first flips this:**
- AI reads Git repos directly (no site needed)
- AI understands relationships (no navigation needed)
- AI helps maintain content (assisted updates)
- Natural language replaces clicking

## Architecture (v2.0)

```
Git Repository (Source of Truth)
  ↓
.mcp-config.json (Configuration)
  ↓
github-repos-manager-mcp v3.0+ (MCP server, handles OAuth)
  ↓
github-business-docs skill (optional, business-friendly layer)
  ↓
Claude Desktop (AI Interface)
  ↓
You (Natural Language)
```

**Simple. Clean. Works.**

## How It Works

### With Claude Desktop + MCP

```
You: "Get the catalog of documents in this repository"
Claude: [Uses MCP tools to show all files in docs/]

You: "Create a new remote work policy"
Claude: [Uses MCP tools to create and commit file with your attribution]
```

### Why Claude Desktop Only?

**OAuth Requirement:** GitHub integration requires OAuth authentication to attribute commits to individual users (not a bot account).

**Current Reality:**
- ✅ **Claude Desktop**: MCP server runs locally, OAuth works
- ❌ **Claude.ai**: Can't run local OAuth flow in web environment
- ❌ **Direct API approach**: Failed - couldn't solve OAuth in code execution

**Future:** If Anthropic adds native OAuth support to Claude.ai, this could expand.

## Components

### Required

**github-repos-manager-mcp** v3.0+
- MCP server that runs locally
- Handles OAuth authentication with GitHub
- Provides 7 tools for document management
- 93% context reduction vs full GitHub MCPs

### Optional but Recommended

**github-business-docs skill**
- Uses the MCP tools
- Provides business-friendly workflows
- Non-technical user language
- Document templates and helpers

## What Makes This Minimal (v2.0)

**What we have:**
- Clean directory structure (`docs/`)
- MCP configuration (`.mcp-config.json`)
- Simple markdown templates
- Git for version control

**What we don't have:**
- npm dependencies
- Build processes
- Validation tooling
- Complex metadata

**Trust:** AI + human review

## Repository Configuration

This repository is configured with:
- **Docroot:** `docs/` (all documentation here)
- **Platform:** Claude Desktop with MCP
- **File types:** `.md`, `.txt`, `.pdf`

See `.mcp-config.json` for current configuration.

## Using This Repo

1. **Install prerequisites:**
   - Claude Desktop (latest version)
   - github-repos-manager-mcp v3.0+
   - github-business-docs skill (optional)

2. **Ask Claude to work with docs:**
   - "Show me all policies"
   - "Create a new guide for [topic]"
   - "Update the [document name]"

3. **Review and approve:**
   - AI generates or updates content
   - You review before committing
   - Git tracks all changes with your name

## Future Enhancements

Planned features (see template repo for details):
- AI metadata frontmatter
- Auto-summary generation
- Semantic markers
- Multi-platform support (as OAuth solutions emerge)

v2.0 is intentionally minimal - features added based on real usage.

## The Revolutionary Part

Documents become:
- **Queryable** through natural language
- **Maintainable** with AI assistance
- **Traceable** via Git history (with your attribution!)
- **Accessible** without navigation

This isn't just docs-as-code. It's **docs-as-intelligence**.

---

**Version:** 2.0
**Last Updated:** October 2025
**Platform:** Claude Desktop + MCP
**Philosophy:** Minimal by design, powerful by AI
