# Python

## Indexing


<!-- vim-markdown-toc GFM -->

  * [User Input](#user-input)
    * [List comperhansions](#list-comperhansions)
    * [Slicing a list](#slicing-a-list)
    * [Copy array](#copy-array)
    * [Logic](#logic)
    * [Dictionary](#dictionary)
* [Functions](#functions)
    * [Undeifined number for argum,ents](#undeifined-number-for-arguments)
    * [For dictionairies](#for-dictionairies)
* [Soring](#soring)

<!-- vim-markdown-toc -->

[images](CheatSheet/index.md)


### User Input

```python
name = input("what's your name? ")
print(name)
```


#### List comperhansions
```python
squars= [x**2 for x in range(1,11)]
print(squars)
```
>ouput: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
#### Slicing a list 
```python 
fishers = ['sam','bob','ada','bea']
first_two=fishers[:2]
print(first_two)
```
>output: [sam,bob]

#### Copy array

```python
copy_of_bike = bikes[:] # making list
```

#### Logic

```python
'trey' in bikes # Array contains
'some' not in bikes # Array not contins

logic = True

if logic or False:
    print("some logic")
elif age>=18  and True:
    print("You have 18")
else:
    print("Nothing")


list = ['a','b']
print("start loop")
while list:
    x = list.pop()
    print(x)
print("end loop")


```

#### Dictionary

```python
alien = {'color':'green', 'points':5}   #create dictionary
alien['x_position'] = 0                 #new value
print(f'alian color is{alien['color']}')

 far_numbers = {'eric' :17, 'ever' :4}
 for name,number in far_numbers.items():
     print(name + ' loves ' + str(number))
 for name in far_numbers.keys():
     print(name))
```
>output : green
>eric loves 17
>ever loves 4
>eric
>ever


## Functions

```python 
# Simple
def greetUser(name="User"):
    """Diplay a simple greeting."""
    print(f"Hello! {name}")

greetUser()
```

#### Undeifined number for argum,ents
```python 
def make_pizza(size, *toppings):
    print(f'\n Make a {size} pizza.\n with toping')
    for t in toppings:
        print(f'- {t}')
make_pizza('small','papperoni','becon','ananas')
```
>Output:
> Make a small pizza.
> with toping
>- papperoni
>- becon
>- ananas

#### For dictionairies
 `**toppings`not `*toppings`

```python
def make_pizza(size, **toppings):
 ```
 #### Module

 If we save our code in `pizza.py`
 Then we would be able to do
 ```python
 import pizza
 
 pizza.make_pizza("small","brokoli","sparge")
 ```
 or other way around would be to do:
 ```python
 from pizza import make_pizza 
 ```
 or even:
```python
 import pizza as  p
 p.make_pizza("big","meet")
 ```
 or importing all with
```python
from pizza import *
 make_pizza("big","meet")
 ```
## Soring

`arr.sort()` - gives me sorted array


