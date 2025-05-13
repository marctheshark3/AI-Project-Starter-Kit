# GitHub Project Setup Guide

This guide provides practical, step-by-step instructions for setting up a GitHub repository and project for your AI application.

## Initial Repository Setup

### 1. Create a New Repository

1. Go to [GitHub.com](https://github.com) and sign in to your account
2. Click on the "+" icon in the top-right corner and select "New repository"
3. Fill in the repository details:
   - **Repository name**: Choose a clear, descriptive name (e.g., `ai-project-name`)
   - **Description**: Add a brief description of your project
   - **Visibility**: Choose between Public or Private
   - **Initialize this repository with**: Check the following options:
     - README file
     - .gitignore (select the template that matches your tech stack, e.g., Python, Node.js)
     - License (choose appropriate license for your project)
4. Click "Create repository"

### 2. Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/yourusername/ai-project-name.git
cd ai-project-name
```

### 3. Set Up Repository Structure

Create the following directory structure:

```bash
mkdir -p docs src tests .github/workflows .github/ISSUE_TEMPLATE .github/PULL_REQUEST_TEMPLATE
```

This creates:
- `docs/`: For your PRD and other documentation
- `src/`: For your source code
- `tests/`: For test files
- `.github/`: For GitHub-specific configurations

### 4. Add Essential Files

#### README.md

Edit the README.md to include:

```markdown
# Project Name

Brief description of your project.

## Features

- Feature 1
- Feature 2
- Feature 3

## Getting Started

### Prerequisites

- Requirement 1
- Requirement 2

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/ai-project-name.git
   ```

2. Install dependencies
   ```bash
   # Add installation commands
   ```

## Usage

Instructions on how to use your project.

## Development

Instructions for setting up the development environment.

## Deployment

Instructions for deployment.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to contribute to this project.

## License

This project is licensed under the [LICENSE NAME] - see the [LICENSE](LICENSE) file for details.
```

#### CONTRIBUTING.md

Create a CONTRIBUTING.md file with:

```markdown
# Contributing Guidelines

Thank you for your interest in contributing to this project! Here's how you can help.

## Code of Conduct

Please make sure to read and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## How to Contribute

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes
4. Commit your changes: `git commit -m 'Add some feature'`
5. Push to the branch: `git push origin feature/your-feature-name`
6. Submit a pull request

## Commit Message Guidelines

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

## Pull Request Process

1. Update the README.md with details of changes if applicable
2. Update the documentation with details of changes if applicable
3. The PR should work for all supported platforms
4. The PR must pass all CI/CD checks
5. At least one code review approval is required for merging

## Issue Process

1. Use the issue template provided
2. Be as detailed as possible
3. Include steps to reproduce if reporting a bug
4. Include expected and actual behavior
```

#### Issue Templates

Create `.github/ISSUE_TEMPLATE/bug_report.md`:

```markdown
---
name: Bug report
about: Create a report to help us improve
title: '[BUG] '
labels: bug
assignees: ''
---

**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Environment:**
 - OS: [e.g., iOS]
 - Browser/Version: [e.g., chrome, safari]
 - Project Version: [e.g., 1.0.0]

**Additional context**
Add any other context about the problem here.
```

Create `.github/ISSUE_TEMPLATE/feature_request.md`:

```markdown
---
name: Feature request
about: Suggest an idea for this project
title: '[FEATURE] '
labels: enhancement
assignees: ''
---

**Is your feature request related to a problem? Please describe.**
A clear and concise description of what the problem is.

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.
```

#### Pull Request Template

Create `.github/PULL_REQUEST_TEMPLATE/pull_request_template.md`:

```markdown
## Description
Please provide a summary of the changes and the related issue. 

Fixes # (issue)

## Type of change
Please check the options that are relevant.

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## How Has This Been Tested?
Please describe the tests that you ran to verify your changes.

- [ ] Test A
- [ ] Test B

## Checklist:
- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
```

### 5. Configure Branch Protection

1. Go to your repository on GitHub
2. Click on "Settings" > "Branches"
3. Under "Branch protection rules", click "Add rule"
4. In "Branch name pattern", enter "main" (or your default branch name)
5. Check the following options:
   - Require pull request reviews before merging
   - Require status checks to pass before merging
   - Require branches to be up to date before merging
   - Include administrators
6. Click "Create" to save the rule

## Setting Up GitHub Projects

### 1. Create a New Project

1. Go to your repository on GitHub
2. Click on the "Projects" tab
3. Click "Create a project"
4. Select "Board" template
5. Enter a name for your project (e.g., "AI Project Development")
6. Click "Create project"

### 2. Configure Project Columns

Your project board will have default columns (To do, In progress, Done). You can customize these:

1. To add a new column, click "+ Add column" at the right side of the board
2. Enter column name (e.g., "Backlog", "In Review", "Blocked")
3. Click "Add column"
4. To reorder columns, click and drag them to your desired position

### 3. Set Up Project Automation

1. For each column, click the "..." menu at the top right
2. Select "Manage automation"
3. Configure automation rules:
   - **To do**: Automatically move newly added items and reopened items here
   - **In progress**: Automatically move items when they are assigned to someone or when a pull request is opened
   - **In review**: Automatically move items when a pull request is ready for review
   - **Done**: Automatically move items when they are closed or when a pull request is merged

### 4. Create Issues from Your PRD

Now, create issues based on your PRD document:

1. Go to the "Issues" tab in your repository
2. Click "New issue"
3. Select the appropriate issue template
4. For each task or feature in your PRD:
   - Create a new issue with a clear title
   - Include detailed description, acceptance criteria, and references to the PRD
   - Add appropriate labels (e.g., "enhancement", "bug", "documentation")
   - Assign to team members if applicable
   - Add to your project board
   - Link to a milestone if applicable

### 5. Set Up Milestones

1. Go to the "Issues" tab
2. Click "Milestones"
3. Click "New milestone"
4. Create milestones based on your project phases:
   - Title: Phase name (e.g., "Phase 1: Discovery and Planning")
   - Due date: Target completion date
   - Description: Phase objectives and deliverables
5. Repeat for each project phase

## Implementing GitHub Actions (CI/CD)

### 1. Create Basic CI Workflow

Create a file `.github/workflows/ci.yml`:

```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up environment
      # Add steps to set up your project environment
      run: echo "Setting up environment"
      
    - name: Install dependencies
      # Add steps to install dependencies
      run: echo "Installing dependencies"
      
    - name: Run tests
      # Add steps to run tests
      run: echo "Running tests"
      
    - name: Lint code
      # Add steps to lint your code
      run: echo "Linting code"
```

### 2. Create Docker Build Workflow

If your project uses Docker, create `.github/workflows/docker-build.yml`:

```yaml
name: Docker Build

on:
  push:
    branches: [ main ]
    tags: [ 'v*.*.*' ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Set up Docker Buildx
      uses: docker/setup-buildx-action@v2
      
    - name: Login to DockerHub
      if: github.event_name != 'pull_request'
      uses: docker/login-action@v2
      with:
        username: ${{ secrets.DOCKERHUB_USERNAME }}
        password: ${{ secrets.DOCKERHUB_TOKEN }}
      
    - name: Build and push
      uses: docker/build-push-action@v4
      with:
        context: .
        file: ./Dockerfile
        push: ${{ github.event_name != 'pull_request' }}
        tags: ${{ steps.meta.outputs.tags }}
        labels: ${{ steps.meta.outputs.labels }}
```

## GitHub Workflow Best Practices

### 1. Branching Strategy

Implement a clear branching strategy:

```
main           - Production-ready code
└── develop    - Integration branch for features
    ├── feature/feature-name - New features
    ├── bugfix/bug-name     - Bug fixes
    └── hotfix/fix-name     - Critical fixes for production
```

### 2. Commit Message Format

Follow a consistent commit message format:

```
<type>(<scope>): <subject>

<body>

<footer>
```

Where:
- **type**: feat (feature), fix, docs, style, refactor, test, chore
- **scope**: component or file affected
- **subject**: short description in present tense
- **body**: detailed explanation if needed
- **footer**: reference issues, PRs, breaking changes

Example:
```
feat(auth): implement user authentication

- Add login form component
- Implement JWT token handling
- Add session management

Closes #123
```

### 3. Code Review Process

1. Author creates a pull request from their feature branch to develop
2. CI/CD runs automated tests and checks
3. Assigned reviewers review the code:
   - Check for coding standards compliance
   - Verify functionality meets requirements
   - Look for potential bugs or edge cases
   - Ensure sufficient test coverage
4. Author addresses feedback
5. Once approved, merge the pull request
6. Delete the feature branch after merging

### 4. Release Process

1. Create a release branch from develop when ready to release
2. Perform final testing in the release branch
3. Create a pull request from release branch to main
4. Once approved and merged:
   - Tag the release with appropriate version (e.g., v1.0.0)
   - Create a GitHub Release with release notes
   - Merge changes back to develop

## Adding Project Documentation to GitHub

1. Store your PRD and other documentation in the `docs/` directory
2. Add your PRD as `docs/project-prd.md`
3. Add your architecture diagrams as `docs/architecture-diagrams.md`
4. Add your Docker configuration as `docs/docker-configuration.md`
5. Update the README.md to link to these documents

Commit and push your documentation:

```bash
git add docs/
git commit -m "docs: add project documentation"
git push origin main
```

## Maintaining Your GitHub Project

### 1. Regular Maintenance

- Review and triage new issues regularly
- Update project board status
- Close completed issues
- Update documentation as the project evolves

### 2. Tracking Progress

- Use project board views to visualize progress
- Check milestone completion rates
- Review open issues and pull requests regularly

### 3. Generating Reports

- Use GitHub Insights to track contributions and activity
- Review pull request statistics
- Monitor issues closed vs. opened rates

## Conclusion

This guide has provided a step-by-step process for setting up a GitHub repository and project for your AI application. By following these instructions, you can create a well-organized, efficient, and collaborative development environment.

Remember to adapt these guidelines to fit your specific project needs and team workflow. As your project grows, you may need to adjust your GitHub configuration and processes.
