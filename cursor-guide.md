# Cursor Guide: Using the @ Tool with Your PRD

This guide provides practical instructions for using Cursor with the @ tool to reference your PRD and other project documents during development.

## What is Cursor?

Cursor is an AI-enhanced code editor built on top of VS Code that integrates AI assistance directly into your development workflow. One of its powerful features is the @ tool, which allows you to reference project documents in your prompts to the AI assistant.

## Installation and Setup

### 1. Install Cursor

1. Go to [cursor.sh](https://cursor.sh/) and download the installer for your operating system (Windows, macOS, or Linux)
2. Run the installer and follow the on-screen instructions
3. Launch Cursor after installation is complete

### 2. Organize Your Project Documents

For optimal use with the @ tool, organize your project documents as follows:

```
your-project/
├── docs/
│   ├── project-prd.md           # Your Product Requirements Document
│   ├── architecture-diagrams.md # Mermaid diagrams
│   └── docker-config.md         # Docker configuration
├── src/
│   └── ... (your source code)
├── README.md
└── ... (other project files)
```

### 3. Configure Cursor Settings (Optional)

For a better experience with the @ tool:

1. Open Cursor Settings (File > Preferences > Settings or Ctrl+,)
2. Search for "AI"
3. Enable relevant AI features (you may want to adjust token limits based on your documents' size)

## Using the @ Tool

### Basic Usage

1. Open any file in your project using Cursor
2. Press Ctrl+K (or your configured keybinding) to open the AI chat panel
3. In your prompt, type `@` followed by the document name you want to reference
4. Select the document from the dropdown that appears
5. Continue writing your prompt, using the referenced document for context

Example:
```
Using the requirements in @docs/project-prd.md, help me implement the user authentication feature.
```

### Referencing Specific Sections

To reference a specific section of a document:

1. Type `@` followed by the document name
2. Add `#` followed by the section header
3. The dropdown will show available sections - select the one you need

Example:
```
Using the user stories in @docs/project-prd.md#User Stories, create unit tests for the login functionality.
```

### Multiple Document References

You can reference multiple documents in a single prompt:

Example:
```
Based on the architecture in @docs/architecture-diagrams.md#System Architecture and the requirements in @docs/project-prd.md#Functional Requirements, implement the data access layer.
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

### Implementing Database Schema

```
According to the data requirements in @docs/project-prd.md#Data Model,
help me create the database schema with the appropriate tables and relationships.
```

## Best Practices

1. **Use Clear Document Names**: Name your documents descriptively for easier referencing
2. **Create Clear Section Headers**: Use distinct, hierarchical headers (##, ###) in your markdown documents
3. **Keep Documents Updated**: Ensure your PRD and other documents stay current as requirements evolve
4. **Be Specific in Prompts**: Reference exact sections rather than entire documents when possible
5. **Use with Version Control**: Keep your documents under version control so you can track changes

## Troubleshooting

### Document Not Found

If Cursor cannot find your referenced document:
- Check the document path is correct
- Ensure the document exists in your project directory
- Try using the full path from the project root

### Section Not Found

If a specific section cannot be found:
- Verify the section header exists exactly as referenced
- Make sure you're using the correct heading level (# vs ## vs ###)
- Check for any special characters or spaces in the heading

### Context Limitations

If Cursor seems to miss context from your documents:
- Your document might be too large for the context window
- Try referencing smaller, more specific sections
- Break complex prompts into multiple smaller prompts

### Cursor Not Responding or Slow

If Cursor becomes unresponsive when using @ references:
- The document might be too large for processing
- Close and reopen Cursor
- Update to the latest version of Cursor

## Advanced Tips

1. **Create Template Prompts**: Save commonly used prompts with @ references for repeated tasks
2. **Reference Code Files Too**: You can use the @ tool to reference code files, not just documentation
3. **Combine with AI Commands**: Use @ references alongside Cursor's other AI commands for powerful workflows
4. **Use with Multiple Models**: If you have access to different AI models in Cursor, you can experiment to see which handles @ references best for different tasks

By effectively using Cursor with the @ tool, you can significantly streamline your development process and ensure your implementation closely follows your project requirements.
