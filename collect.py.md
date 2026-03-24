### Imports
- `import json` - reads and writes .json files
- `import time` - lets Python pause execution for a set number of seconds
- `import psutil` - third party library that reads live system data like running processes, CPU, memory
- `import os` - communicates with the file system, builds and resolves folder paths
- `import subprocess` - runs terminal commands from inside a Python script
- `import sys` - controls Python's runtime settings, including where it looks for files to import
- `from datetime import datetime` - imports only the datetime tool from Python's time library

### Path and Import Setup
- `sys.path` - the list Python searches when you import something
- `.append()` - adds a new item to the end of a list
- `os.path.expanduser()` - converts ~ shorthand into the full folder path your OS understands
- `from module import function` - pulls one specific function out of another file without importing the whole thing
- `VARIABLE = value` - stores a value under a name so you can reuse it without retyping

### Functions
- `def` - defines a reusable block of code with a name
- `list() `- converts something into a list
- `set()` - removes duplicates from a collection
- `[:20]` - slice notation, take only the first 20 items
- `.decode()` - converts raw bytes output into a readable string
- `[-1]` - grabs the last item in a list
- `.replace('x', 'y')` - finds every occurrence of x in a string and swaps it for y

### Writing the Output
- `open(file, "w")` - opens a file in write mode, overwrites whatever was there before
- `with open() as f` - opens the file, gives it a short nickname f, and closes it automatically when done
- `json.dump(data, file)` - writes a Python dictionary into a file in JSON format
- `indent=2` - formats the JSON with spacing so it is human readable
- `if __name__ == "__main__"` - only execute this block if this file was run directly, not imported
- `while True` - loop forever until manually stopped
- `time.sleep(30)` - pause execution for 30 seconds

### Key Concepts
- `subprocess` - runs a terminal command from inside Python and captures what it prints
- `JSON` - a structured text format for storing labeled data, programs use it to pass information to each other
- `state.json` - the shared live file everything else reads from
- `try/except` - error handling, attempt something and catch failures without crashing
