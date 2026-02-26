## Week 0 - Terminal Commands
- `cp <source> <destination>` - Copy a file
- `mv <source> <destination>` - Move or rename a file
- `rm <filename>` - Remove/delete a file
- `mkdir <dirname>` - Make a new directory/folder
- `cd <dirname>` - Change into a directory
- `cd ..` - Go up to parent directory
- `cd` - Return to default/home directory
- `rmdir <dirname>` - Remove an empty directory
- `clear` - Clear the terminal screen

### Shortcuts
- `Tab` — Autocomplete a file/folder name
- `Ctrl + L` — Clear the terminal (same as `clear`)
- `↑ / ↓ arrow keys` — Scroll through command history

### Special Syntax
- `.` — Represents the current directory
- `..` — Represents the parent directory
- `/` at end of name — Indicates a directory (e.g. `folder/`)

### Functions
- `python <filename.py>` - Run a Python file
- `python` - Open interactive mode (type code directly)
- `print("text")` - Display text on screen (print(text.lower())–makes text lowercase)
- `input("prompt")` - Ask user to type something, returns what they typed
- `int(value)` - Convert to integer
- `float(value)` - Convert to decimal number
  `.1f` - The number before f is  how many decimal places you want (.3f → 2.000, .0f → 2)
- `round(number, digits)` - Round a number (digits optional)
- `print(text.replace("text","text"))` - Replace a segment with another.
- `[::-1]` reverse a string
    - `[start : stop : step]`
    - start → where to begin (empty = beginning of string)
    - stop → where to end (empty = end of string)
    - step → how to move (-1 = go backwards one at a time)

### Defining
- `def function_name(parameter)`: - Define a function
Indent the code underneath with 4 spaces or Tab
- `return value` - Hand back a result from the function

### Syntax
- `variable = value` - Store a value (assignment)
- `f"Hello, {name}"` - F-string, inserts variable into text
- `"text" + variable` - Concatenate (join) text
- `x * y` - Multiply
- `x ** y` - Raise to a power
- `x % y` - Remainder after division
- '##' this is a comment - Note to myself, ignored by Python
