# {{COMPANY_NAME}} Documentation

AI-first documentation repository for {{COMPANY_NAME}}.

## Setup Complete

This repository is configured with:
- ✅ MCP docroot: `docs/`
- ✅ Claude Ecosystem ready
- ✅ Skills integration configured

## Prerequisites Installed

**Required**:
- [github-repos-manager-mcp](https://github.com/cto4ai/github-repos-manager-mcp) v3.0+
- [github-docs-skill](https://github.com/cto4ai/claude-skills)

**Setup Instructions**: See [Claude Ecosystem Setup](.github/DOCUMENTATION/claude-ecosystem-setup.md)

## Quick Start with Claude

### Using Claude Desktop (with MCP)
```
You: "Get the catalog of documents in this repository"
Claude: [Uses MCP to show all files in docs/]

You: "Create a new remote work policy"
Claude: [Uses MCP to create and commit file]
```

### Using Claude.ai (with Skills)
```
You: "Use the github-docs-skill to list policies"
Claude: [Uses Skill to access GitHub API]
```

## Repository Structure

All documentation lives in `/docs`:

- `policies/` - Company policies and governance
- `procedures/` - Standard operating procedures and runbooks
- `guides/` - How-to documentation and tutorials
- `architecture/` - Technical documentation and system design
- `references/` - API docs, specifications, references
- `skills/` - Available Claude Skills documentation
- `cheatsheets/` - Quick reference guides
- `prompts/` - Reusable AI prompts
- `templates/` - Document templates

## Using Templates

See `docs/templates/` for basic document structures:
- `policy-template.md` - For company policies
- `procedure-template.md` - For SOPs and runbooks
- `guide-template.md` - For how-to guides

## Ecosystem

**Primary**: Claude (Claude Desktop + Claude.ai)
**Planned**: OpenAI support

## Future Features

This repository is ready for future AI metadata enhancements.
See `.github/DOCUMENTATION/future-features/` for planned features.

## Support

- **MCP Issues**: [github-repos-manager-mcp issues](https://github.com/cto4ai/github-repos-manager-mcp/issues)
- **Skills Issues**: [claude-skills issues](https://github.com/cto4ai/claude-skills/issues)
- **This Repository**: Create an issue

## License

MIT
