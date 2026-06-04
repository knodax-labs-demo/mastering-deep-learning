# Installing Jupyter Notebook

Jupyter Notebook is one of the most widely used tools for learning data science, machine learning, and deep learning. It provides an interactive browser-based environment where code can be executed one cell at a time while displaying outputs, visualizations, and explanations alongside the code.

The examples and hands-on labs in this repository are designed to run in Jupyter Notebook.

---

## Prerequisites

Before installing Jupyter Notebook, ensure that Python 3.10 or later is installed.

Verify the installation:

```bash
python --version
```

or

```bash
python3 --version
```

---

## Create a Virtual Environment (Recommended)

Create a virtual environment:

```bash
python -m venv venv
```

Activate the environment:

### Windows

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
source venv/bin/activate
```

---

## Install Jupyter Notebook

Install Jupyter Notebook using pip:

```bash
pip install notebook
```

Verify the installation:

```bash
jupyter --version
```

---

## Install Repository Dependencies

Install the packages required for the book examples:

```bash
pip install torch torchvision torchaudio
pip install numpy pandas matplotlib scikit-learn
```

Alternatively, if a requirements file is provided:

```bash
pip install -r requirements.txt
```

---

## Launch Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

A browser window should automatically open displaying the Jupyter Notebook dashboard.

If it does not open automatically, copy and paste the URL displayed in the terminal into your web browser.

---

## Create a New Notebook

1. Open the Jupyter dashboard.
2. Click **New**.
3. Select **Python 3**.
4. Begin running the examples from the repository.

---

## Verify PyTorch Installation

Create a new notebook cell and run:

```python
import torch

print("PyTorch Version:", torch.__version__)
print("CUDA Available:", torch.cuda.is_available())
```

Example output:

```text
PyTorch Version: 2.x.x
CUDA Available: False
```

If no errors occur, the environment is ready for the hands-on labs.

---

## Updating Jupyter Notebook

Update Jupyter Notebook to the latest version:

```bash
pip install --upgrade notebook
```

---

## Troubleshooting

### Command Not Found

If the `jupyter` command is not recognized:

```bash
python -m notebook
```

### Package Installation Issues

Upgrade pip and reinstall:

```bash
python -m pip install --upgrade pip
pip install notebook
```

### Verify Installed Packages

List installed packages:

```bash
pip list
```

---

## Optional: Install JupyterLab

JupyterLab provides a modern interface with multiple tabs, terminals, and file management features.

Install JupyterLab:

```bash
pip install jupyterlab
```

Launch JupyterLab:

```bash
jupyter lab
```

---

The Jupyter environment is now ready to run all examples and hands-on labs provided in the *Mastering Deep Learning* repository.
