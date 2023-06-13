# Standard Library - Type Functions

## `num`
```aurora
fn num any -> num
```
### Description
Converts the given value to a number.
Otherwise, returns `math::NaN`.
### Example
```aurora
print num("123") # 123
print num("abc") # NaN
```

## `str`
```aurora
fn str any -> str
```
### Description
Converts the given value to a string.
### Example
```aurora
print str(123.4) # 123.4
```

## `type_of`
```aurora
fn type_of any -> str
```
### Description
Returns the type of the given value as a string.
### Example
```aurora
print type_of(123) # "num"
print type_of("abc") # "str"
```

## `is?`
```aurora
fn is? any, str -> bool
```
### Description
Returns `true` if the given value is of the given type, `false` otherwise.
### Example
```aurora
print is?(123, 'num) # true
print is?(123, 'str) # false
```