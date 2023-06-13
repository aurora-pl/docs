# Standard Library - Misc Functions

## `execute`
```aurora
fn execute str... -> {
    wait_for -> (fn -> num)
}
```
### Description
Executes the given command in a new process.
Returns an object with a `wait_for` method that waits for the process to finish and returns its exit code.

### Example
```aurora
print execute("echo", "Hello, World!")::wait_for() # 0
```

## `times`
```aurora
sub times num, fn
```

### Description
Calls the given function the given number of times.

### Example
```aurora
3.times do i
    print i
end
```

