# JupyterDebug

**JupyterDebug** is a Python package designed to help users debug code in Jupyter notebooks using OpenAI's language models. It provides an easy-to-use interface for automatically fixing errors in your code by leveraging the power of large language models (LLMs).

---

## Features

- **Automatic Debugging**: Fix errors in your code with a single function call.
- **Customizable Models**: Choose from multiple OpenAI models for debugging.
- **Interactive Initialization**: Prompt the user for their OpenAI API key and model selection.
- **Cross-Platform Support**: Works in Jupyter Notebook, JupyterLab, Google Colab, and VSCode.

---

## Installation

You can install `JupyterDebug` using pip:

```bash
pip install JupyterDebug


Here’s the recommended documentation structure and content for your `JupyterDebug` project. The documentation is organized into two main files: `index.md` (main documentation) and `usage.md` (usage instructions). These files should be placed in the `docs/` directory of your project.

---

## 1. `docs/index.md` (Main Documentation)

```markdown
# JupyterDebug

**JupyterDebug** is a Python package designed to help users debug code in Jupyter notebooks using OpenAI's language models. It provides an easy-to-use interface for automatically fixing errors in your code by leveraging the power of large language models (LLMs).

---

## Features

- **Automatic Debugging**: Fix errors in your code with a single function call.
- **Customizable Models**: Choose from multiple OpenAI models for debugging.
- **Interactive Initialization**: Prompt the user for their OpenAI API key and model selection.
- **Cross-Platform Support**: Works in Jupyter Notebook, JupyterLab, and VSCode.

---

## Installation

You can install `JupyterDebug` using pip:

```bash
pip install JupyterDebug
```

---

## Quick Start

1. **Initialize the Package**:
   ```python
   import JupyterDebug as jd
   jd.init()
   ```

2. **Debug Your Code**:
   ```python
   # Cell 1: Code with an error
   x = 10
   y = "20"
   z = x + y  # This will raise a TypeError

   # Cell 2: Debug the error
   jd.debug(max_iter=2)
   ```

---

## Documentation

For detailed usage instructions, see the [Usage Guide](usage.md).

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```