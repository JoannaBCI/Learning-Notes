## Week 4 — Libraries
- Library/Module? -  file of code someone else wrote that you can pull into your own program, instead of rewriting it yourself
- `import` - loads a module into your file so you can use its functions
- `from X import Y` - loads only ONE specific function from a module, so you don't need to prefix it with the module name every time
- `random.choice(list)` - picks one item from a list at random, equal probability for each
- `random.randint(a, b)` - returns a random whole number between a and b, inclusive
- `random.shuffle(list)` - shuffles the list in plac, has no return value.
- Don't do `result = random.shuffle(cards)`, just call random.shuffle(cards) and the list itself is now shuffled.
- `statistics.mean(list)` - returns the average of a list of numbers, same idea as random, just a different module you import
