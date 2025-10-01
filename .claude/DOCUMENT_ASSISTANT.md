# Document Assistant Setup

## Important: Performance Note

Based on real-world usage, **long project instructions can cause performance issues** in Claude Desktop. Instead of loading extensive instructions here, we recommend using **simple copy-paste prompts** at the beginning of each chat session.

## Quick Start

1. **Start a new chat** in Claude Desktop
2. **Copy and paste** the appropriate prompt from `docs/prompts/doc-repo-related/`
3. Begin working with your documents

## Available Prompts

### Repository Access Instructions

Copy from: [`docs/prompts/doc-repo-related/repo-access-instructions.md`](../docs/prompts/doc-repo-related/repo-access-instructions.md)

This short prompt tells Claude how to access your GitHub repository via MCP.

**Important:** The `{{MCP_NAME}}` placeholder must be manually replaced with your actual MCP configuration name from Claude Desktop settings. The initialization workflow automatically replaces `{{GITHUB_ORG}}` and `{{REPO_NAME}}` with your repository information.

### Artifact Coaxing

Copy from: [`docs/prompts/doc-repo-related/coaxing.md`](../docs/prompts/doc-repo-related/coaxing.md)

Use this prompt to get Claude Desktop to open documents in the right pane as artifacts for easier viewing and editing.

## Customization for Your Organization

This is a **template repository**. When you create your repository from this template:

1. The initialization workflow will automatically personalize the prompts with your repository details
2. Update the prompts in `docs/prompts/doc-repo-related/` with any organization-specific guidance
3. Add additional prompts for common workflows specific to your team

## Why This Approach?

**What we discovered:**
- ✅ Short copy-paste prompts (~7 lines) work reliably
- ✅ Claude Desktop performs better with minimal project instructions
- ✅ Users have more control over each conversation's context
- ❌ Long project instructions (300+ lines) can cause Claude Desktop to hang
- ❌ Combining project instructions + project knowledge files adds complexity

**The working solution:**
Keep this file minimal and guide users to copy-paste simple prompts that provide just enough context for the specific task at hand.
