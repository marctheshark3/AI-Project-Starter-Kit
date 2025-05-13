# Cursor Guide: Using the @ Tool with Your PRD

This guide provides practical instructions for using Cursor with the @ tool to reference your PRD and other project documents during development.

## What is Cursor?

Cursor is an AI-enhanced code editor built on top of VS Code that integrates AI assistance directly into your development workflow. One of its powerful features is the @ symbol reference system, which allows you to incorporate various types of context into your AI interactions, including project documents, code snippets, and external documentation.

## Installation and Setup

### 1. Install Cursor

1. Go to [cursor.sh](https://cursor.sh/) and download the installer for your operating system (Windows, macOS, or Linux)
2. Run the installer and follow the on-screen instructions
3. Launch Cursor after installation is complete
4. You can import your VS Code settings and extensions during the initial setup

### 2. Organize Your Project Documents

For optimal use with the @ tool, organize your project documents as follows:

```
your-project/
├── docs/
│   ├── project-prd.md           # Your Product Requirements Document
│   ├── architecture-diagrams.md # Mermaid diagrams
│   ├── docker-config.md         # Docker configuration
│   └── ergo-integration.md      # Optional Ergo blockchain integration
├── src/
│   └── ... (your source code)
├── README.md
└── ... (other project files)
```

### 3. Configure Cursor Settings

To optimize your experience with @ references:

1. Open Cursor Settings (File > Preferences > Settings or Ctrl+,)
2. Search for "AI" to access AI-related settings
3. Under Features > Docs, you can manage your custom documentation
4. You can also create a `.cursorignore` file (similar to `.gitignore`) to exclude specific files or directories from indexing

## Understanding @ Symbol References in Cursor

The @ symbol in Cursor is a powerful tool for referencing different types of context in your AI interactions:

### Types of @ References

1. **@Files** - Reference any file in your project
2. **@Code** - Reference specific code snippets or symbols
3. **@Docs** - Reference external or custom documentation
4. **@Web** - Get up-to-date information from the internet
5. **@Codebase** - Reference your entire codebase

## Managing Documentation for Cursor

### Adding Custom Documentation

Cursor allows you to add custom documentation as context:

1. In any AI input (Chat, Cmd+K, or Composer), type `@Docs`
2. Select `> Add new doc`
3. Enter the URL of the documentation you want to add
4. Cursor will crawl and index the documentation
5. Make sure to add a trailing slash to the URL if you want to index all subpages

### Creating Effective Documentation

For documentation to work well with the @ tool, follow these guidelines:

1. **Use Markdown Format**: Write your documents in Markdown (.md) format for best results
2. **Clear Hierarchical Structure**: Use headings and subheadings (# for h1, ## for h2, etc.)
3. **Descriptive Section Titles**: Use unique, descriptive titles for sections that you'll want to reference
4. **Code Blocks**: Use triple backticks (```) for code examples with language specification
5. **Tables**: Use Markdown tables for structured data
6. **Links**: Include relevant links to external resources

Example of a well-structured document section:

```markdown
## Authentication System

### User Registration Flow

The system must implement a secure registration process with the following steps:

1. Email validation with verification code
2. Password strength requirements:
   - Minimum 8 characters
   - At least one uppercase letter
   - At least one number
   - At least one special character
```

### Importing Existing Documentation

To make existing documentation available for the @ tool:

1. **Copy External Documents**: Copy the content of external documents (like your LLM-generated PRD)
2. **Create Markdown Files**: Create new .md files in your project's docs directory
3. **Paste and Format**: Paste the content and ensure proper Markdown formatting
4. **Save in the Project**: Save the files in your project's directory structure
5. **Commit to Version Control**: If using Git, commit the docs to your repository

### Managing Your Documentation

You can manage your custom documentation in Cursor:

1. Go to Cursor Settings > Features > Docs
2. Here you can:
   - View all added documentation
   - Edit documentation sources
   - Delete documentation
   - Add new documentation sources

## Using the @ Tool

### Basic File References

1. Open any file in your project using Cursor
2. Press Ctrl+K (or Cmd+K on Mac) to open the AI command bar
3. In your prompt, type `@` to see a list of all files and code symbols in your project
4. Start typing the name of a file to filter the list
5. Select the file from the dropdown that appears
6. Continue writing your prompt, using the referenced file for context

Example:
```
Using the requirements in @docs/project-prd.md, help me implement the user authentication feature.
```

### Referencing Specific Code

To reference specific code in your project:

1. Select the code you want to reference
2. Press Ctrl+Shift+L (or Cmd+Shift+L on Mac) to add it to Chat
3. Or press Ctrl+Shift+K (or Cmd+Shift+K on Mac) to add it to a Cmd+K prompt
4. Alternatively, type `@Code` and select from available code symbols

### Referencing Specific Document Sections

To reference a specific section of a document:

1. Type `@` followed by the document name
2. Add `#` followed by the section header
3. The dropdown will show available sections - select the one you need

Example:
```
Using the user stories in @docs/project-prd.md#User Stories, create unit tests for the login functionality.
```

### Referencing External Documentation

To reference external documentation that you've added:

1. Type `@Docs` in your prompt
2. Select from the available documentation sources
3. You can also type part of the documentation name to filter the list

Example:
```
Based on @Docs React best practices, optimize this component for performance.
```

### Using Multiple References

You can reference multiple sources in a single prompt:

Example:
```
Based on the architecture in @docs/architecture-diagrams.md#System Architecture and the requirements in @docs/project-prd.md#Functional Requirements, implement the data access layer.
```

## AI-Assisted Documentation Creation

You can use Cursor's AI capabilities to help create or improve documentation:

### Creating New Documentation

1. Create a new .md file in your docs directory
2. Open the AI chat panel (Ctrl+K)
3. Ask the AI to help create documentation structure:

Example:
```
Help me create a documentation file for our API endpoints. Please include sections for authentication, user endpoints, product endpoints, and error handling.
```

### Enhancing Existing Documentation

1. Open an existing documentation file
2. Use the AI chat panel to suggest improvements:

Example:
```
Review this documentation and suggest improvements for clarity, completeness, and structure.
```

## Practical Examples

### Implementing Features Based on PRD

```
I need to implement the user registration feature as described in @docs/project-prd.md#User Registration. 
Please generate the necessary API endpoint and front-end components based on these requirements.
```

### Creating Docker Configuration Based on Infrastructure Requirements

```
Using the specifications in @docs/project-prd.md#Infrastructure Requirements, 
help me create a Dockerfile for the development environment.
```

### Writing Tests Based on User Stories

```
Based on the user stories in @docs/project-prd.md#User Stories that relate to the shopping cart, 
help me write unit tests to verify this functionality.
```

### Implementing Blockchain Features

```
According to @docs/ergo-integration.md#Wallet Connection, help me implement the wallet connection component
using Fleet SDK as specified.
```

### Using Codebase Context

```
@Codebase Are there any existing authentication functions I can reuse for the user registration feature?
```

## Best Practices

1. **Use Clear Document Names**: Name your documents descriptively for easier referencing
2. **Create Clear Section Headers**: Use distinct, hierarchical headers (##, ###) in your markdown documents
3. **Keep Documents Updated**: Ensure your PRD and other documents stay current as requirements evolve
4. **Be Specific in Prompts**: Reference exact sections rather than entire documents when possible
5. **Use with Version Control**: Keep your documents under version control so you can track changes
6. **Link Between Documents**: Use cross-references between documents for better context
7. **Include Examples**: Add code examples in your documentation to help the AI understand implementation patterns
8. **Create a .cursorignore File**: Exclude irrelevant files from indexing to focus the AI on what matters

## Troubleshooting

### Document Not Found

If Cursor cannot find your referenced document:
- Check the document path is correct
- Ensure the document exists in your project directory
- Try using the full path from the project root
- Verify that the file isn't excluded in your .cursorignore file

### Section Not Found

If a specific section cannot be found:
- Verify the section header exists exactly as referenced
- Make sure you're using the correct heading level (# vs ## vs ###)
- Check for any special characters or spaces in the heading
- Try typing more of the section name to help Cursor find it

### Symbol References Not Working

If code symbol references aren't working:
- Make sure your project has been fully indexed
- Try entering the "Code" context first before typing @
- Restart Cursor to trigger re-indexing
- Check your extensions for any conflicts

### Context Limitations

If Cursor seems to miss context from your documents:
- Your document might be too large for the context window
- Try referencing smaller, more specific sections
- Break complex prompts into multiple smaller prompts
- Use @Codebase instead of individual references for larger context needs

## Advanced Tips

1. **Create Template Prompts**: Save commonly used prompts with @ references for repeated tasks
2. **Use Keyboard Shortcuts**: Learn the shortcuts (Ctrl+Shift+L, Ctrl+Shift+K) for adding code context
3. **Combine Different @ References**: Mix file, code, docs, and web references for comprehensive context
4. **Link to External Resources**: Use @Web to incorporate up-to-date information from the internet
5. **Documentation-Driven Development**: Write documentation first, then reference it with the @ tool to implement features
6. **Team Collaboration**: Share custom documentation sources with your team for consistent context
7. **Use @Codebase for Complex Queries**: When you need to understand patterns across multiple files
8. **Regularly Update Documentation Sources**: Cursor will periodically re-index them to keep them current

By effectively using Cursor with the @ symbol reference system, you can significantly streamline your development process and ensure your implementation closely follows your project requirements.
