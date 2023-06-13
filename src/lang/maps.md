# Maps
Maps are a type of collection that store key-value pairs. They are also known as dictionaries or associative arrays in other languages.
In Aurora, maps are surrounded by curly braces (`{}`), and contain key-value pairs separated by commas or newlines.
```aurora
{
    foo -> 2, bar -> 4
    baz -> 6
}
```
Maps can be accessed using either the `:` operator, or the `::` operator.
```aurora
m = {
    foo -> 2, bar -> 4
    baz -> 6
}
print m:"foo" # 2
print m::foo # 2
```
You can assign to a map index.
```aurora
m = {
    foo -> 2, bar -> 4
    baz -> 6
}
m::foo = 3 # or m:"foo" = 3
print m # {foo -> 3, bar -> 4, baz -> 6}
```
See [Map Functions](../stdlib/map.md) for functions that operate on maps.