# AI-First Documentation Strategy

**v2.0** - Minimal, Claude Ecosystem Native

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
github-repos-manager-mcp v3.0+ (Claude Desktop)
OR
github-docs-skill (Claude.ai)
  ↓
Claude (AI Interface)
  ↓
You (Natural Language)
```

**Simple. Clean. Works.**

## How It Works

### With Claude Desktop (MCP)
```
You: "Get the catalog of documents in this repository"
Claude: [Uses MCP to show all files in docs/]

You: "Create a new remote work policy"
Claude: [Uses MCP to create and commit file]
```

### With Claude.ai (Skills)
```
You: "Use the github-docs-skill to list policies"
Claude: [Uses Skill to access GitHub API]
```

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
- **Ecosystem:** Claude (primary), OpenAI (planned)
- **File types:** `.md`, `.txt`, `.pdf`

See `.mcp-config.json` for current configuration.

## Using This Repo

1. **Install prerequisites** (choose one):
   - Claude Desktop + github-repos-manager-mcp v3.0+
   - Claude.ai + github-docs-skill

2. **Ask Claude to work with docs:**
   - "Show me all policies"
   - "Create a new guide for [topic]"
   - "Update the [document name]"

3. **Review and approve**
   - AI generates or updates content
   - You review before committing
   - Git tracks all changes

## Future Enhancements

See `.github/DOCUMENTATION/future-features/` (if in template repo) for planned features like:
- AI metadata frontmatter
- Auto-summary generation
- Semantic markers

v2.0 is intentionally minimal - features added based on real usage.

## The Revolutionary Part

Documents become:
- **Queryable** through natural language
- **Maintainable** with AI assistance
- **Traceable** via Git history
- **Accessible** without navigation

This isn't just docs-as-code. It's **docs-as-intelligence**.

---

**Version:** 2.0
**Last Updated:** October 2025
**Philosophy:** Minimal by design, powerful by AI
