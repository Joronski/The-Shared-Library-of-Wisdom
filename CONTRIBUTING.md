# Contributing to [Project Name]

Thank you for your interest in contributing to our Android project! This guide will help you understand our development workflow using Android Studio and GitHub.

## Table of Contents

- [Development Setup](#development-setup)
- [Branching Strategy](#branching-strategy)
- [Commit Message Format](#commit-message-format)
- [Pull Request Requirements](#pull-request-requirements)
- [Code Review Process](#code-review-process)

## Development Setup

### Prerequisites

- Android Studio (latest stable version recommended)
- Git configured with your GitHub account
- JDK 11 or higher

### Getting Started

1. **Fork and Clone the Repository**
   ```bash
   git clone https://github.com/[organization]/[repository].git
   cd [repository]
   ```

2. **Open in Android Studio**
    - Open Android Studio
    - Select "Open an Existing Project"
    - Navigate to the cloned repository directory
    - Wait for Gradle sync to complete

3. **Configure Git in Android Studio**
    - Go to `File > Settings > Version Control > Git`
    - Ensure Git executable path is configured
    - Go to `File > Settings > Version Control > GitHub`
    - Add your GitHub account

## Branching Strategy

We follow a structured branching model to maintain code quality and organization.

### Branch Types

#### Main Branch
- **`main`**: Production-ready code only
- ⛔ **Direct pushes are STRICTLY PROHIBITED**
- All changes must go through Pull Requests
- Protected branch with required reviews

#### Development Branches

**Feature Branches**
- Format: `feature/[issue-number]-[brief-description]`
- Examples:
    - `feature/123-user-authentication`
    - `feature/456-add-dark-mode`
- Used for new features and enhancements

**Bugfix Branches**
- Format: `bugfix/[issue-number]-[brief-description]`
- Examples:
    - `bugfix/789-fix-login-crash`
    - `bugfix/101-resolve-memory-leak`
- Used for bug fixes

**Hotfix Branches**
- Format: `hotfix/[issue-number]-[brief-description]`
- Examples:
    - `hotfix/112-critical-security-patch`
- Used for urgent production fixes

**Refactor Branches**
- Format: `refactor/[brief-description]`
- Examples:
    - `refactor/repository-pattern`
    - `refactor/viewmodel-cleanup`
- Used for code refactoring without functional changes

### Creating a Branch in Android Studio

1. **Using the UI:**
    - Click on the Git branch indicator (bottom-right corner)
    - Select `+ New Branch`
    - Enter branch name following our convention
    - Check "Checkout branch" to switch to it

2. **Using the Terminal:**
   ```bash
   git checkout -b feature/123-your-feature-name
   ```

### Branch Lifecycle

1. Create branch from `main`
2. Make your changes
3. Keep branch updated with `main`
4. Submit Pull Request
5. Address review comments
6. Merge after approval
7. Delete branch after merge

## Commit Message Format

We follow the **Conventional Commits** specification for clear and structured commit history.

### Format Structure

```
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code refactoring without feature changes
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **build**: Build system or dependency changes
- **ci**: CI/CD configuration changes
- **chore**: Other changes that don't modify src or test files

### Scope

Optional but recommended. Indicates the module or component affected:
- `auth`
- `ui`
- `database`
- `api`
- `repository`
- `viewmodel`
- etc.

### Subject

- Use imperative mood: "add" not "added" or "adds"
- Don't capitalize first letter
- No period at the end
- Maximum 50 characters

### Examples

```
feat(auth): add biometric authentication support

fix(ui): resolve crash on profile image loading

docs(readme): update installation instructions

refactor(repository): implement repository pattern for data layer

test(auth): add unit tests for login validation

build(gradle): update kotlin version to 1.9.0
```

### Commit Message Body (Optional)

- Separate from subject with a blank line
- Wrap at 72 characters
- Explain what and why, not how

### Commit Message Footer (Optional)

- Reference issues: `Fixes #123` or `Closes #456`
- Breaking changes: `BREAKING CHANGE: description`

### Full Example

```
feat(auth): add social media login integration

- Integrate Google Sign-In
- Integrate Facebook Login
- Add OAuth2 authentication flow
- Update login UI to include social buttons

Closes #234
```

### Making Commits in Android Studio

1. **Stage Changes:**
    - Go to `Git > Commit` (or press `Ctrl+K` / `Cmd+K`)
    - Select files to commit from the Changes panel

2. **Write Commit Message:**
    - Enter your commit message following the format above
    - Use the commit message template if configured

3. **Commit:**
    - Click "Commit" (local only)
    - Or "Commit and Push" (commits and pushes to remote)

## Pull Request Requirements

All code changes must be submitted through Pull Requests (PRs). Direct pushes to `main` are disabled.

### Before Creating a PR

- [ ] Code compiles without errors
- [ ] All existing tests pass
- [ ] New tests added for new features
- [ ] Code follows project style guidelines (run code formatter)
- [ ] No lint warnings or errors
- [ ] Update documentation if needed
- [ ] Branch is up to date with `main`

### PR Title Format

Follow the same format as commit messages:

```
<type>(<scope>): <brief description>
```

Examples:
- `feat(auth): implement OAuth2 authentication`
- `fix(ui): resolve RecyclerView scroll issue`

### PR Description Template

```markdown
## Description
Brief description of changes made

## Type of Change
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] New feature (non-breaking change adding functionality)
- [ ] Breaking change (fix or feature causing existing functionality to not work as expected)
- [ ] Documentation update

## Related Issue
Fixes #[issue number]

## Screenshots (if applicable)
[Add screenshots for UI changes]

## Checklist
- [ ] My code follows the project's style guidelines
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
- [ ] Any dependent changes have been merged and published

## Testing Done
Describe the testing you performed

## Additional Notes
Any additional information reviewers should know
```

### Creating a PR in Android Studio

1. **Push Your Branch:**
    - Go to `Git > Push` (or press `Ctrl+Shift+K` / `Cmd+Shift+K`)
    - Review changes and push

2. **Create PR on GitHub:**
    - Android Studio will show a notification with "Create Pull Request" link
    - Or go to GitHub repository in browser
    - Click "Compare & pull request"
    - Fill in the PR template
    - Assign reviewers
    - Add appropriate labels
    - Submit the PR

### PR Review Requirements

- ✅ Minimum of **1 approval** from a code owner/maintainer
- ✅ All CI/CD checks must pass
- ✅ No merge conflicts with `main`
- ✅ All review comments addressed
- ✅ Code coverage maintained or improved

### Updating Your PR

When changes are requested:

1. Make the requested changes in your branch
2. Commit with descriptive message
3. Push to the same branch
4. PR will automatically update
5. Re-request review if needed

```bash
git add .
git commit -m "fix(auth): address review comments on token handling"
git push origin feature/123-your-feature
```

## Code Review Process

### For Contributors

1. Respond to all review comments
2. Mark conversations as resolved after addressing
3. Be open to feedback and suggestions
4. Ask for clarification if needed
5. Keep PRs small and focused (recommended: < 400 lines changed)

### For Reviewers

1. Review within 24-48 hours when possible
2. Provide constructive feedback
3. Approve when satisfied or request changes
4. Use GitHub's review features (Comment, Approve, Request Changes)

## Branch Protection Rules

The `main` branch has the following protections:

- ❌ No direct pushes allowed
- ✅ Pull Request required before merging
- ✅ At least 1 approval required
- ✅ Status checks must pass
- ✅ Branch must be up to date before merging
- ✅ Conversations must be resolved
- ✅ Force pushes disabled
- ✅ Deletions disabled

## Syncing Your Branch with Main

Keep your feature branch updated with the latest `main`:

### Using Android Studio

1. **Update Main:**
    - Switch to `main` branch
    - Go to `Git > Pull`

2. **Rebase Your Branch:**
    - Switch back to your feature branch
    - Go to `Git > Rebase`
    - Select `origin/main`
    - Resolve conflicts if any

### Using Terminal

```bash
git checkout main
git pull origin main
git checkout feature/123-your-feature
git rebase main
# Resolve conflicts if any
git push origin feature/123-your-feature --force-with-lease
```

## Getting Help

- Check existing issues and PRs
- Ask questions in PR comments
- Reach out to maintainers
- Review project documentation

## Code Style

- Follow [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)
- Use Android Studio's built-in formatter (`Ctrl+Alt+L` / `Cmd+Option+L`)
- Maximum line length: 120 characters
- Use meaningful variable and function names
- Write self-documenting code with appropriate comments

## Thank You!

Your contributions help make this project better. We appreciate your time and effort! 🎉

---

**Questions?** Feel free to open an issue for clarification on any contribution guidelines.