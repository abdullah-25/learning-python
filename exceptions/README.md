2 types of errors

1) syntax error

2) exceptions

    - when code is executed

handle `exceptions` by:

- start with try
- then except <Exception Name>

good practise is to print each exception, 
handle all other exception in th end by saying

` except Exception as err:`

then raise


```
import sys

try:
    f = open('myfile.txt')
    s = f.readline()
    i = int(s.strip())
except OSError as err:
    print("OS error:", err)
except ValueError:
    print("Could not convert data to an integer.")
except Exception as err:
    print(f"Unexpected {err=}, {type(err)=}")
    raise

```

to define clean up task, use `finally` which runs after try and except block 

```
try:
    raise KeyboardInterrupt
finally:
    print('Goodbye, world!')
```

to raise multiple exceptions use `ExceptionGroup`

```
def f():
    excs = [OSError('error 1'), SystemError('error 2')]
    raise ExceptionGroup('there were problems', excs)

f()












try:
    f()
except Exception as e:
    print(f'caught {type(e)}: e')

```