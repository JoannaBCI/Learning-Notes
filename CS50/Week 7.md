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
-  `|`	-	.org
-  `( )`	-	Group and capture	returned via matches.group(1)
-  `(?:)`	-	 Group but don't capture, use when you only need grouping for ? or |
