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

## `set_dir`
```aurora
sub set_dir str
```

### Description
Sets the current working directory to the given path.

### Example
```aurora
set_dir "/home/user"
```

## `get_dir`
```aurora
fn get_dir -> str
```

### Description
Returns the current working directory.

### Example
```aurora
print get_dir() # /home/user
```

## `in_dir`
```aurora
sub in_dir str, callable
```

### Description
Sets the current working directory to the given path, calls the given callable, and then restores the previous working directory.

### Example
```aurora
set_dir "/foo/bar"
print get_dir() # /foo/bar

in_dir "/home/user" do
    print get_dir() # /home/user
end

print get_dir() # /foo/bar
```
