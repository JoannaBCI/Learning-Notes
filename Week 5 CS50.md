## Week 5 — Unit Tests
Write code that tests your code automatically, so you don't have to test manually every time
- `def` - define, creating a function with a name.
- `assert` — boldly claim something is true. If it's false, raises an error.
   `assert square(2) == 4` → passes silently if true, crashes if false
- `pytest `— third party tool that runs your tests automatically and gives you readable output
   install: pip install pytest
   run: pytest test_calculator.py
- `test_something.py` - test file name
- `test_something()` - test functions name
- `pytest.raises` — use this when you expect an error to be raised
```
pythonimport pytest
with pytest.raises(TypeError):
    square("cat")
```
### Organizing tests:
Functions should return values, not just print them, otherwise you can't test them with assert:
1. Split into multiple small functions (test_positive, test_negative, test_zero) so failures give more specific clues
2. Can put tests in a folder called tests/ — needs an empty __init__.py file inside
3. Run whole folder: pytest tests/
