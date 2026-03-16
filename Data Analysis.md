## Matplotlib Commands
### Setup
- `import matplotlib.pyplot` as plt — loads the plotting library, plt is the standard nickname
- `import statistics` — loads math functions like mean and standard deviation
- `import csv` — loads CSV file reading (already in my Week 6 notes)

### Statistics
- `statistics.mean(list)` — average of all values in a list
- `statistics.stdev(list)` — standard deviation, how spread out the values are
- `min(list)` — smallest value, built into core Python
- `max(list)` — largest value, built into core Python

### Enumerate
- for `i`, row in `enumerate(list)`: — loops through a list giving you both a counter i AND the actual item at the same time
- `row` → the actual item at that position, useful when you need to know both where you are AND what you're looking at

### Expression
- `if i >= 50000: break` — example: stop after 50,000 iterations so you don't process a massive file
- `sum(1 for x in list if condition)` — counts how many items in a list meet a condition, without making a new list
- example: `sum(1 for s in signal if s > 0)` → counts how many values are above 0

## Creating a Figure
- `fig, axes = plt.subplots(rows, cols, figsize=(width, height))` — creates a figure with multiple subplots
- `figsize=(14, 7)` — width and height in inches
- `axes[0]` — first subplot, axes[1] — second subplot, and so on
- `fig.suptitle("text")` — adds a title to the whole figure, above all subplots

## Drawing a Line Plot
- `axes[0].plot(x_list, y_list)` — draws a line graph on a subplot
- `color="red"` — sets line color, accepts names or hex codes like "#2c5f8a"
- `linewidth=0.5` — thickness of the line
- `alpha=0.85` — transparency, 1.0 = fully solid, 0.0 = invisible
- `label="text"` — text that appears in the legend for this line

## Reference Lines
- `axes[0].axhline(value)` — draws a flat horizontal line across the whole plot at that y value
- `linestyle="--"` — dashed line
- `linestyle=":"` — dotted line

## Labels & Titles
- `axes[0].set_title("text")` — title above that specific subplot
- `axes[0].set_xlabel("text")` — label on the x axis
- `axes[0].set_ylabel("text")` — label on the y axis
- `axes[0].legend(fontsize=9)` — shows the legend box using all the label= values you set

## Saving & Showing
- `plt.tight_layout()` — auto-adjusts spacing between subplots so nothing overlaps
- `plt.savefig("filename.png", dpi=150)` — saves the figure as an image file to your current folder
- `dpi=15`0 — resolution, dots per inch — higher = sharper, 150 is good for slides
- `bbox_inches="tight"` — prevents edges of the plot from being cut off when saving
- `plt.show()` — opens the interactive plot window

## Slicing a List for Plotting
- `list[:5000]` — grabs only the first 5,000 items, useful for zooming into a section of data
- same slicing rules as strings — [start:stop], empty start = beginning, empty stop = end
