# Literal Values
Aurora has a few literal values that can be used in expressions.

## String Literals
String literals are surrounded by double quotes (`"`), or backticks (`` ` ``).
There is also a shorthand syntax for string literals, which is the `'` character followed by a single word. It does not have an end delimiter.

```aurora
"Hello, world!" # A string literal
`Hello, world!` # Also a string literal
'hello # Shorthand syntax for string literals, known as a symbol in other languages
```

You can do string interpolation with the `fmt` operator.
It takes a string, with expressions inside curly braces (`{}`).

```aurora
name = "world"
print fmt"Hello, {name}!"
```

## Number Literals
Number literals are pretty standard.
They can be written in decimal, hexadecimal, octal, or binary.
They can also be written in scientific notation.

```aurora
123 # Decimal
0x123 # Hexadecimal
0o123 # Octal
0b101 # Binary
1.23e2 # Scientific notation
```

## Boolean Literals
Boolean literals are either `true` or `false`.

```aurora
true
false
```

## List Literals
List literals are surrounded by square brackets (`[]`).
They can contain any number of values, separated by commas.

```aurora
[1, 2, 3]
```

## Map Literals
Map literals are surrounded by curly braces (`{}`).
They can contain any number of key-value pairs, separated by commas, or newlines.

```aurora
{
    foo -> 2, bar -> 4
    baz -> 6
}
```