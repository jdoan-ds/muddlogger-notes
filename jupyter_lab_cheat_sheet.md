# 📓 Jupyter Notebook Cheat Sheet

A quick-reference guide to using `.ipynb` files effectively without rage-quitting. Covers keyboard shortcuts, cell types, markdown, and pro tips.

---

## 🧠 What is a Jupyter Notebook?

An interactive document for writing and running Python code in chunks (cells). Great for data exploration, plotting, and documentation.

---

## ⚡ Cell Types

| Type      | Description                                      |
|-----------|--------------------------------------------------|
| Code      | Executes Python (or other kernel) code           |
| Markdown  | For formatted text, headers, links, notes        |
| Raw       | Untouched text, not processed (rarely used)      |

To switch cell type:
- Use the dropdown menu at the top
- Or hit `Esc + M` (Markdown) or `Esc + Y` (Code)

---

## ⌨️ Keyboard Shortcuts

| Action                      | Shortcut           |
|-----------------------------|--------------------|
| Run cell                    | `Shift + Enter`    |
| Run cell, insert below      | `Alt + Enter`      |
| Insert cell below           | `B` (in command mode) |
| Insert cell above           | `A`                |
| Delete cell                 | `D` + `D`          |
| Switch to command mode      | `Esc`              |
| Switch to edit mode         | `Enter`            |
| Save notebook               | `Ctrl + S` / `Cmd + S` |

---

## 🧙‍♂️ Magic Commands

These are special commands prefixed with `%` or `%%` that do cool stuff inside notebooks.

```python
%timeit my_function()      # Time how long a function runs
%run my_script.py          # Run another script
%load my_script.py         # Load script into current cell
%matplotlib inline         # Render plots inline
```

## Use ? to get help:

```python
%timeit?
```

---

## 📝 Markdown Basics in Cells

```md
# H1 Header
## H2 Header
### H3 Header

**Bold text**
*Italic text*
- Bullet list
1. Numbered list

[Link text](https://example.com)
`inline code`
```

To write markdown:
	•	Change the cell to Markdown (M)
	•	Run the cell (Shift + Enter) to render it
    
---

## 🧠 Tips

- Name your notebooks clearly: project_01_analysis.ipynb
- Keep Markdown cells clean and useful
- Avoid giant cells—split code into logical chunks
- Restart your kernel (⏹️ + 🔁) if things get weird

---

## 📘 Resources

- Jupyter Notebook Docs
- Markdown Guide
- IPython Magic Commands

---

## 🧪 Creating Environments in JupyterLab

Use environments to isolate packages and avoid version conflicts between projects.

---

### ⚙️ Using `venv` (Built-in Python)

```bash
# Create new environment
python3 -m venv myenv

# Activate it (Mac/Linux)
source myenv/bin/activate

# Activate it (Windows)
myenv\Scripts\activate

# Install Jupyter in the environment
pip install jupyterlab ipykernel

# Add to Jupyter
python -m ipykernel install --user --name=myenv --display-name "Python (myenv)"
```

---

## 📓 Accessing the Environment in JupyterLab

- Restart JupyterLab if it was already open
- Open the Launcher
- Select the kernel: Python (myenv)

---

## 💡 Tips

- Keep one environment per project for sanity
- Always install ipykernel inside your env so Jupyter can see it
- Delete unused kernels with:

```bash
jupyter kernelspec list
jupyter kernelspec remove myenv
```

---