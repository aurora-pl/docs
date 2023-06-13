# Standard Library - File Functions

## `copy!`
```aurora
sub copy! str str
```
### Description
Copies a file from one path to another.
Will overwrite the destination file if it already exists.
### Example
```aurora
copy! `file.txt`, `file2.txt`
```

## `copy`
```aurora
fn copy str str -> bool
```
### Description
Copies a file from one path to another.
Will not overwrite the destination file if it already exists.
Returns `true` if the file was copied, `false` otherwise.
### Example
```aurora
copy `file.txt`, `file2.txt`

# error-checking
unless copy(`file.txt`, `file2.txt`)
    print "Failed to copy file!"
end
```

## `move!`
```aurora
sub move! str str
```
### Description
Moves a file from one path to another.
Will overwrite the destination file if it already exists.
### Example
```aurora
move! `file.txt`, `file2.txt`
```

## `move`
```aurora
fn move str str -> bool
```
### Description
Moves a file from one path to another.
Will not overwrite the destination file if it already exists.
Returns `true` if the file was moved, `false` otherwise.
### Example
```aurora
move `file.txt`, `file2.txt`

# error-checking
unless move(`file.txt`, `file2.txt`)
    print "Failed to move file!"
end
```

## `delete!`
```aurora
sub delete! str
```
### Description
Deletes a file.
### Example
```aurora
delete! `file.txt`
```

## `new!`
```aurora
sub new! str
```
### Description
Creates a new file.
Will overwrite the file if it already exists.
### Example
```aurora
new! `file.txt`
```

## `new`
```aurora
fn new str -> bool
```
### Description
Creates a new file.
Will not overwrite the file if it already exists.
Returns `true` if the file was created, `false` otherwise.
### Example
```aurora
new `file.txt`

# error-checking
unless new(`file.txt`)
    print "Failed to create file!"
end
```

## `exists?`
```aurora
fn exists? str -> bool
```
### Description
Returns `true` if the file exists, `false` otherwise.
### Example
```aurora
if exists?(`file.txt`)
    print "File exists!"
end
```

## `write!`
```aurora
sub write! str str
```
### Description
Writes a string to a file.
Will overwrite the file if it already exists.
### Example
```aurora
write! `file.txt`, "Hello, world!"
```

## `write`
```aurora
fn write str str -> bool
```
### Description
Writes a string to a file.
Will not overwrite the file if it already exists.
Returns `true` if the file was written to, `false` otherwise.
### Example
```aurora
write `file.txt`, "Hello, world!"
   
# error-checking
unless write(`file.txt`, "Hello, world!")
    print "Failed to write to file!"
end
```