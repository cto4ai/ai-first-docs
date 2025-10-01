# {{COMPANY_NAME}} Documentation

Welcome to our AI-first documentation repository. This is your central hub for policies, procedures, technical documentation, and guides - powered by intelligent AI-assisted editing.

## 🤖 AI-First Workflow

This repository is designed for **AI-first documentation editing**. You can interact with your documentation using natural language through AI assistants that understand your organizational context.

### Quick Start Examples

**First, paste the repo access prompt** from `docs/prompts/doc-repo-related/repo-access-instructions.md`, then try:

- **"Show me the vacation policy"** → Use coaxing prompt to open as artifact → **"Update it to add 2 more PTO days"**
- **"List the policies in this repository"**
- **"Create a new expense policy for travel reimbursements"**
- **"Draft a security policy based on our compliance requirements"**

## 📁 Repository Structure

- **`docs/policies/`** - Company policies and governance documents
- **`docs/procedures/`** - Standard operating procedures and runbooks
- **`docs/architecture/`** - Technical documentation and system architecture
- **`docs/guides/`** - How-to guides and tutorials
- **`docs/references/`** - API documentation and reference materials
- **`docs/templates/`** - Document templates with AI instructions
- **`docs/prompts/`** - Copy-paste prompts for Claude Desktop workflows
- **`docs/cheatsheets/`** - Quick reference guides
- **`docs/examples/`** - Example content for testing and reference
- **`docs/assets/`** - Images and other media files

## 🚀 Getting Started

### For AI-Powered Editing (Claude Desktop)
1. **Start each chat** by pasting the prompt from `docs/prompts/doc-repo-related/repo-access-instructions.md`
2. **Ask your AI assistant** to help with documentation tasks
3. **Use artifacts** for visual editing (use the coaxing prompt if needed)
4. **Review AI-generated content** before it's committed to the repository

### For Traditional Editing
1. See [CONTRIBUTING.md](CONTRIBUTING.md) for documentation guidelines
2. Use templates in `docs/examples/` for new documents
3. Run `npm run validate` before submitting changes

## 🛠️ Local Development

```bash
# Install dependencies
npm install

# Validate your documentation
npm run validate

# Check spelling
npm run spell

# Check for broken links
npm run links

# Fix markdown formatting
npm run lint
```

## 📋 Quality Assurance

This repository uses automated validation to ensure high-quality documentation:

- **Markdown Linting** - Consistent formatting and structure
- **Spell Checking** - Catches typos and misspellings
- **Link Validation** - Ensures all links work correctly
- **AI Review Integration** - AI-assisted content validation
- **PR Reviews** - All changes reviewed before merge

## 🤖 AI Assistant Features

Your AI assistant can help with:

### Content Creation
- **Draft new policies** based on organizational requirements
- **Generate documentation** from existing templates
- **Create meeting notes** and procedure documentation

### Content Updates
- **Update existing documents** with new requirements
- **Revise policies** for compliance changes
- **Modernize documentation** language and structure

### Content Management
- **Find relevant documents** across the repository
- **Suggest related content** for cross-referencing
- **Identify outdated information** that needs updates

## 📖 AI-First Best Practices

### Working with AI
1. **Be specific** in your requests - "Update vacation policy to increase PTO by 2 days"
2. **Review all changes** before approving commits
3. **Use artifacts** for complex edits to see changes visually
4. **Provide context** about your organization when creating new content

### Quality Guidelines
- **AI generates, humans approve** - Always review AI-created content
- **Maintain consistency** with existing organizational style
- **Document AI usage** in commit messages when appropriate
- **Test workflows** with example content before making real changes

## 🤖 AI Assistant Setup

This repository uses a **copy-paste prompt approach** for Claude Desktop that's been proven to work reliably.

### Claude Desktop Integration

**Quick Setup (Recommended Workflow):**

1. **Start Each Chat Session** with the repository access prompt:
   - Open `docs/prompts/doc-repo-related/repo-access-instructions.md`
   - Replace `{{MCP_NAME}}` with your actual MCP configuration name from Claude Desktop settings
   - Copy and paste the personalized prompt at the start of your chat

2. **Working with Documents**:
   - Ask Claude to find or load documents: *"Show me the vacation policy"*
   - Use the coaxing prompt from `docs/prompts/doc-repo-related/coaxing.md` to open documents as artifacts
   - Make your edits with Claude's assistance

3. **Why This Approach?**
   - **Performance**: Short prompts (~7 lines) work reliably in Claude Desktop
   - **Flexibility**: Each chat session has just the context it needs
   - **User Control**: You decide what context to provide for each task

   *Previous approach: Long project instructions (300+ lines) caused Claude Desktop to hang*

### Dual AI Integration

This repository supports two complementary AI workflows:

- **CLAUDE.md**: Configuration for Claude Code integration (technical editing, development workflow)
- **`docs/prompts/`**: Copy-paste prompts for Claude Desktop (business user editing, artifact-based workflow)

Both approaches work together to provide comprehensive AI-first documentation support for different user types.

### Customization

The prompts in `docs/prompts/doc-repo-related/` can be customized for {{ORGANIZATION_NAME}}'s specific needs:
- Add organization-specific terminology
- Include compliance reminders
- Add workflow-specific instructions
- Create additional prompts for common tasks

## 📞 Support

- **Documentation Issues**: Create an issue in this repository
- **AI Integration Help**: See `.claude/DOCUMENT_ASSISTANT.md` and `docs/prompts/` for setup guidance
- **Template Questions**: {{DOCS_EMAIL}}
- **General Support**: {{SLACK_CHANNEL}}

## 🔒 Security & Compliance

### AI Data Handling
- AI assistants only access repository content you explicitly share
- No sensitive data is sent to AI services without your approval
- All AI interactions are logged in commit history with proper attribution

### Document Security
- Follow your organization's data classification guidelines
- Review AI-generated content for sensitive information
- Use branch protection and approval workflows for critical documents

---

**Need help getting started?** Ask your AI assistant: *"How do I create a new company policy using this repository?"*

*This repository uses AI-first documentation practices. See the [examples](docs/examples/) folder for reference content and templates.*