# Introduction to Aurora
Aurora is a programming language designed for scripting and automation. It is designed to be easy to learn and use, while still being powerful enough to be used for complex tasks.
It's meant to replace shell scripts which have been (mis)used for complex tasks for decades. 

## Features
- Lua/Ruby-like syntax
- Dynamic typing
- Extraordinarily simple

## Example
```aurora
# This is a comment

# This is a subroutine
sub hello name
    print "Hello, ", name, "!"
end

# This is a function
fn add a, b
    return a + b
end

# This is a variable
name = "world"

# This is a top-level call (subroutine or function)
hello name # Hello, world!

print add(1, 2) # cannot call a subroutine like this; only functions
```

## Functions vs. Subroutines
Aurora has two types of top-level calls: functions and subroutines. Functions are called like `add(1, 2)`, while subroutines are called like `print "Hello, world!"`. Functions can be called from anywhere, while subroutines can only be called from the top level. Functions can (and must) return values, while subroutines cannot. Functions are defined with `fn`, while subroutines are defined with `sub`.

## Variables
Variables use scoping like most C-like languages. 
    
```aurora
# This is a global variable
global = "global"

# this is a 'do' block; an anonymous subroutine
do 
    # This is a local variable
    local = "local"
end 
# the 'do' block is called here, as it's at the top level

print global # global
print local # error: undefined variable 'local'
```

## Nil
Aurora has no `null` or `nil` value.
This is why the distinction between functions and subroutines must be made; if a subroutine were to be called from an expression, it would return `nil`, which would be very confusing, as Aurora has no `nil` value.

## Types
Aurora has the following types:
- `str`: a string
- `num`: a number
- `bool`: a boolean
- `list`: a list of values
- `fn`: a function
- `sub`: a subroutine
- `map`: a map of keys to values

