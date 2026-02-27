## Week 2 - Loop
- `while` — repeat as long as condition is True
```
i = 0
while i < 3:
    print("meow")
    i += 1
```
- `for` — repeat over a sequence of values, find anomaly in char
```
  for i in range(3):
    print("meow")
```
- `break` — exit the loop when condition is met
- `continue` — skip current iteration, go back to top of loop
- `range(n)` — generates numbers 0 up to but not through n

### i means Index
- `i` - the location for the value, not the value itself
- i += 1 is shorthand for i = i + 1
- `Ctrl + C` to escape an infinite loop
- Always change the variable or you get an infinite loop
- `in` - checks whether a value exists inside a list, python is asking "is the number the user typed one of these three values?"

### Lists
- `[]`– creates list, first item is `[0]` index
- `:` – categorizes what is with what, while `,` seperates words
- `len(students)` — returns length of list
- `{}` - cictionaries
- `print()` - prints a newline
- `print("#", end="")` — no newline after printing
- `char` - runs through each character in a word
- `isupper` - built-in method that checks upper/lower case char
