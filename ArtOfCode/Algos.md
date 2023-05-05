# Algorithms


![CheetSheet](./res/algo/LeetCodeChatsheet.png)

![Math Secret](./res/MathSumSecret.jpg)

## Outline

- [Stack and Queue](#stack--queue)
- [Stack](#stack)
- [Problems](#problems)
  - [20 Valid Parentheses](#20-valid-parentheses)
- [Queue](#queue)
- [Greedy](#greedy)
- [Dynamic programming](#dynamic-programming)
    - [Types](#types)


## Links

- [LeetCode Top Interview Questions](https://tinyurl.com/38hh47up)
- [LeetCode DS&Algo Crash Course](https://tinyurl.com/yvrv5znb)
- [NeetCode 150](https://neetcode.io/practice)
- [Tech Interview Handbook](https://yangshun.github.io/tech-interview-handbook/)

## Courses

### LeetCode Algo&DSA

**25-50 hours** - To complete the course

[Course link](https://tinyurl.com/yvrv5znb)

![Leet Code Crash Couse](./res/leetcode/CrashCouse.png)

## Array & String


### Sliding Window

![Sliding Window Meme](./res/memes/sliding-window.gif)

![Sliding window](./res/algo/sliding-window.gif)


- [Amotized Analysis](https://en.wikipedia.org/wiki/Amortized_analysis)

#### Code Example

```python
def sldidingWindow(arr):
    left = ans =curr = 0

    def windowCondition(arr,start,end):
        return True #here is some logic of this condition

    for right in range(len(arr)):
        # do logic with particular sliding window

        while windowCondition(arr,left,right):
            left+=1
        #update answ

    return ans
```

## Stack & Queue

**FIFO** (**F**irst **I**n **F**irst **O**ut) and **LIFO** (**L**ast **I**n **F**irst **O**ut) are two common data structures. They are used to store data in a specific order. The order is determined by the way the data is added and removed from the data structure.

### Stack

> **Stack** is a **LIFO** data structure. The last element added to the stack will be the first element retrieved from the stack.
 
![AlgoStack](./res/algo/AlgoStack.gif)

```python
# Simple Stack Implementation

class Stack:
    def __init__(self):
        self.items = []
    
    def push(self, item):
        self.items.append(item)
    
    def pop(self):
        return self.items.pop()
    
    def peek(self):
        return self.items[-1]
    
    def is_empty(self):
        return self.items == []
    
    def get_stack(self):
        return self.items
```

#### Problems

- [1065 Index pair of string](https://leetcode.com/problems/index-pairs-of-a-string/description/)
> Super simple I was looking for indexes to remove but it all can be done with pop

##### 20 Valid Parentheses

- [LeetCode](https://leetcode.com/problems/valid-parentheses/)

```python
class Solution:
    def isValid(self, s: str) -> bool:
        Map = {")": "(", "]": "[", "}": "{"}
        stack = []

        for c in s:
            if c not in Map:
                stack.append(c)
                continue
            if not stack or stack[-1] != Map[c]:
                return False
            stack.pop()

        return not stack
```

```python 
def isValid(self, s:str) -> bool
    Map = {")":"(","}":"{","]":"["}
    stack = []

    for c in s:
        if c not in Map:
            stack.append(c)
        elif not stack or stack[-1] != Map[c]:
            return False
        else
            stack pop()
    return not stack
```

### Queue

> **Queue** is a **FIFO** data structure. The first element added to the queue will be the first element retrieved from the queue.
> 

### Heaps(heapq)


**1.5-3.5 hours** - to complite this section

[link](https://tinyurl.com/bdew8u9y)

1. `heapq.heapify(x)` - Transforms a regular list `x` into a heap. In the resulting heap, the smallest element is at the root.
2. `heapq.heappush(heap, ele)` - Pushes the value `ele` onto the heap, maintaining the heap invariant.
3. `heapq.heappop(heap)` - Pops and returns the smallest item from the heap, maintaining the heap invariant.
4. `heapq.heappushpop(heap, ele)` - Pushes `ele` onto the heap and then pops and returns the smallest item from the heap.
5. `heapq.heapreplace(heap, ele)` - Pops and returns the smallest item from the heap, and then pushes the new item `ele`. The value of `ele` can be larger than the replaced item.
6. `heapq.nlargest(n, iterable, key=None)` - Returns the `n` largest elements from the `iterable` in descending order.
7. `heapq.nsmallest(n, iterable, key=None)` - Returns the `n` smallest elements from the `iterable` in ascending order.

```python

# Import important to get info
import heapq

# Our Input can be any array
arr = [1, 5, 8, 3, 2, 9]

# We heapify our array
heapq.heapify(arr)

# To remove and return the smallest element, use heapq.heappop()
smallest = heapq.heappop(arr)
print("Smallest element removed:", smallest)
print("Heap after removing smallest element:", arr)

# To add a new element to the heap, use heapq.heappush()
heapq.heappush(arr, 4)
print("Heap after adding new element:", arr)

# To push a new element onto the heap and then pop and return the smallest item from the heap, use heapq.heappushpop()
smallest_after_push = heapq.heappushpop(arr, 7)
print("Smallest element after pushing 7:", smallest_after_push)
print("Heap after heappushpop:", arr)

# To pop and return the smallest item from the heap, and then push the new item, use heapq.heapreplace()
smallest_replaced = heapq.heapreplace(arr, 6)
print("Smallest element replaced:", smallest_replaced)
print("Heap after heapreplace:", arr)

# To find the n smallest elements in the array, use heapq.nsmallest()
n = 3
n_smallest = heapq.nsmallest(n, arr)
print(f"{n} smallest elements:", n_smallest)

# To find the n largest elements in the array, use heapq.nlargest()
n_largest = heapq.nlargest(n, arr)
print(f"{n} largest elements:", n_largest)
```

## Greedy 

> LeetCode asking to find maximum or minimum value, it is a good sign to use greedy algorithm.
 
**Greedy** is an algorithmic paradigm that builds up a solution piece by piece, always choosing the next piece that offers the most obvious and immediate benefit.

- [LeetCode Problems](https://leetcode.com/tag/greedy/)
- [11 LeetCode](https://leetcode.com/problems/container-with-most-water/)

- [Greedy Algorithm](https://www.geeksforgeeks.org/greedy-algorithms/)
- [TSM(Traveling Salesman Problem)](https://www.geeksforgeeks.org/traveling-salesman-problem-tsp-implementation/)

```python
class Solution:
    def maxArea(self, height: List[int]) -> int:
        max_area = 0
        left, right = 0, len(height) - 1
        while left < right:
            max_area = max(max_area, min(height[left], height[right]) * (right - left))
            if height[left] < height[right]:
                left += 1
            else:
                right -= 1
        return max_area
```
### 





## Dynamic programming

- [LeetCode DP Intro](https://tinyurl.com/ya68vadn)

### Types

- [B-Up(Bottom Up)](https://en.wikipedia.org/wiki/Fibonacci_number)
- T-Dn(Top Down)
- [1D DP](https://tinyurl.com/5xhvxdrn) 
- [2D DP](https://tinyurl.com/2p82kfha)

### Signes it's DP

1. The problem will be asking for an optimal value (max or min) of something, or the number of ways to do something.
    - What is the minimum cost of doing ...
    - What is the maximum profit of ...
    - How many ways are there to ...
2. What is the longest possible ...
    - At each step, you need to make a "decision", and decisions affect future decisions.
    - A decision could be picking between two elements
    - Decisions affecting future decisions could be something like "if you take this element, then you can't take that element in the future"

### Problems

- [70 Climbin Stairs](#### Clibming Stairs)
- [1416 Restore the Array](#restore-the-array)

#### Climbing Stairs

- [link](https://leetcode.com/problems/climbing-stairs/)

##### Solution


![Fi Formual](./res/FiFormula.png)

```python
class Solution:
    def climbStairs(self, n: int) -> int:
        sqrt5 = math.sqrt(5)
        phi = (1 + sqrt5) / 2
        psi = (1 - sqrt5) / 2

        return round((math.pow(phi, n+1) - math.pow(psi, n+1)) / sqrt5)
```

![Fibonachi staris](./res/Fibonacci_climbing_stairs.svg)

#### Restore the array

- [link](https://leetcode.com/problems/restore-the-array/)
