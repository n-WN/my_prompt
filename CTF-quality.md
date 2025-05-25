> Here's a concise prompt template for transforming code into CTF-quality solutions:

**Prompt:**

Convert this Python code into competition-quality CTF solution code with these characteristics:

1. Variable Names:
   - Use minimal single-letter variables (e.g., 'g' instead of 'generator')
   - Remove all type hints and descriptive names

2. Structure:
   - Remove all comments and docstrings
   - Collapse nested functions into main flow
   - Use maximum 3 levels of indentation

3. Output:
   - Direct raw output without formatting
   - No progress messages or debug prints
   - Single print statement for final result

4. Error Handling:
   - Remove all try/except blocks
   - Assume perfect input conditions

5. Math Focus:
   - Keep all cryptographic primitives
   - Maintain core algorithm unchanged
   - Use most aggressive early termination

Example Transformation:

Before:

```python
def safe_inverse(value, modulus):
    """Computes modular inverse safely"""
    try:
        return pow(value, -1, modulus)
    except ValueError:
        raise Exception("No inverse exists")
```

After:

```python
def inv(v, m):
    return pow(v,-1,m)
```

Apply this transformation to the following code:

[PASTE CODE HERE]
