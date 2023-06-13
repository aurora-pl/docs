# Functions and Subroutines
In Aurora, functions and subroutines are defined using the `fn` and `sub` keywords, respectively.

## Functions
Functions are defined using the `fn` keyword, followed by the function's name, its parameters, and its body.
It must always return a value.

```aurora
fn add a, b
    return a + b
end

# or, using the shorthand syntax:
fn add a, b -> a + b
```

## Subroutines
Subroutines are defined using the `sub` keyword, followed by the subroutine's name, its parameters, and its body.
Subroutines cannot return a value.
They can return early using the `return` keyword, but it must not be followed by any value.

```aurora
sub say_hi name
    print "Hello, ", name
end

# or, using the shorthand syntax:
sub say_hi name -> print "Hello, ", name
```

## Anonymous Functions and Subroutines
Functions and subroutines can also be anonymous.
They are `do` and `lambda` blocks, respectively.

```aurora
# Anonymous function:
add = lambda a, b -> a + b
# or:
add = lambda a, b
    return a + b
end

# Anonymous subroutine:
say_hi = do name
    print "Hello, ", name
end
```

## Calling Functions and Subroutines
There are two places where functions can be called: in expressions and in statements.
At the top level, functions can be called, just discarding the result.
However, subroutines can only be called in statements, as they produce no result.

```aurora
# Calling a function in an expression:
print add(1, 2) # 3

# Calling a function at the top level:
add 1, 2 # Discards the result, but still executes the function

# Calling a subroutine in a statement:
print "Hello, World!"
```

### Top-Level Calls
Top-level calls don't have to be to a named function or subroutine.
They can also be calls to `do` blocks or `lambda` block expressions, or any other expression (list indexing, for example).

If an expression is at the top level, it is immediately evaluated, and the result must be a callable value.

```aurora
# Calling a do block:
do
    print "Hello, World!"
end  # It is immediately executed, as it's at the top level

foo = [print]
foo:0 "Hello, World!" # Calling a subroutine in a list
```