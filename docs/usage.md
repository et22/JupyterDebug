# Usage Guide

This guide provides detailed instructions on how to use the `JupyterDebug` package.

---

## Initialization

The `init()` function initializes the package by prompting the user for their OpenAI API key and selecting a model. It can also accept the API key and model as optional arguments.

### Syntax
```python
jd.init(api_key=None, model=None)
```

### Parameters
- **`api_key`** (optional): Your OpenAI API key. If not provided, the user will be prompted to enter it.
- **`model`** (optional): The model to use for debugging. Options include:
  - `gpt4o-mini` (default)
  - `gpt4o`
  - `o1`
  - `o1-mini`

### Example
```python
import JupyterDebug as jd

# Initialize with API key and model
jd.init(api_key="your-api-key-here", model="gpt4o")

# Initialize interactively (prompts for API key and model)
jd.init()
```

---

## Debugging Code

The `debug()` function automatically debugs the code in the previous cell by calling the selected language model iteratively to fix errors.

### Syntax
```python
jd.debug(max_iter=1)
```

### Parameters
- **`max_iter`** (optional, default=1): The maximum number of times the language model is called to iteratively debug the code. If the first solution does not fix all errors, the method will retry up to `max_iter` times.

### Example
```python
# Cell 1: Code with an error
x = 10
y = "20"
z = x + y  # This will raise a TypeError

# Cell 2: Debug the error
jd.debug(max_iter=2)
```

---

---

## Revising Code

The `revise(prompt)` function automatically revises the code in the previous cell by calling the selected language model iteratively to implement the revision specified by the prompt.

### Syntax
```python
jd.revise(prompt="Please add comments to the code.")
```

### Parameters
- **`prompt`** (optional, default="Please add comments to this code."): The instruction the language model receives for revising the code. 

### Example
```python
# Cell 1: Code 
x = 10
y = 20
z = x + y  

# Cell 2: Revise this code
jd.revise(prompt="Please add comments to the code.")
```

---

## Troubleshooting

### Common Issues
1. **API Key Not Recognized**:
   - Double-check that the API key is correct and has sufficient permissions.
   - If using an environment variable, ensure it is set correctly.

2. **Model Not Available**:
   - Verify that the selected model is supported by your OpenAI account.


## Support

For additional help, please open an issue on the [GitHub repository](https://github.com/et22/JupyterDebug).