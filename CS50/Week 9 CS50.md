## Week 9 — Et Cetera
- `set()` — empty set, auto-removes duplicates
- `s.add(x)` — add item (not .append())
- `if x in s` — membership check
- `global x` - to modify globals inside functions freely

### Type Hints
- `n: int` — hint a variable's type
- `def f(n: int) -> str:` — hint param and return types
- `pip install mypy` - pell-checker but for your variable types.
- `"""` - triple quotes inside the function (not above), tools can auto-generate documentation from them

### argparse
Replaces manual `sys.argv` parsing:
- `argparse.ArgumentParser(description=)` — creates parser
- `.add_argument("-n", default=, type=, help=)` — defines a flag
- `.parse_args()` — reads sys.argv automatically, access values via `args.n`

### Unpacking
- `*list` — unpacks list into positional args
- `**dict` — unpacks dict into named args
- `*args` in a function def — accepts any number of positional args
- `**kwarg`s in a function def — accepts any number of named args
- `map(func, iterable)` — applies function to every element
- `filter(func, iterable)` — keeps elements where function returns True (both work well with `lambda`)

### List / Dict Comprehensions
- `[expr for x in iterable]` — build a list
- `[expr for x in iterable if condition]` — filtered list
- `{k: v for x in iterable}` — build a dict
- `for i, val in enumerate(list)` — gives index + value, replaces `range(len(...))`


yield / Generators

return — gives everything back at once
yield — gives one value at a time, remembers where it left off
Prevents memory crashes on large data
