# Control Flow
Aurora has the control flow you'd expect from a modern language.
It also has a few features that are (somewhat) unique to Aurora.

## If Statements
If statements are pretty standard.

```aurora
if condition
    # do something
end
```

If statements can also have an `else` clause.

```aurora
if condition
    # do something
else
    # do something else
end
```

## Unless Statements
Unless statements are the opposite of if statements.

```aurora
unless condition
    # do something
end
```

Unless statements can also have an `else` clause.

```aurora
unless condition
    # do something
else
    # do something else
end
```

## While Loops
While loops are pretty standard.

```aurora
while condition
    # do something
end
```

## Until Loops
Until loops are the opposite of while loops.

```aurora
until condition
    # do something
end
```

## For Loops
For loops iterate over a list.
For doing something a certain number of times, see [`times`](../stdlib/misc.md#times).
```aurora
for i, upTo(10)
    # do something
end
```

## Break and Continue
Break and continue are pretty standard.

```aurora
while condition
    if condition
        break
    end
    if condition
        continue
    end
end
```

## Switch Statements
Switch statements are pretty standard.

```aurora
switch value
    case 1
        # do something
    case 2
        # do something else
    else
        # do something else
end
```

## Select Statements
Select statements are like a chain of if statements.
```aurora
select
    case condition1
        # do something
    case condition2
        # do something else
    else
        # do something else
end
```

