# Contributing Guide

Thank you for considering contributing to the FlyAI Skill project! 🎉

## 📝 How to Contribute

### Reporting Bugs

If you find a bug, please create an issue with the following information:

1. **Clear title**: Briefly describe the problem
2. **Steps to reproduce**: Detailed instructions on how to reproduce the issue
3. **Expected behavior**: Describe what you think should happen
4. **Actual behavior**: Describe what actually happened
5. **Environment info**: 
   - Node.js version
   - flyai-cli version
   - Operating system

Example:

```markdown
### Description
Price filter parameter not working when searching hotels

### Steps to Reproduce
1. Run `flyai search-hotels --dest-name "Hangzhou" --max-price 500`
2. Results include hotels with prices exceeding 500

### Expected Behavior
Only return hotels with prices below 500 yuan

### Actual Behavior
Returned a hotel priced at 618 yuan

### Environment
- Node.js: v18.16.0
- flyai-cli: v1.0.10
- macOS: 13.4
```

### Suggesting New Features

New feature suggestions are welcome! Please create an issue explaining:

1. **Feature description**: Clearly describe the feature you want
2. **Use case**: Explain the use case for this feature
3. **Implementation suggestions**: Share if you have implementation ideas
4. **Alternatives**: Have you considered other solutions?

### Submitting Code

#### 1. Fork the Repository

Click the "Fork" button in the upper right corner of the GitHub page

#### 2. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/flyai-skill.git
cd flyai-skill
```

#### 3. Create a Branch

```bash
# Feature development
git checkout -b feature/your-feature-name

# Bug fix
git checkout -b fix/bug-fix-description

# Documentation improvement
git checkout -b docs/documentation-improvement
```

Branch naming conventions:
- `feature/*`: New features
- `fix/*`: Bug fixes
- `docs/*`: Documentation updates
- `refactor/*`: Code refactoring
- `test/*`: Test related
- `chore/*`: Build/tool related

#### 4. Make Your Changes

Ensure your changes:
- ✅ Follow existing code style
- ✅ Add necessary comments
- ✅ Update relevant documentation
- ✅ Pass all tests (if applicable)

#### 5. Commit Changes

```bash
git add .
git commit -m "feat: add new hotel filter option"
```

Commit message conventions ([Conventional Commits](https://www.conventionalcommits.org/)):

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation update
- `style`: Code formatting (no functional change)
- `refactor`: Code refactoring (no new features or bug fixes)
- `test`: Test related
- `chore`: Build process or auxiliary tool changes

#### 6. Push Branch

```bash
git push origin feature/your-feature-name
```

#### 7. Create Pull Request

1. Visit your forked repository
2. Click "Compare & pull request"
3. Fill in PR description:
   - **Title**: Clear and concise
   - **Description**: Explain changes, reasons, scope of impact
   - **Related Issue**: e.g., `Closes #123`
4. Wait for Code Review

## 🔍 Code Review Standards

PRs must meet the following requirements before being merged:

- [ ] Code follows project style guidelines
- [ ] Added necessary unit tests (if applicable)
- [ ] Updated relevant documentation
- [ ] Commit message follows conventions
- [ ] No new warnings or errors introduced
- [ ] Passed CI checks (if configured)

## 📚 Development Environment Setup

### Prerequisites

- Node.js >= 16.0.0
- npm >= 8.0.0
- Git

### Install Dependencies

```bash
npm install
```

### Local Testing

```bash
# Test CLI commands
npm run test

# Build project
npm run build

# Link to global (optional)
npm link
```

## 🙏 Acknowledgments

Thanks to everyone who has contributed to this project!

---

If you have any questions, feel free to ask in an issue or contact the maintainers.
