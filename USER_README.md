# {{COMPANY_NAME}} Documentation

Welcome to our AI-first documentation repository. This is your central hub for policies, procedures, technical documentation, and guides - powered by intelligent AI-assisted editing.

## 🤖 AI-First Workflow

This repository is designed for **AI-first documentation editing**. You can interact with your documentation using natural language through AI assistants that understand your organizational context.

### Quick Start Examples
- **"Load the vacation policy into an artifact for editing"**
- **"Update the remote work policy to allow 4-day work weeks"**
- **"Create a new expense policy for travel reimbursements"**
- **"Draft a security policy based on our compliance requirements"**

## 📁 Repository Structure

- **`docs/policies/`** - Company policies and governance documents
- **`docs/procedures/`** - Standard operating procedures and runbooks
- **`docs/architecture/`** - Technical documentation and system architecture
- **`docs/examples/`** - Example content and templates for reference

## 🚀 Getting Started

### For AI-Powered Editing
1. **Ask your AI assistant** to help with documentation tasks
2. **Use artifacts** for visual editing before committing changes
3. **Review AI-generated content** before it's committed to the repository
4. **AI instructions** are configured in `.claude/DOCUMENT_ASSISTANT.md`

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

This repository includes pre-configured AI assistant instructions designed for your organization's documentation workflow.

### Claude Desktop Integration

**Set up your Documentation Assistant:**

1. **Copy Master Instructions**
   - Open `.claude/DOCUMENT_ASSISTANT.md` in this repository
   - Copy the entire content to your Claude Desktop Project instructions
   - These instructions are already personalized for {{ORGANIZATION_NAME}}

2. **For Claude Team Users**
   - Create a shared "{{ORGANIZATION_NAME}} Documentation" Project
   - Import the instructions to enable team-wide consistent AI assistance
   - All team members can then use the same documentation assistant behavior

3. **Test Your Setup**
   ```
   Try asking: "Load the vacation policy into an artifact for editing"
   Try asking: "Create a new remote work policy for our company"
   ```

### Dual AI Integration

This repository supports two complementary AI workflows:

- **CLAUDE.md**: Configuration for Claude Code integration (technical editing, development workflow)
- **DOCUMENT_ASSISTANT.md**: Instructions for Claude Desktop Projects (business user editing, artifact-based workflow)

Both files work together to provide comprehensive AI-first documentation support.

### Customization Options

The assistant instructions can be customized for {{ORGANIZATION_NAME}}'s specific needs:
- Modify tone and language preferences
- Update approval workflow requirements
- Add compliance and regulatory constraints
- Include organization-specific terminology

## 📞 Support

- **Documentation Issues**: Create an issue in this repository
- **AI Integration Help**: See `.claude/DOCUMENT_ASSISTANT.md` for AI-specific guidance
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