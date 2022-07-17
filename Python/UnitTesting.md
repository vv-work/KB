# Unit Testing Python

## Questions 

- Writing Python in vim
- Freamworks list ?
- Mocking ?
- Ide for Running tests

## Unittest

```python
import unittest
import sys

def add(x:int,y:int) -> int:
	return x+y

class TestAdd(unittest.TestCase:

	def testAdd(self):
		self.assertAlmostEqual(11,add(4.482,6.508) places=1)

unittest.main(argv=['ignored', '-v'],exit=False)

```

## Doctest

[Chris Albon Notes](http://localhost/ChrisNotes/python/testing/testable_documentation/)

```python
import doctest

def summation(a,b):
"""
Take two impuit and out theri sum

Tests:

>>> summation(5,4)
9

>>> summation(0,0)
0

>>> summation(5,-6)
-1

>>> summation('foo','bar')
'foobar'


"""
return a+b
```

