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
### PIP, APIs, and Requests Package
- Python's package manager — lets you install third-party libraries that don't come built-in
- `pip install cowsay` — example of installing a third-party package from command line
- Packages live on PyPI (Python Package Index) at pypi.org. After installing, you import them the same way as built-in modules
- Application Programming Interface (API) — get data from someone else's server using code
- `pip install requests` — install the requests package to make web requests from Python
- `requests.get(url)` — your code acts like a browser, fetches data from a URL
- Response usually comes back as *JSON* — key-value data format (like a Python dict)
- `response.json()` — converts the server response into a Python dictionary you can work with
- `json.dumps(data, indent=2)` — pretty-prints *JSON* so you can actually read it


