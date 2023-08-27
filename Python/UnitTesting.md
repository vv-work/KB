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

# Top Python Unit Testing Frameworks 🐍

1. **unittest** 📦
    - **Built into the Python standard library**. Comprehensive testing suite including fixtures and mock objects.
    ```python
    import unittest

    class TestDemo(unittest.TestCase):
        def test_example(self):
            self.assertEqual(1 + 1, 2)
    ```

2. **pytest** 🚀
    - Powerful features in a **no-boilerplate format**. Provides fixtures, parameterized testing, and a rich ecosystem of plugins.
    ```python
    def test_example():
        assert 1 + 1 == 2
    ```

3. **nose2** 👃
    - Successor to `nose`. Extends `unittest` for **easy test discovery** and a variety of plugins.
    ```python
    def test_example():
        assert 1 + 1 == 2
    ```

4. **doctest** 📖
    - Embed tests within your documentation. Good for **verifying examples in docstrings**.
    ```python
    def add(a, b):
        """
        >>> add(1, 2)
        3
        """
        return a + b
    ```

5. **Hypothesis** 💡
    - Property-based testing tool. **Descriptive testing** rather than specific inputs.
    ```python
    from hypothesis import given
    from hypothesis.strategies import integers

    @given(integers(), integers())
    def test_ints_are_commutative(x, y):
        assert x + y == y + x
    ```

6. **Tox** 🧪
    - **Test code under multiple Python environments**. Ensures compatibility.
    - Configuration-based, usually defined in `tox.ini`.

7. **unittest.mock** 🎭
    - Allows you to **mock objects** in your tests. Isolate tests from external factors.
    ```python
    from unittest.mock import Mock
    
    mock = Mock()
    mock.method.return_value = 'mocked_value'
    ```

8. **Factory Boy** 🏭
    - Set up complex objects in tests. Often used with **Django or SQLAlchemy**.
    - More configuration-based and often used with models.

9. **VCR.py** 📼
    - Records HTTP interactions and replays them. Great for **testing external API calls**.
    ```python
    import vcr

    @vcr.use_cassette('path_to_cassette')
    def test_api_call():
        response = make_api_call()
        assert response == 'expected_value'
    ```

10. **Testify** 👩‍⚖️
    - More feature-rich alternative to `unittest`. Includes **fixtures, matchers, and plugins**.
    ```python
    from testify import TestCase, assert_equal

    class TestExample(TestCase):
        def test_example_method(self):
            assert_equal(1 + 1, 2)
    ```


