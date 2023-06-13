# Standard Library - Time Functions

## `now`
```aurora
fn now -> {
    year -> num,
    month -> num,
    day -> hour,
    hour -> num,
    minute -> num,
    second -> num
}
```
### Description
Returns the current date and time as an object with the following fields:
- `year` - The current year.
- `month` - The current month.
- `day` - The current day.
- `hour` - The current hour.
- `minute` - The current minute.
- `second` - The current second.

### Example
```aurora
print now() # {year -> 2021, month: 9, day -> 1, hour -> 0, minute -> 0, second -> 0}
```

## `clock`
```aurora
fn clock -> num
```
### Description
Returns the number of milliseconds since the Unix epoch.

### Example
```aurora
print clock() # 1686614986960
```
