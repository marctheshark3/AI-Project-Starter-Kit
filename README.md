# AI Project Starter Kit

A comprehensive toolkit for efficiently starting and managing AI projects using LLMs for documentation generation, GitHub for project management, and Cursor for AI-assisted development.

## 🚀 Overview

This toolkit streamlines the AI project development process by providing:

1. **LLM-Powered Documentation Generation** - Templates and prompts for generating comprehensive PRDs, architecture diagrams, and Docker configurations
2. **GitHub Project Management** - Step-by-step guide for setting up and managing GitHub repositories
3. **AI-Assisted Development** - Guide for using Cursor with the @ tool to reference documentation during implementation
4. **Optional Blockchain Integration** - Tools for integrating with the Ergo blockchain ecosystem via Fleet SDK

## 📚 Contents

### System Prompts for LLMs
- **[Comprehensive AI Project Initialization System Prompt](system-prompt.md)** - A unified prompt for generating PRDs, diagrams, and Docker configurations
- **[Ergo Blockchain Integration System Prompt](ergo-blockchain-system-prompt.md)** - Extended prompt for optional Ergo blockchain integration with Fleet SDK
- **[Lovable.dev System Prompt](lovable/system-prompt.md)** - Template for generating web applications with Lovable.dev
- **[Bolt.new System Prompt](bolt/system-prompt)** - Template for generating web applications with Bolt.new
- **[Lovable.dev Ergo Integration Prompt](lovable/ergo-system-prompt.md)** - Specialized template for Ergo blockchain apps with Lovable.dev
- **[Bolt.new Ergo Integration Prompt](bolt/ergo-system-prompt)** - Specialized template for Ergo blockchain apps with Bolt.new

### Guides
- **[Cursor Guide](cursor/Cursor-Guide.md)** - How to use Cursor with the @ tool to reference your PRD during development
- **[GitHub Setup Guide](github/github-guide.md)** - Step-by-step instructions for setting up GitHub repositories and project boards
- **[Ergo Blockchain API Guide](cursor/Ergo-Blockchain-API-Guide-for-Cursormd)** - Documentation resources and integration patterns for Ergo blockchain development

### Visual Resources
- **AI Project Workflow Diagrams** - Mermaid diagrams included in the system prompts illustrating project components and workflows

## 🛠️ How to Use This Toolkit

### Step 1: Generate Project Documentation

1. Copy the [Comprehensive AI Project Initialization System Prompt](system-prompt.md) or the [Ergo Blockchain Integration System Prompt](ergo-blockchain-system-prompt.md) if your project includes blockchain functionality
2. Replace the placeholder sections with your specific project details
3. For the Ergo prompt, select which blockchain integration options you want (or none)
4. Submit to your preferred LLM (Claude, GPT-4, etc.)
5. Save the generated PRD, diagrams, and Docker configurations

### Step 2: Set Up GitHub Repository

1. Follow the [GitHub Setup Guide](github/github-guide.md) to create and configure your repository
2. Create a project board with appropriate columns
3. Set up issue templates and branch protection
4. Add your generated documentation to the repository

### Step 3: Set Up Cursor with Documentation

1. Install Cursor following the instructions in the [Cursor Guide](cursor/Cursor-Guide.md)
2. Import your project documentation
3. Add recommended documentation resources from the [Ergo Blockchain API Guide](cursor/Ergo-Blockchain-API-Guide-for-Cursormd) if using blockchain functionality
4. Use the @ tool to reference documentation during development

### Step 4: Develop and Deploy

1. Use Cursor with @ tool to reference PRD and other documentation
2. Implement features according to specifications
3. Create pull requests and track progress through GitHub
4. Use the generated Docker configurations for deployment

## 📋 Workflow Overview

1. **Project Inception**
   - Define project goals and requirements
   - Use the appropriate system prompt to generate comprehensive documentation
   - For projects with blockchain needs, select desired Ergo integration options

2. **Project Setup**
   - Create GitHub repository with appropriate structure
   - Configure project board with automation
   - Create milestones based on project phases

3. **Development**
   - Use Cursor with @ tool to reference PRD
   - Implement features according to specifications
   - Create pull requests and track progress
   - If applicable, implement Ergo blockchain integration

4. **Deployment**
   - Use generated Docker configurations
   - Deploy development and production environments
   - Set up CI/CD pipelines

## 📊 Project Management

The included guides and templates support:
- Task breakdown and organization
- Progress tracking through GitHub Projects
- Phase-based development with milestones
- Collaborative development with PR templates and review processes

## 🧩 Infrastructure Management

The system prompt generates:
- Development container specifications
- Production container with Nginx for custom DNS deployment
- Docker Compose configurations for local development
- Nginx configurations for production deployment

## 🔗 Ergo Blockchain Integration (Optional)

The [Ergo Blockchain Integration System Prompt](ergo-blockchain-system-prompt.md) provides:
- Fleet SDK implementation specifications
- Ergo node API interaction via the official REST API
- Multiple integration options:
  - Cryptocurrency payment processing via Nautilus wallet
  - Smart contract automation
  - Data verification and timestamping
  - Token creation for loyalty or rewards
- Security considerations for blockchain interactions
- Option to skip blockchain functionality entirely

The [Ergo Blockchain API Guide](cursor/Ergo-Blockchain-API-Guide-for-Cursormd) offers:
- Documentation resources to add to Cursor
- Common API endpoints reference
- Example integration patterns
- Best practices for Ergo development
- Step-by-step instructions for adding Ergo documentation to Cursor

## 🔄 Extensibility

This toolkit is designed to be extensible:
- Update the system prompts for different project types
- Modify the GitHub templates for your team's workflow
- Customize the Docker configurations for different tech stacks
- Choose which (if any) blockchain features to implement

## 📝 Contributing

Feel free to fork this repository and customize it for your specific needs. Pull requests for improvements and extensions are welcome!

## 📜 License

This toolkit is provided under the [MIT License](LICENSE) - see the LICENSE file for details.

---

Created with ❤️ to streamline AI project development. Happy building!