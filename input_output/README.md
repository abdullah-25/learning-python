## write/read a file

to read a file, use 

```
with open('workfile', encoding="utf-8") as f:
    read_data = f.read()

# We can check that the file has been automatically closed.
f.closed
```

use **with** as this closes the file automatically when operation is complete on file

**open** returns a file object

good pracctice is to read file line by line to save memory

```
for line in f:
    print(line, end='')
```



## JSON - json.dumps() and json.load()

writng to text/string file is easy, numbers are more complex and so is other types like list, dict etc.

To solve this issue, we can convert file content to JSON by serilaizing:

```
import json
x = [1, 'simple', 'list']
json.dumps(x)
```

and then deseralize after operation is complete

```
x = json.load(f)
```