# Contributing to Avenida

Thank you for your interest in contributing to Avenida! This document provides guidelines and information about contributing to our projects.

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## Getting Started

### Development Setup

1. Clone the [workspace repository](https://github.com/avenidaeng/avenidaeng)
2. Follow the setup instructions in the README
3. Clone the specific project you want to contribute to

### Project Structure

Avenida is organized as multiple repositories:

- **avenida-web** — Main web application (Next.js)
- **avenida-site** — Marketing website (Next.js)
- **avenida-packages** — Shared TypeScript packages
- **avenida-extension** — Browser extension (WXT)
- **avenida-infra** — Database migrations and infrastructure

## How to Contribute

### Reporting Bugs

1. Check if the issue already exists in the relevant repository
2. Use the **Bug Report** issue template
3. Include:
   - Clear description of the bug
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable
   - Environment details (browser, OS, etc.)

### Suggesting Features

1. Use the **Feature Request** issue template
2. Describe the problem you're trying to solve
3. Explain your proposed solution
4. Consider alternatives you've thought about

### Pull Requests

1. **Fork** the repository
2. **Create a branch** from `main`:
   ```bash
   git checkout -b feat/your-feature-name
   ```
3. **Make your changes** following our coding standards
4. **Write tests** for new functionality
5. **Commit** using [Conventional Commits](https://www.conventionalcommits.org/):
   ```bash
   git commit -m "feat(scope): add new feature"
   ```
6. **Push** and create a Pull Request

### Branch Naming

Use descriptive branch names with prefixes:

- `feat/` — New features
- `fix/` — Bug fixes
- `docs/` — Documentation changes
- `refactor/` — Code refactoring
- `test/` — Test additions/changes
- `chore/` — Maintenance tasks

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**Types**: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`

**Examples**:

```
feat(wishlist): add sharing functionality
fix(extension): handle null price in extraction
docs(readme): update setup instructions
```

## Coding Standards

### General

- Write clear, self-documenting code
- Add JSDoc comments for public APIs
- Follow existing patterns in the codebase
- Keep functions small and focused

### TypeScript

- Use strict mode
- Prefer `type` for object shapes
- Validate external inputs with Zod
- Avoid `any` — use `unknown` and narrow

### Testing

- Write tests for new features
- Add regression tests for bug fixes
- Keep tests deterministic

### Pull Request Checklist

- [ ] Code follows project style guidelines
- [ ] Tests pass locally
- [ ] New code has appropriate test coverage
- [ ] Documentation updated if needed
- [ ] Commit messages follow Conventional Commits
- [ ] PR description explains the changes

## Review Process

1. A maintainer will review your PR
2. Address any feedback or requested changes
3. Once approved, a maintainer will merge your PR

## Questions?

- Open a [Discussion](https://github.com/orgs/avenidaeng/discussions) for questions
- Check existing issues and discussions first
- Reach out at engineering@avenida.so

Thank you for contributing! 🎉
