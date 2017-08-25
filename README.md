# pipe! 
## Write Python the functional way

from pyplin import pipe

from math import sqrt, fsum

def sq(n):
    return n * n


def diff(a, b):
    return tuple(ea - eb for ea, eb in zip(a, b))


v1 = (1, 1)

v2 = (4, 5)

d = diff(v1, v2)

**r = pipe(d) | sq | sum | sqrt**

**assert r.value == 5.0**

**r | print**
	
