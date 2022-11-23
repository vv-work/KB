# Pip Packges

Here I will put all *not essential* packages with there use casses

## Image Magic


`pip install wand`

```python
from wand.image import Image
 
ny = Image(filename ='new york.jpg')
```
### Convert JPG to PNG

```python
from wand.image import Image
 
ny = Image(filename ='new york.jpg')
ny_convert = ny.convert('png')
ny_convert.save(filename ='converted new york.png')
```
