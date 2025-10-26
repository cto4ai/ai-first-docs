# Future Features

This directory documents planned enhancements for AI-first documentation workflows.

**Status**: Documented concepts, not yet implemented in v2.0

## Planned Features

### 1. AI Metadata Frontmatter
**File**: [ai-metadata-frontmatter.md](ai-metadata-frontmatter.md)
**Status**: Design phase
**Target**: v2.1 or v3.0

Full YAML frontmatter specification for AI-native document management:
- `ai_metadata` section with auto-summary capability
- `ai_instructions` for behavior guidance
- `ai_edit_constraints` for safety and compliance
- Schema versioning for evolution
- Document lifecycle tracking

### 2. Auto-Summary Generation
**File**: [auto-summary-generation.md](auto-summary-generation.md)
**Status**: Design phase
**Requires**: MCP v3.1+

Automatic document summarization on push:
- LLM-generated 1-2 sentence summaries
- Updates frontmatter automatically
- Exposed via MCP catalog API
- Searchable and filterable

### 3. Semantic Markers
**File**: [semantic-markers.md](semantic-markers.md)
**Status**: Design phase
**Target**: v2.1

HTML comment-based AI directives:
- `<!-- AI-READONLY -->` - Never modify these sections
- `<!-- AI-UPDATEABLE -->` - Safe to update with constraints
- `<!-- AI-CONTEXT -->` - Invisible guidance for AI
- `<!-- AI-AUTO -->` - Auto-updated fields (dates, summaries)

### 4. Metadata Catalog Integration
**File**: [metadata-catalog-integration.md](metadata-catalog-integration.md)
**Status**: Design phase
**Requires**: MCP v3.1+

Enhanced `get_repository_catalog` with metadata:
- Document titles, summaries, status in catalog response
- Filter/search by metadata fields
- Performance-optimized catalog responses
- Reduced token usage

## Why Document Before Implementation?

We're separating planning from implementation to:
1. **Keep v2.0 simple** - Ship minimal, working template now
2. **Gather feedback** - Learn what users actually need
3. **Plan thoughtfully** - Design features properly before coding
4. **Avoid complexity** - Don't over-engineer too early

## Contributing Ideas

Have ideas for future features?
- Create an issue in this repository
- Add details to these planning documents
- Share use cases and examples

## Implementation Timeline

Features will be prioritized based on:
- **MCP server capabilities** (some require MCP v3.1+)
- **User feedback and demand**
- **Ecosystem evolution** (Claude, OpenAI)
- **Real-world usage patterns**

## Dependencies

| Feature | Depends On |
|---------|------------|
| Auto-summary | MCP v3.1+ server-side LLM integration |
| Metadata catalog | MCP v3.1+ catalog enhancement |
| AI frontmatter | Template updates (can ship independently) |
| Semantic markers | Template updates (can ship independently) |

## Questions?

See individual feature documents for detailed specifications, or create an issue to discuss.

---

**v2.0**: Simple templates, clean structure, MCP docroot support
**v2.1+**: Gradually add features from this directory as they mature
