## Functions

functions are stored as Objects.

python interpretor when encounters foo(), it does a varaiable reference lookup:
    - first in local table (every func when executed has local table for all variables)
    - enclosing func
    - global
    - built in

Then it retrives **memory address** so foo() -> #1224 etc
This address has all the instructions for function

if only foo then it just retreives, if foo() then it retrives and runs.

Func instructions are stored in **Heap** since memory is needed for as long as program runs
and func reference (memory address) is stored in **stack** since after function finishes, that refrence gets popped and removed from stack


### arguments

2 types:
   - positional
   - keyword

to pass arbitary number of args use -> *args
to pass arbiatary number of kwrgs use -> **kwrgs

```
def concat(*args, sep="/"):
    return sep.join(args)

concat("earth", "mars", "venus")

concat("earth", "mars", "venus", sep=".")

```

PEP8 is offical style guide for python
