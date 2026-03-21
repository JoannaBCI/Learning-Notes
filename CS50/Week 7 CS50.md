## Week 7 - Regex
Pattern you define to validate input (email, URL), clean messy data, or extract parts of a string
- `import re` - python's regex library:
- `re.search(pattern, str)` - search anywhere in string for pattern — returns match object or None
- `re.match(pattern, str)` - Same but auto-matches from start (no need for ^)
- `re.fullmatch(pattern, str)` - Must match entire string (no ^ or $ needed)
- `re.sub(pattern, replacement, str)` - Find and replace — returns the modified string
- `re.split(pattern, str)` - Split string using a regex pattern
- `re.findall(pattern, str)` - Returns list of all matches found in string

### Pattern symbols
- `.` -	Any single character (except newline)
- `*`	- Zero or more of previous	(a* = "", "a", "aa"...)
- `+`	- One or more of previous	(a+ = "a", "aa"... (not ""))
- `?` -	Zero or one, makes it optional	(https? = "http" or "https")
- `{m}`	-	Exactly m repetitions	(a{3} = "aaa")
- `{m,n}`	-	Between m and n repetitions	(a{2,4} = "aa", "aaa", "aaaa")
- `^`	-	Start of string	(^hello must start with "hello")
- `$`	-	End of string	(edu$ must end with "edu")
- `[ ]`	-	Set of allowed characters
- `[^ ]` -	Any character NOT in set ([^@] = anything except @)
-  `\`	-	Escape after char
-  `|` -	.org
-  `( )`	-	Group and capture	returned via matches.group(1)
-  `(?:)`	-	 Group but don't capture, use when you only need grouping for ? or |

### Symbol	Meaning
- `\w`	-	Word character = [a-zA-Z0-9_]
- `\W`	-	Anything NOT a word character
- `\d`	-	Decimal digit = [0-9]
- `\D`	-	Anything NOT a digit
- `\s`	-	Whitespace (space, tab)
- `\S`	Anything NOT whitespace
- `Flags` -	(3rd argument to re.search)
- `Flag`	-	What it does
- `re.IGNORECASE`	-	Case-insensitive matching
- `re.MULTILINE`	-	^ and $ match per line, not whole string
- `re.DOTALL`	-	. also matches newlines
- `r"\."` - raw strings for regex
- `r"\w+"` - raw strings for regex word chars

### Capturing groups
Wrap part of a pattern in ( ) to extract that piece
- `matches.group(1)` - first set of parens, group(2) → second, etc.
- `matches.groups()` - returns all as a tuple, groups start at 1, not 0, can unpack: `last, first = matches.groups(`),
- `:=` - Walrus operator, assign and check in one line inside an `if`
```
if matches := re.search(r"^(\w+), *(\w+)$", name):
    last, first = matches.groups()
```
