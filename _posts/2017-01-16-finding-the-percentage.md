---
layout: post
title: "Finding the Percentage"
categories:
  - Learning
tags:
  - Python 3
  - Hacker Rank
  - Coding
---

```python
def avg(list):
    return "{0:.2f}".format(sum(list) / len(list))

if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    
    print(avg(student_marks[query_name]))
```
