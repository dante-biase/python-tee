# python-tee

python-tee is a simple tool that allows you to simultaneously print output to console and a variable number of files.

# features
- **zero** dependencies
- object oriented and functional implementations
- same function signature as standard print function 
- write and append file modes

# requirements

- Python >= 3.6

# install

```bash
$ pip3 install python-tee
```

# examples

## OOP
```python
from tee import Tee

tee = Tee("output1.log", "output2.log", mode='w')

tee("Hello", "World", sep=', ', end='!')
# >>> Hello, World!
tee()
# >>> ''
tee(1, 2, 3, ['a', 'b', 'c'])
# >>> 1 2 3 ['a', 'b', 'c']

```
```
# output1.log, output2.log
Hello, World!
1  2  3 ['a', 'b', 'c']
```

## Functional
```python
from tee import tee

tee("Hello", "World", sep=", ", end="!", files=["output1.log", "output2.log"], mode='w')
# >>> Hello, World!

```
```
# output1.log, output2.log
Hello, World!
```
