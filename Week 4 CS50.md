## Week 4 — Libraries
Library/Module -  file of code someone else wrote that you can pull into your own program, instead of rewriting it yourself
- `import` - loads a module into your file so you can use its functions
- `from X import Y` - loads only ONE specific function from a module, so you don't need to prefix it with the module name every time
- `random.choice(list)` - picks one item from a list at random, equal probability for each
- `random.randint(a, b)` - returns a random whole number between a and b, inclusive
- `random.shuffle(list)` - shuffles the list in plac, has no return value.
- Don't do `result = random.shuffle(cards)`, just call random.shuffle(cards) and the list itself is now shuffled.
- `statistics.mean(list)` - returns the average of a list of numbers, same idea as random, just a different module you import
 ```
  import random
random.choice(["heads", "tails"])
```

### SYS Built-in module
input typed when running the file, not when prompted inside it. Running "python name.py David" means David lands in sys.argv[1].
- `sys.argv` - a list of everything the user typed at the command line when running the program
- `sys.argv[0]` - always the filename itself (e.g. name.py) — not useful usually
- `sys.argv[1]` - the first actual argument the user typed after the filename
- `sys.exit("msg")` - prints the message and quits the whole program immediately
- `sys.argv[1:]` - a slice — grabs everything EXCEPT argv[0], so you skip the filename
```
import sys # Guard clause pattern — check before assuming argv[1] exists
  if len(sys.argv) < 2: sys.exit("Too few arguments")
  elif len(sys.argv) > 2: sys.exit("Too many arguments")
print(f"Hello, {sys.argv[1]}")
```
