## Week 1 - Conditionals Operators
- `>` — Greater than
- `>=` — Greater than or equal to
- `<` — Less than
- `<=` — Less than or equal to
- `==` — Equal to (comparison, NOT assignment)
- `!=` — Not equal to
- `=` — Assignment only (copies value from right to left)

### Keywords
Use if/elif when you're checking conditions, ranges, or using .startswith(), .lower(), >, <, etc:
- `if` — Ask a question; run indented code if the answer is True
- `elif` — "Else if" — only asked if the previous `if` was False
- `else` — Catch-all; runs if no previous condition was True
- `and` — Both conditions must be True
- `or` — At least one condition must be True

Use match/case when you're checking if something equals specific exact values:
- `match` — Match a variable against specific cases 
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
- `%` – returns
- `if` → always asked first
- `elif` → only asked if previous was False
- `else` → runs if nothing above was True
- `and` – both must be True
- `or` – one must be True
- Using `elif`/`else` means only one branch runs

### Match name:
- `.lower()` – converts whatever the user types to all lowercase.
- `.strip()` – removes accidental spaces at the start or end of the input.
- `.startswith()` — checks if a string begins with something. H in Hello.
- `.split()` — cuts a string into a list of pieces wherever you tell it to split. [cat.jpg] → ["cat", "jpg"]
- `|` separates multiple values in one case
- `_` is the catch-all (like `else`)
- No `break` needed — Python exits after a match automatically
