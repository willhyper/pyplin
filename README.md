# pipe! 
Write Python the functional way

```python
from pyplin import pipe
from math import sqrt
import numpy as np

v1 = np.array((1, 1))
v2 = np.array((4, 5))

d = v1 - v2
r = pipe(d) | (lambda x : x*x) | sum | sqrt
assert r.value == 5.0
r | print # 5.0
```	
