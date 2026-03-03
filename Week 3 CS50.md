#Types of Errors
- `SyntaxError:` — typo/mistake in your code (missing quote, colon, etc.) — must be fixed before running
- `ValueError:` — wrong type of value passed to a function (e.g. passing "cat" to int())
- `NameError:` — using a variable that was never defined or failed to be assigned
- `Runtime errors:` — happen while the program is running, not when you write it

#New Commands
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

