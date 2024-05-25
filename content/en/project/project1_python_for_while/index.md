---
title: Loops in Python
summary: In this project, I will try to explain how for and while loops work in Python.
tags:
  - Deep Learning
date: '2024-05-10T20:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption:
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Follow
    url: https://github.com/7S7eVe7N7
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: loops in Python
---

# Loops

Cycles allow you to perform some action depending on the observance of some condition. Python has the following types of loops:

- for;
- while.

# While

- Loops is a basic Python programming tool. With their help, developers can quickly perform repetitive actions, automating the process;

- In each cycle there is a condition and a code block that are fulfilled as long as the condition is true;

- Using for loops, you can iterate data collections by performing transformations;

```Python
for n in range(4, 10):
    print(n, end=" ")
```

- An explicit condition is specified in **while** loops;

```Python
number = 1
 
while number < 5:
    print(f"number = {number}")
    number += 1
print("Program completed")
```

- Using the **break** keyword, you can interrupt a loop at any time;

```Python
number = 0
while number < 5:
    number += 1
    if number == 3: # if number = 3, exit the loop
        break
    print(f"number = {number}")
```

- **Continue** allows you to skip iterations that do not fit the condition.

```Python
number = 0
while number < 5:
    number += 1
    if number == 3: # if number = 3, go to a new iteration of the loop
        continue
    print(f"number = {number}")
```






















