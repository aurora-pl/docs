# Standard Library - I/O Functions

## `print`
```aurora
sub print any...
```
### Description
Prints the given arguments to the standard output stream, with no separator between them.
### Example
```aurora
print "Hello, ", "world!"
```
## `ask`
```aurora
fn ask str -> str
```
### Description
Asks the user for input and returns it.
### Example
```aurora
name = ask("What is your name? ")
print "Hello, ", name
```
## `read`
```aurora
fn read str -> str
```
### Description
Reads the contents of a file and returns it as a string.
### Example
```aurora
contents = read("file.txt")
print contents
```