# Operators
## Precedence Table
| Precedence | Operator                         | Description                     |
|------------|----------------------------------|---------------------------------|
| 1          | `.`                              | Apply operator                  |
| 3          | `()`, `:`, `::`                  | Function call, index, map index |
| 4          | `not`                            | Logical not                     |
| 5          | `*`, `/`, `%`                    | Multiplication, division, mod   |
| 6          | `+`, `-`                         | Addition, subtraction           |
| 7          | `==`, `!=`, `<`, `<=`, `>`, `>=` | Comparison                      |
| 8          | `and`                            | Logical and                     |
| 9          | `or`                             | Logical or                      |


## Arithmetic Operators
```aurora
1 + 1 # 2
1 - 1 # 0
1 * 1 # 1
1 / 1 # 1
1 % 1 # 0
```
## Comparison Operators
```aurora
1 == 1 # true
1 != 1 # false
1 < 1 # false
1 <= 1 # true
1 > 1 # false
1 >= 1 # true
```
## Logical Operators
```aurora
true and false # false
true or false # true
not true # false
```
## Apply Operator
The apply operator (`.`) is used to call a function on a value.
It basically re-orders it's operands, so `f.g(x)` is equivalent to `g(f, x)`.
The parentheses are optional if the function takes only one argument.
```aurora
fn plus_one num -> num + 1
print 1.plus_one # 2

fn add num1, num2 -> num1 + num2
print 1.add(2) # 3
```
## Function Call Operator
The function call operator (`()`) is used to call a function.
It has a comma-separated list of arguments inside the parentheses.
```aurora
fn plus_one num -> num + 1
print plus_one(1) # 2
```

## Index Operator
The index operator (`:`) is used to index a list or map.
```aurora
a = [1, 2, 3]
print a:0 # 1
print a:1 # 2
print a:2 # 3

m = {
    foo -> 2, bar -> 4
    baz -> 6
}
print m:"foo" # 2
```
## Map Index Operator
The map index operator (`::`) is used to index a map without quotes.
```aurora
m = {
    foo -> 2, bar -> 4
    baz -> 6
}
print m::foo # 2
```