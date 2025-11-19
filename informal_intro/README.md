### Numbers

int and float.

 3 / 2 returns float and 3 // 2 would omit decimal values

### Strings

**immutable** cant be changed.

create a new string by getting values from old string as 'hello' + old_s[3:]

### Lists

simple assignment does not create a copy.

```
rgb = ["Red", "Green", "Blue"]
rgba = rgb
id(rgb) == id(rgba)  # they reference the same object

rgba.append("Alph")
rgb 
```
Both refer to same assignment, so create a copy to change like

```
correct_rgba = rgba[:]
correct_rgba[-1] = "Alpha"
correct_rgba

rgba
```
