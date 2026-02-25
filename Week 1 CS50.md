## Week 1 - Conditionals Operators
- `>` — Greater than
- `>=` — Greater than or equal to
- `<` — Less than
- `<=` — Less than or equal to
- `==` — Equal to (comparison, NOT assignment)
- `!=` — Not equal to
- `=` — Assignment only (copies value from right to left)

### Keywords
- `if` — Ask a question; run indented code if the answer is True
- `elif` — "Else if" — only asked if the previous `if` was False
- `else` — Catch-all; runs if no previous condition was True
- `and` — Both conditions must be True
- `or` — At least one condition must be True
- `match` — Match a variable against specific cases (like a cleaner if/elif/else)
- `case` — Defines each option inside a `match` block
- `_` — Wildcard/catch-all inside a `match` (equivalent to `else`)

### Syntax Rules
- Always end `if`, `elif`, `else`, `match`, `case` lines with a **colon `:`**
- Indent the code block under each condition (4 spaces or 1 Tab)
- Python **enforces indentation** — code will break without it
- No parentheses required around conditions (optional)
- No curly braces `{}` — Python uses indentation instead

### Boolean Expressions
A question with only a **True or False** answer.
- `True` — capital T
- `False` — capital F
- Functions can **return** True or False directly
```python
def is_even(n):
    return n % 2 == 0

    
