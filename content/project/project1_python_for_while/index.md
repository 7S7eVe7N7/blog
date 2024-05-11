---
title: Циклы в Python
summary: В этом проекте я постараюсь объяснить принцип действия циклов for и while в Python.
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

# Циклы

Циклы позволяют выполнять некоторое действие в зависимости от соблюдения некоторого условия. В языке Python есть следующие типы циклов:

- for;
- while.

# While

- Циклы — базовый инструмент программирования на Python. С их помощью разработчики могут быстро выполнять повторяющиеся действия, автоматизируя процесс;

- В каждом цикле есть условие и блок кода, которые выполняются, пока условие истинно;

- С помощью циклов for можно итерировать коллекции данных, выполняя преобразования;

```Python
for n in range(4, 10):
    print(n, end=" ")
```

- В циклах while задается явное условие;

```Python
number = 1
 
while number < 5:
    print(f"number = {number}")
    number += 1
print("Работа программы завершена")
```

- С помощью ключевого слова break можно в любой момент прервать выполнение цикла;

```Python
number = 0
while number < 5:
    number += 1
    if number == 3: # если number = 3, выходим из цикла
        break
    print(f"number = {number}")
```

- Continue позволяет пропускать итерации, не подходящие под условие.

```Python
number = 0
while number < 5:
    number += 1
    if number == 3: # если number = 3, переходим к новой итерации цикла
        continue
    print(f"number = {number}")
```






















