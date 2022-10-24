# Data Structes & Algoirthms in Python

## Links

- [Data Structures in Chriss Notes](https://chrisalbon.com/code/python/basics/data_structure_basics/)

## Data Structuress 

### Built-In Data types

- Lits
- Sets
- Dictionary
- Tuple

#### Set


#### Dictionary

```py
dic = dict()
dic['a'] = 5

if 'a' in dic:
	dic['a']= dic['a'] +1

```

### Stack&Queue

[Chris Albon Notes](http://localhost/ChrisNotes/python/basics/queues_and_stacks/)

### Set

Is like Hash set but a bit more complicated


```python	
BRI = set(['brazil','canada','ukraine']

if 'brazil' in BRI:
	print('We have Brazil')
BRI.add('china')
BRI.remove('brazil')
BRIC = BRI.copy()
```

### Dictionary

```python
staff	{'Chris': 'chris@gmail.com',
	 'Jake' : 'jake@gmail.com',
	 'Tom'  : 'tom@gmail.com'
	}
staff['Tom']
# Deleting based on the key
del staff['Tom'];staff 
# Add entry 
Staff['Guido'] = 'guido@gmail.org;
```
