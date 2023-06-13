# The Standard Library
The standard library is a collection of functions and variables that are distributed with the
Aurora programming language. These items are imported by default in every
Aurora program.

## Conventions
Functions which do a "destructive" operation (i.e. they modify their arguments, manipulate the filesystem in a possibly destructive way, etc.) are suffixed with an exclamation mark (`!`).
Functions which "ask" a question (i.e. they return a boolean value) are suffixed with a question mark (`?`).

## Type Signatures
The type signatures of functions and variables are written in a pseudo-Aurora syntax.
`...` means that the function or variable takes a variable number of arguments.

## Categories
The standard library is divided into these categories:
- [**I/O**](./io.md): Input and output functions.
- [**File**](./file.md): File manipulation functions.
- [**String**](./string.md): String manipulation functions.
- [**Math**](./math.md): Mathematical functions and constants.
- [**Time**](./time.md): Time and date functions.
- [**Type**](./type.md): Type checking and conversion functions.
- [**List**](./list.md): List manipulation functions.
- [**Misc**](./misc.md): Miscellaneous functions.