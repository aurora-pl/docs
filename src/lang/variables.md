# Variables
Variables in Aurora are defined using no keywords, but just the variable's name and its value.
```aurora
a = 1
```
Variables can be reassigned.
```aurora
a = 1
a = 2
```
Variables can be reassigned to a different type.
```aurora
a = 1
a = "Hello, world!"
```
You can add, subtract, multiply, and divide variables.
```aurora
a = 1
a += 1 # 2
a -= 1 # 1
a *= 2 # 2
a /= 2 # 1
```
Variables are scoped to the block they are defined in, or globally if defined at the top level.
```aurora
a = 1
if true
    a = 2
end
print a # 2

do
    b = 1
end
print b # Error: b is not defined
```

## Constants
Constants are denoted by an uppercase first letter.
```aurora
A = 1
```
Constants cannot be reassigned.
```aurora
A = 1
A = 2 # Error: A is a constant
```