# Contributing to claude-code-test

Thank you for your interest in contributing! This document provides guidelines for contributing to this project.

## Branch Strategy

We follow the **Git Flow** branching model:

### Main Branches
- **`main`** - Production-ready code. Only merge from `release` or `hotfix` branches.
- **`develop`** - Main development branch. All features are merged here first.

### Supporting Branches
- **`feature/*`** - New features (branch from `develop`, merge to `develop`)
- **`release/*`** - Release preparation (branch from `develop`, merge to `main` and `develop`)
- **`hotfix/*`** - Emergency fixes (branch from `main`, merge to `main` and `develop`)

## How to Contribute

### 1. Fork and Clone
```bash
git clone https://github.com/Makoto38710/claude-code-test.git
cd claude-code-test
```

### 2. Create a Feature Branch
```bash
git checkout develop
git pull origin develop
git checkout -b feature/your-feature-name
```

### 3. Make Your Changes
- Write clean, readable code
- Follow existing code style
- Add tests for new features
- Update documentation as needed

### 4. Commit Your Changes
```bash
git add .
git commit -m "feat: add your feature description"
```

#### Commit Message Format
We follow conventional commits:
- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation changes
- `style:` - Code style changes (formatting, etc.)
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

### 5. Push and Create Pull Request
```bash
git push origin feature/your-feature-name
```

Then create a Pull Request to the `develop` branch.

## Pull Request Guidelines

- Fill out the PR template completely
- Ensure all tests pass
- Update documentation if needed
- Request review from maintainers
- Address review feedback promptly

## Code Review Process

1. At least one maintainer must approve the PR
2. All CI checks must pass
3. No merge conflicts
4. PR will be merged by a maintainer

## Questions?

Feel free to open an issue or discussion if you have any questions!
