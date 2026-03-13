## Week 6 — Files
To saving data that survives after the program ends:
- `memory` — variables only last while the program runs — gone when it exits
- `file` — stores data on disk permanently — survives after program ends
- `File I/O` — code that reads from or writes to files
- `open(filename, mode)` — opens a file and returns a file handle (your connection to that file)
- "w" — write mode, creates file if needed, but OVERWRITES existing content every time
- "a" — append mode, adds to the bottom, never overwrites
- "r" — read mode, default, no need to type it
- `open(f, "w")` - create/overwrite file
`open(f, "a")` - append to file
`open(f)`,`open(f, "r")` - read file
`with open(...) as file:` - auto-closes 
`.write(text)`	write to file (add \n manually)
- `file.write(text)` — writes text to the file (no automatic newline — you must add \n yourself)
- 	`file.close()` — saves and closes file — easy to forget, so use with instead
```
with open("names.txt", "a") as file:
    file.write(f"{name}\n"x)
```
- `file.readlines()` — reads ALL lines at once, returns them as a list
- `for line in file:` — loops over the file line by line (more memory-efficient)
- `.rstrip()` — strips whitespace/newline from the END of a string, use this when reading lines
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

### Sort Dictionaries
- `key=` — tells `sorted()` what to sort by when items aren't plain strings
- `lambda` — anonymous (nameless) function — used when you only need it once(?)
- `sorted(x, key=lambda...)` - sort list of dicts by a field
```
# Sort by name
sorted(students, key=lambda s: s["name"])
# Sort by home, reversed
sorted(students, key=lambda s: s["home"], reverse=True)
```
### Binary Files and Images
Not all files are text as images, audio, video are binary (zeros and ones)
- pip install pillow — installs the Pillow image library
- from PIL import Image — imports image support
- `Image.open(filename)` — opens an image file
- `image.save(filename, ...)` — saves image — library handles opening/closing
  
Create an animated GIF from two images
```
import sys
from PIL import Image
images = []
for arg in sys.argv[1:]:       # skip argv[0] (filename itself)
    images.append(Image.open(arg))
images[0].save(
    "output.gif",
    save_all=True,
    append_images=[images[1]],
    duration=200,   # ms per frame
    loop=0          # 0 = loop forever
)
```
