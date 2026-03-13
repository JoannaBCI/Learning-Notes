## Week 6 — Files
Input and Output of Files — saving data that survives after the program ends
- `memory` — variables only last while the program runs — gone when it exits
- `file` — stores data on disk permanently — survives after program ends
- `File I/O` — code that reads from or writes to files
- `open(filename, mode)` — opens a file and returns a file handle (your connection to that file)
- "w" — write mode, creates file if needed, but OVERWRITES existing content every time
- "a" — append mode, adds to the bottom, never overwrites
- "r" — read mode, default, no need to type it
- `file.write(text)` — writes text to the file (no automatic newline — you must add \n yourself)
- 	`file.close()` — saves and closes file — easy to forget, so use with instead
```
with open("names.txt", "a") as file:
    file.write(f"{name}\n"x)
```
- `file.readlines()` — reads ALL lines at once, returns them as a list
- `for line in file:` — loops over the file line by line (more memory-efficient)
- `.rstrip()` — strips whitespace/newline from the END of a string — use this when reading lines
```
names = []
with open("names.txt") as file:
    for line in file:
        names.append(line.rstrip())

for name in sorted(names):
    print(f"hello, {name}")
```
### Comma-Separated Values (CSV) Files
Commas separate columns but if your data contains a comma then split() break, so use Python's csv module.
- `import csv`  — always at top of file
- `csv.reader(file)` — reads CSV row by row, each row comes back as a list
- `csv.DictReader(file)` — reads CSV using the first row as column names, each row is a dictionary
```
import csv
students = []
with open("students.csv") as file:
    reader = csv.DictReader(file)
    for row in reader:
        students.append({"name": row["name"], "home": row["home"]})

for student in sorted(students, key=lambda s: s["name"]):
    print(f'{student["name"]} is from {student["home"]}')
```
- `csv.writer(file)` — writes rows as lists
- `csv.DictWriter(file, fieldnames=[...])` — writes rows as dicts–safer, order doesn't matter
- `writer.writerow([...])` — writes one row
```
import csv
name = input("Name: ")
home = input("Home: ")
with open("students.csv", "a") as file:
    writer = csv.DictWriter(file, fieldnames=["name", "home"])
    writer.writerow({"name": name, "home": home})
```
