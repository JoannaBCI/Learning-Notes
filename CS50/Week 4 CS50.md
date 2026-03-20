## Week 4 — Libraries
Library/Module -  file of code someone else wrote that you can pull into your own program, instead of rewriting it yourself
- `import` - loads a module into your file so you can use its functions
- `import requests` - importing a library someone else built that handles internet connections. It lets Python talk to websites/APIs.
- `import sys` - importing allow access to system-level stuff, like what the user typed in the terminal, not the input command line.
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
- `len` -  length, as in how many items are in a list, 'python bitcoin.py' 1 gives you ["bitcoin.py", "1"] — length 2.
- `!` -  "not equal to", so this says "if the user didn't type exactly one argument, complain."
  
### SYS Built-in module
input typed when running the file, not when prompted inside it. Running "python name.py David" means David lands in sys.argv[1].
- `sys.argv` - a list of everything the user typed at the command line in terminal
- `sys.argv[0]` - always the filename itself (e.g. name.py) — not useful usually
- `sys.argv[1]` - the first actual argument the user typed after the filename
- `sys.exit("msg")` - prints the message and quits the whole program immediately
- `sys.argv[1:]` - a slice — grabs everything EXCEPT argv[0], so you skip the filename
- `len(sys.argv)` — counts how many command-line arguments were passed

### File Handling
- `open(filename)` — opens a file on your computer so Python can read it
- `with open(sys.argv[1]) as f:` — opens the file the user passed in as a command-line argument. The as f just a variable name for the file object, nothing to do with float or f-strings
- `FileNotFoundError` — a built-in Python error (not your variable), fires automatically when you try to open a file that doesn't exist
- `TypeError` — wrong type used
- `ValueError` — right type, wrong value
- `.endswith("")` — checks if a string ends with whatever I write

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
- Any .py file you create can be imported as a module by another file in the same folder
- If your file has a `main()` function, wrap the call in a guard so it only runs when you run the file directly — not when you import it
```
if __name__ == "__main__":
    main()
```
It's just asking Python "wait, am I being run directly or imported right now?" and acting accordingly.



