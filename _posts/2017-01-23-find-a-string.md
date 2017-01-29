---
layout: post
title: "Find a String"
categories:
  - Learning
tags:
  - Python 3
  - Hacker Rank
  - Coding
---

```python
def count_substring(string, substring):
    count = 0

    for i in range(0, len(string)):
        if string[i:(i+len(substring))] == substring:
            count = count + 1

    return count
```
