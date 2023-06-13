# Lists
Lists are declared as comma-seperated values between two square brackets.
```aurora
[1, 2, 3]
```

Lists can be indexed using the `:` operator.
```aurora
a = [1, 2, 3]
print a:0 # 1
print a:1 # 2
print a:2 # 3
```

You can assign to a list index.
```aurora
a = [1, 2, 3]
a:0 = 4
print a # [4, 2, 3]
```

See [List Functions](../stdlib/list.md) for functions that operate on lists.