# 🐍 Anaconda Cheat Sheet

A quick-reference for managing Python environments and packages using Anaconda and `conda`.

---

## 🚀 Getting Started

- Install from [anaconda.com](https://www.anaconda.com)
- Comes with Python, JupyterLab, and over 150 packages
- Use Anaconda Navigator for GUI (optional)

---

## 🔧 Conda Environment Basics

```bash
# Create new environment with Python 3.10
conda create -n myenv python=3.10

# Activate the environment
conda activate myenv

# Deactivate environment
conda deactivate

# Delete an environment
conda remove -n myenv --all

---

## 📦 Managing Packages

```bash
# Install a package
conda install pandas

# Install from pip inside conda
pip install seaborn

# List all installed packages
conda list

# Update a package
conda update numpy
```

---

## 🧠 Environment Management

```bash
# Export environment to file
conda env export > environment.yml

# Create env from file
conda env create -f environment.yml

# List environments
conda env list
```

---

## 💬 Tips

- Always activate your env before installing packages
- Prefer conda over pip when using Anaconda (better dependency resolution)
- Keep environments small and project-specific

---
