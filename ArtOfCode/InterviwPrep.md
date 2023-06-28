# Intervew Prep

## Links

- [Sys Design](https://www.educative.io/courses/grokking-the-system-design-interview/B8nMkqBWONo#Step-1:-Requirements-clarifications)

- [Interview Preparation Guide from Dan783](https://docs.google.com/document/d/1RLc8Gbljbg9OtteJ7Mn0xsOPJJIg4AGVsf0F6mCpvNA/edit?hl=uk)

- [Dan Behavioural Preparaiton Gudie from Dan783](https://docs.google.com/document/d/1meEAkcopHPjiH7jThyVfnzVHHpnETJ4UxLz1Xsbr958/edit?hl=uk)

- [System Design Prime](https://github.com/donnemartin/system-design-primer)

## Wojtek recomendation.
- Build...Build... 
- Experience....
- Find application that you patianted

## D J recomendations:
- Program for Microsoft mentors.

apinterest program SF, Atlanta, New York 3 round Fit interview. 
Data specialist. 1-10 job suite. Data in AI team. Good feed.  
Deployment web contact 

StartUp Hands on Scaling bussiness. 
Find job at StartUP to have hand's on exprience


## Dan783

1. Resume Guide
2. Guide on Interview

Coding -
> See how Think
Behivoural

SysDesign

> Need template

Write on Coding inter

> time complexity 
> Space Complexity


May I code it. 


>I code exactly what he support


My Time complexity should match the one I named


#B:\Temp\Coding Mock Interview： Product of Array Except for Self (with Google Software Engineer) [riBWq1DvVb8].mp4# Finale ???

Testing 
Let's test it up


🛑 Watch after time.
`5-10` to test it out.

```python
[]
[0,1]
[-5,-15]
[1,0,-1]
```
I am compiler 

Line by line because anexity. 
If I found a problem and I fix it.
Write comments near by about the values.

Keep Talking

Max 120 tasks

Make a good list of Solutions

Behavioural questions are more complexity 

> Backbone

Remember The Step by Step guide.
If we do like second case.

I can end-up in team I wan't to get.
In one year I can switch the team.

❗❗❗ Train **FOCUS** Hell 

print(


**Goal Develop skills**

3 month = 4 hours


Found a job.

Make on Djini. 

0. Do minimal actions.
1. Submit all appliation.
2. EPAM.

1. Luxosoft.
2. DataArt.
3. MakePost in LinkedIn.

Back by Data.
Just do it.


## Another call with Dan


You can write. You should write. 

Bad question.  Ask one bad question 

I should ask about dublicates. 

# 1 Write down notes/task (not all questiuon asked]
 - no writing in teses 
 - Writing time and space 
# 2 Ask clarification questions
# 3 Propose solutions + write down in short words + time complexity + space complexity
# 4 Ask to code
# 5 Code approved solution with explanation along 
# 6 Perform a dry run with a simple case

+  Listen more.  
Train by hour 


Don't jup to code withoug discussion.  

Don't use other's work thone. 


NO ASSUMPTION - Ask question. 

I missed signature methos. Pay attention 

Verbalie talk through the task. 

Don't is there mistake shou'd I preciede.  


Dry run. To much time for explaining time. 


⌚ time. Time to talk to avoid.  

Timing 

# Write all code together. And made dry Run.  Let's just assume. 


Let's assume this method exist. 


Binary Search =  

Не писати додаткову. А потім .

```python
Given a sorted array and a number, count how many times this number occurs in the array.

Examples:
array = [1,1,2,5,5,5,7], n=5, output=3   
array = [3,5,5,5,5,5,5,5,6], n=5, output=3 

# Binary LOw High
# TC: O(logN)
# SC: O(1)


def binarySortedCount(arr,n) -> int:
  lm,rm = 0,len(arr)-1
  
  #Left Min
  l,r = lm,rm
  i = lm
  while i>0 and l!=r:
    i = (r-l)//2 
    num = arr[i]
    if n>num:
      l = i
    elif n<num:
      r =i
    else:
  if lm==rm:
    return 1
  return rm-lm+1


Binary Tree:

     1            <---
   /   \
  2     3         <---
   \  
   5              <---

Answer: [1, 3, 5]

     1            <---
   /   \
  2     3         <---
   \   /
   5   4          <---
Answer: [1, 3, 4]
  
Simple BFS
#TC: O(N)
#SC: O(N) 

from collecions import deque

def righSideOfTree(root:BinaryNode) -> [int]:
  
  if root==None:
    return []
  
  queue = deque([root])  
  res,nl = [],[]
  
  while len(queue)>0: #2
    elem = queue.popleft() # root [3,5]
    
   	if elem.left:
      nl.append(elem.left) # nl = [2,3]
   	if elem.right:
      nl.append(elem.right) #nl [3,5,5]
      
    if len(queue)==0:
      res.append(elem.val) #res [1]
      queue.append(nl)  #queue [2,3]
      nl =[]
  
  return res 
  
  # 3 Axis of Evil in Meta
  # 0 Problem Solving
  
  # 1 Coding is *bad*
  # 1 A bit more compact 
  
  
  # 3 How Good did you coded
  # 4 How you gove throug
  # 5 Communication 
  
  
  # 5 Really anoyed with **ADHD**
  # 5 Not be all over of place look more 
  
  # Bad NL 
  # Work on snippets 
  # Communicaiton is good
  # Coding communication is haotic really really really bad.
  # Take all easy taks fast   
  
  # Sport programming
  # Behaviour 
  
  # Pramt.com Interview web page 
  
  # Fight anexiety did 30 Interview
  # Binary Search -> Automtiation 
  
# pramp.com
# All competition with a team
# 10-15 topic and you can solve each 
# pamp.com
```
```

## Dan BFS/DFS/DP

- Number of Islands

-  DP is Recursion + Memorization 

- ❗Module can bee 10000000+7  or 10**9

- `@lru_cache` We use it a lot

