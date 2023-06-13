# Standard Library - String Functions

## `len`
```aurora
fn len str -> num
```

### Description
Returns the length of the given string.

### Example
```aurora
print len("abc") # 3
```

## `split`
```aurora
fn split str, str -> [str]
```

### Description
Splits the given string into substrings at each occurrence of the given separator and returns them as an array.

### Example
```aurora
print split("a,b,c", ",") # ["a", "b", "c"]
```

## `replace`
```aurora
fn replace str, str, str -> str
```

### Description
Replaces all occurrences of the given substring in the given string with the given replacement.

### Example
```aurora
print replace("abcabc", "a", "x") # "xbcxbc"
```

## `substring`
```aurora
fn substring str num num -> str
```

### Description
Returns the substring of the given string starting at the given index and ending at the given index.

### Example
```aurora
print substring("abc", 1, 2) # "bc"
```
