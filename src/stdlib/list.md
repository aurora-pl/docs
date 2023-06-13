# Standard Library - List Functions

## `len`
```aurora
fn len [any] -> num
```

### Description
Returns the length of the given list.

### Example
```aurora
print len([1, 2, 3]) # 3
```

## `push`
```aurora
sub push [any] any
```

### Description
Adds the given value to the end of the given list.

### Example
```aurora
list = [1, 2, 3]
push list, 4
print list # [1, 2, 3, 4]
```

## `pop`
```aurora
fn pop [any] -> any
```

### Description
Removes and returns the last element of the given list.

### Example
```aurora
list = [1, 2, 3]
print pop(list) # 3
print list # [1, 2]
```

## `shift`
```aurora
fn shift [any] -> any
```

### Description
Removes and returns the first element of the given list.

### Example
```aurora
list = [1, 2, 3]
print shift(list) # 1
print list # [2, 3]
```

## `unshift`
```aurora
sub unshift [any] any
```

### Description
Adds the given value to the beginning of the given list.

### Example
```aurora
list = [1, 2, 3]
unshift list, 0
print list # [0, 1, 2, 3]
```

## `join`
```aurora
fn join [any], str -> str
```

### Description
Returns a string containing the elements of the given list joined by the given separator.

### Example
```aurora
print join([1, 2, 3], ", ") # "1, 2, 3"
```

## `map`
```aurora
fn map [any], (fn any -> any) -> [any]
```

### Description
Returns a new list containing the results of applying the given function to each element of the given list.

### Example
```aurora
print map([1, 2, 3], lambda x -> x * 2) # [2, 4, 6]
```

## `map!`
```aurora
sub map! [any], (fn any -> any)
```

### Description
Applies the given function to each element of the given list.

### Example
```aurora
list = [1, 2, 3]
map! list, lambda x -> x * 2
print list # [2, 4, 6]
```

## `filter`
```aurora
fn filter [any], (fn any -> bool) -> [any]
```

### Description
Returns a new list containing the elements of the given list for which the given function returns true.

### Example
```aurora
print filter([1, 2, 3], lambda x -> x % 2 == 0) # [2]
```

## `filter!`
```aurora
sub filter! [any], (fn any -> bool)
```

### Description
Removes all elements from the given list for which the given function returns false.

### Example
```aurora
list = [1, 2, 3]
filter! list, lambda x -> x % 2 == 0
print list # [2]
```

## `reduce`
```aurora
fn reduce [any], any, (fn any any -> any) -> any
```

### Description
Applies the given function to each element of the given list, accumulating the result.

### Example
```aurora
print reduce([1, 2, 3], 0, lambda x y -> x + y) # 6
```

## `upTo`
```aurora
fn upTo num -> [num]
```

### Description
Returns a list of numbers from 0 up to the given number.

### Example
```aurora
print upTo(3) # [0, 1, 2, 3]
```

## `downTo`
```aurora
fn downTo num -> [num]
```

### Description
Returns a list of numbers from the given number down to 0.

### Example
```aurora
print downTo(3) # [3, 2, 1, 0]
```
