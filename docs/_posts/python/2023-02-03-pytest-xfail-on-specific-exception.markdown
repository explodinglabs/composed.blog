---
layout: post
title: "How to expect a specific exception with Pytest's xfail?"
category: python
permalink: /python/pytest-xfail-on-specific-exception
---

Use `xfail` with the `raises` param.

```python
from pytest import mark

@mark.xfail(raises=RuntimeError)
def test_func() -> None:
    func()
```

While this works, unfortunately it won't let you say exactly _where_ it's expected to be raised in the test.
