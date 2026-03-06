## Week 2 - Types of Errors
- `SyntaxError:` — typo/mistake in your code (missing quote, colon, etc.) — must be fixed before running
- `ValueError:` — wrong type of value passed to a function (e.g. passing "cat" to int())
- `NameError:` — using a variable that was never defined or failed to be assigned
- `Runtime errors:` — happen while the program is running, not when you write it

### New Commands
- `try:` — attempt to run code that might fail
- `except ValueError:` — runs only if a ValueError happens in the try block
- `else:` — runs only if NO exception happened (try succeeded)
- `pass:` — silently ignore the error, stay in the loop without printing anything
- `raise:` — manually trigger your own exception

```
while True:
    try:
        x = int(input("What's x? "))
    except ValueError:
        print("x is not an integer")
    else:
        break
```

### EOFError
- EOF = End of File — means "there is no more input coming," triggered when the user presses Ctrl+D in the terminal.
- Used to let the user exit a while True loop gracefully, means "im done"
  ```
  while True:
    try:
        item = input("Item: ")
    except EOFError:
        break
  ```
