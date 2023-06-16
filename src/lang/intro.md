# Introduction to Aurora

Aurora is a powerful yet remarkably simple programming language designed for scripting and automation. With its Lua/Ruby-like syntax and dynamic typing, Aurora offers an easy learning curve for users while enabling them to tackle complex tasks efficiently. It aims to replace the long-standing (mis)use of shell scripts for intricate operations.

## Features

- **Lua/Ruby-like syntax:** Aurora adopts a syntax reminiscent of popular scripting languages Lua and Ruby, making it familiar and approachable to developers.
- **Dynamic typing:** The language supports dynamic typing, allowing variables to hold values of different types throughout their lifetime.
- **Extraordinarily simple:** Aurora prioritizes simplicity, emphasizing straightforwardness and ease of use.

## Example

```aurora
# This is a comment

# This is a subroutine
sub hello(name)
    print fmt"Hello, {name}!"
end

# This is a function
fn add(a, b)
    return a + b
end

# This is a variable
name = "world"

# This is a top-level call (subroutine or function)
hello name # Hello, world!

print add(1, 2) # Cannot call a subroutine like this; only functions
```

## Functions vs. Subroutines

In Aurora, there are two types of top-level calls: functions and subroutines.

- **Functions:** Functions are called using the syntax `function_name(arguments, ...)`. They can be invoked from anywhere in the program, including within expressions. Functions can return values and are defined using the `fn` keyword.
- **Subroutines:** Subroutines are called using the syntax `subroutine_name arguments, ...`. They can only be called from the top level of the program and cannot be invoked within expressions. Subroutines do not return values and are defined using the `sub` keyword.

## Variables

Aurora employs scoping rules similar to those found in most C-like languages.

```aurora
# This is a global variable
global = "global"

# This is a 'do' block; an anonymous subroutine
do 
    # This is a local variable
    local = "local"
end 

# The 'do' block is called here, as it's at the top level

print global # Output: global
print local # Error: undefined variable 'local'
```

## Nil

In Aurora, the absence of a nil value means that functions must always return a value. Consequently, when a function does not have a specific value to return, it is declared as a subroutine. By designating such functions as subroutines, Aurora ensures clarity and avoids confusion. Subroutines are meant to execute actions or operations without returning a value, highlighting their purpose of performing tasks rather than producing specific outputs. This distinction allows developers to write more precise and understandable code, enhancing code organization and reducing potential errors related to missing or unexpected return values.

## Types

Aurora includes the following types:

- `str`: Represents a string of characters.
- `num`: Represents a numeric value.
- `bool`: Represents a boolean value (`true` or `false`).
- `list`: Represents a collection of values.
- `fn`: Represents a function.
- `sub`: Represents a subroutine.
- `map`: Represents a mapping of keys to values.

Aurora's concise syntax and simplicity make it an appealing choice for scripting and automating tasks efficiently.

## Aurora vs. Shell
Aurora outshines traditional shell scripting with its focus on readability and simplicity. Its intuitive syntax, plain English function names, and clean structure enhance code comprehension. Aurora's built-in functions and higher-level abstractions simplify complex tasks, reducing convoluted command chains. This results in concise, straightforward code that is easier to understand and maintain. By prioritizing readability and simplicity, Aurora offers an approachable and error-resistant scripting experience, boosting productivity.
```bash
#!/bin/bash

directory="/path/to/directory"

echo "Listing files in $directory:"

for file in "$directory"/*; do
    if [ -f "$file" ]; then
        filename=$(basename "$file")
        size=$(du -sh "$file" | awk '{print $1}')
        echo "File: $filename | Size: $size"
    fi
done
```
```aurora
#!/bin/aurora

directory = "/path/to/directory"

print fmt"Listing files in {directory}:"

for file, dir(directory)
    if not isDir(file)
        print fmt"File: {basename(file)} | Size: {size(file, 'kb)}"
    end
end
```