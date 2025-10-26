# AI-First Documentation Template

**Claude Ecosystem Template** - Minimal, production-ready documentation repository

[![Template](https://img.shields.io/badge/template-repository-green)](https://github.com/cto4ai/ai-first-docs/generate)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE.md)

## What This Template Provides

✅ Clean documentation structure
✅ MCP v3.0 compatible configuration
✅ Claude Skills integration ready
✅ Simple document templates
✅ Automatic initialization via GitHub Actions

## Prerequisites

- [github-repos-manager-mcp](https://github.com/cto4ai/github-repos-manager-mcp) (v3.0+)
- [github-docs-skill](https://github.com/cto4ai/claude-skills) from claude-skills repo
- GitHub account with repository access

## Quick Start

1. **Click "Use this template"** button above
2. **GitHub Actions automatically**:
   - Replaces template variables with your repo info
   - Creates `.mcp-config.json` from template
   - Swaps this README with your customized README
   - Creates setup issue with next steps
3. **Follow setup issue** to configure MCP and Skills
4. **Start documenting** with AI assistance

## What Happens on Initialization

- ✅ `.mcp-config.json` created with docroot = `docs`
- ✅ Template variables replaced ({{REPO_NAME}}, {{COMPANY_NAME}}, etc.)
- ✅ This README replaced with your repo's README
- ✅ Setup issue created with personalized instructions
- ✅ Init workflow self-deletes

## Ecosystem Support

**Current**: Claude (Claude Desktop + Claude Skills)
**Planned**: OpenAI support (future)

## What's NOT Included

This is a minimal template. No validation tooling, no build processes.
Trust AI + human review. Add your own tooling if needed.

## Future Features

See `.github/DOCUMENTATION/future-features/` for planned enhancements:
- AI metadata frontmatter
- Auto-summary generation
- Semantic markers
- Enhanced catalog integration

## Learn More

- [Setup Guide](.github/DOCUMENTATION/claude-ecosystem-setup.md)
- [AI-First Strategy](.github/DOCUMENTATION/ai-first-strategy.md)
- [Future Features](.github/DOCUMENTATION/future-features/)

## License

MIT
