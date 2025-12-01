## list

mutable sequences to store collection of items

[list methods api](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists)

to make stack:
    - stack = []
    - stack.append()
    - stack.pop()

to make queue:
   - use deque from collections as its faster
   - queue.popleft()


use list comprehnsion to make code concise

[cond for loop if statetment]


del(obj/vlaue) will delete items from list

## tuple

immmutable data type, build it with () and , like ('Ab' , 26)

## set

for unique items, build using {}

## dictionaries

unique sequence of item:vlaue

- use .get(item) to prevent KeyError if item is not present

## looping technicques

```
knights = {'gallahad': 'the pure', 'robin': 'the brave'}
for k, v in knights.items():
    print(k, v)
```

```
for i, v in enumerate(['tic', 'tac', 'toe']):
    print(i, v) 
```

zip to loop over 2 collections

```
questions = ['name', 'quest', 'favorite color']
answers = ['lancelot', 'the holy grail', 'blue']
for q, a in zip(questions, answers):
    print('What is your {0}?  It is {1}.'.format(q, a))
```

use **sorted()** to sort items as it creates a copy

to loop over unique sorted items

```
basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
for f in sorted(set(basket)):
    print(f)
```

### objects are compared of same types only and it starts with first 2 , then next