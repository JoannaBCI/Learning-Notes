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

### Modulo Operator `%`
- Returns the **remainder** after division.
    ```
    4 % 2 == 0   # True → even
    3 % 2 == 1   # True → odd
    ```
- if / elif / else Structure
    ```
    if x < y:
        print("x is less than y")
    elif x > y:
        print("x is greater than y")
    else:
        print("x is equal to y")
    ```
- `if` → always asked first
- `elif` → only asked if previous was False
- `else` → runs if nothing above was True
- Once a condition is True, the rest are **skipped**
- Both must be True
  ```
  if 90 <= score <= 100:
      print("A")
- One must be True
   ```
   if x < y or x > y:
       print("x is not equal to y")```

## match / case
```python
match name:
    case "Harry" | "Hermione" | "Ron":
        print("Gryffindor")
    case "Draco":
        print("Slytherin")
    case _:
        print("Who?")
```

- `|` separates multiple values in one case
- `_` is the catch-all (like `else`)
- No `break` needed — Python exits after a match automatically

---

## Functions
```python
def is_even(n):
    return n % 2 == 0

def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")

main()
```

---

## Key Concepts

- **Control flow** — the order in which code runs, top to bottom, shaped by conditions
- **Mutually exclusive conditions** — using `elif`/`else` means only one branch runs
- **Design vs. correctness** — code can be correct but still poorly designed
- **Pythonic** — writing code in the clean, readable style preferred by Python community
- **Boolean expression as return value** — instead of `if True else False`, just `return n % 2 == 0`
Click the pencil ✏️ edit button on GitHub, select all, delete, paste this in, then commit. It'll render properly. Sonnet 4.6
    
