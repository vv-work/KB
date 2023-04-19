# Algorithms

![CheetSheet](./res/algo/LeetCodeChatsheet.png)

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

- [LeetCode Top Interview Questions](https://leetcode.com/explore/interview/card/top-interview-questions-easy/)
- [LeetCode DS&Algo Crash Course](https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course/)
- [NeetCode 150](https://neetcode.io/practice)
- [Tech Interview Handbook](https://yangshun.github.io/tech-interview-handbook/)

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

### Greedy 

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

### Types


- [Fibonachi numbers](https://en.wikipedia.org/wiki/Fibonacci_number)
- [LeetCode DP Intro](https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course-data-structures-and-algorithms/712/dynamic-programming/4539/)
- [1D DP](https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course-data-structures-and-algorithms/712/dynamic-programming/4541/) 
- [2D DP](https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course-data-structures-and-algorithms/712/dynamic-programming/4542/)


