# Contributing to Image-Based Classification of Indonesian Traditional Houses

Thank you for considering contributing to this project! Every contribution helps improve the classification of Indonesian traditional houses and supports cultural heritage preservation through technology.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Style Guidelines](#style-guidelines)
- [Reporting Issues](#reporting-issues)

---

## Code of Conduct

This project adheres to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior by opening an issue.

---

## How Can I Contribute?

### 🐛 Report Bugs

Found a bug? Please [open an issue](../../issues/new?template=bug_report.md) with:
- A clear and descriptive title
- Steps to reproduce the behavior
- Expected vs actual behavior
- Your environment details (OS, Python version, GPU)

### 💡 Suggest Features

Have an idea? Please [open a feature request](../../issues/new?template=feature_request.md) with:
- A clear description of the proposed feature
- Why it would be useful to the project
- Any implementation ideas you may have

### 🔧 Submit Code Changes

1. Fork the repository
2. Create a feature branch from `main`
3. Make your changes
4. Submit a Pull Request

---

## Getting Started

### Prerequisites

- Python 3.10+
- Git
- (Optional) NVIDIA GPU with CUDA for training

### Setup

```bash
# Fork and clone your fork
git clone https://github.com/<your-username>/Image-Based-Classification-of-Indonesian-Traditional-Houses.git
cd Image-Based-Classification-of-Indonesian-Traditional-Houses

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # Linux/macOS
# venv\Scripts\activate   # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Development Workflow

1. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes** and test them thoroughly.

3. **Commit with clear messages:**
   ```bash
   git commit -m "feat: add data augmentation comparison"
   ```

   Use [Conventional Commits](https://www.conventionalcommits.org/) format:
   - `feat:` — new feature
   - `fix:` — bug fix
   - `docs:` — documentation changes
   - `refactor:` — code refactoring
   - `test:` — adding or updating tests

4. **Push and open a PR:**
   ```bash
   git push origin feature/your-feature-name
   ```

---

## Style Guidelines

### Python Code

- Follow [PEP 8](https://peps.python.org/pep-0008/) style guidelines
- Use meaningful variable and function names
- Add docstrings to all functions and classes
- Keep notebook cells focused and well-documented

### Jupyter Notebooks

- Include markdown cells explaining each section
- Clear all outputs before committing (to reduce file size)
- Use sequential cell execution order
- Add comments for non-obvious code blocks

### Documentation

- Write in clear, concise English
- Use markdown formatting consistently
- Include code examples where relevant

---

## Reporting Issues

When reporting issues, please include:

| Information | Example |
|------------|---------|
| OS | Ubuntu 22.04 / Windows 11 / macOS 14 |
| Python version | 3.10.12 |
| PyTorch version | 2.1.0 |
| FastAI version | 2.7.13 |
| GPU | NVIDIA RTX 3080 / None (CPU) |
| CUDA version | 12.1 / N/A |

---

## 🙏 Thank You

Your contributions help make this project better for everyone. Whether it's fixing a typo, improving documentation, adding new features, or extending the model — every contribution matters!
