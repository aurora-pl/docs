# Standard Library - Math Functions

## Note
All of these functions are declared under the global `math` object.

## `sin`
```aurora
fn sin num -> num
```
### Description
Returns the sine of the given angle in radians.
### Example
```aurora
print math::sin(0) # 0
print math::sin(1) # 0.8414709848078965
```

## `cos`
```aurora
fn cos num -> num
```
### Description
Returns the cosine of the given angle in radians.
### Example
```aurora
print math::cos(0) # 1
print math::cos(1) # 0.5403023058681398
```

## `tan`
```aurora
fn tan num -> num
```
### Description
Returns the tangent of the given angle in radians.
### Example
```aurora
print math::tan(0) # 0
print math::tan(1) # 1.5574077246549023
```

## `asin`
```aurora
fn asin num -> num
```
### Description
Returns the arc-sine of the given angle in radians.
### Example
```aurora
print math::asin(0) # 0
print math::asin(1) # 1.5707963267948966
```

## `acos`
```aurora
fn acos num -> num
```
### Description
Returns the arc cosine of the given angle in radians.
### Example
```aurora
print math::acos(0) # 1.5707963267948966
print math::acos(1) # 0
```

## `atan`
```aurora
fn atan num -> num
```
### Description
Returns the arc tangent of the given angle in radians.
### Example
```aurora
print math::atan(0) # 0
print math::atan(1) # 0.7853981633974483
```

## `sinh`
```aurora
fn sinh num -> num
```
### Description
Returns the hyperbolic sine of the given angle in radians.
### Example
```aurora
print math::sinh(0) # 0
print math::sinh(1) # 1.1752011936438014
```

## `cosh`
```aurora
fn cosh num -> num
```
### Description
Returns the hyperbolic cosine of the given angle in radians.
### Example
```aurora
print math::cosh(0) # 1
print math::cosh(1) # 1.5430806348152437
```

## `tanh`
```aurora
fn tanh num -> num
```
### Description
Returns the hyperbolic tangent of the given angle in radians.
### Example
```aurora
print math::tanh(0) # 0
print math::tanh(1) # 0.7615941559557649
```

## `asinh`
```aurora
fn asinh num -> num
```
### Description
Returns the inverse hyperbolic sine of the given angle in radians.
### Example
```aurora
print math::asinh(0) # 0
print math::asinh(1) # 0.881373587019543
```

## `acosh`
```aurora
fn acosh num -> num
```
### Description
Returns the inverse hyperbolic cosine of the given angle in radians.
### Example
```aurora
print math::acosh(0) # NaN
print math::acosh(1) # 0
```

## `atanh`
```aurora
fn atanh num -> num
```
### Description
Returns the inverse hyperbolic tangent of the given angle in radians.
### Example
```aurora
print math::atanh(0) # 0
print math::atanh(1) # NaN
```

## `exp`
```aurora
fn exp num -> num
```
### Description
Returns the exponential of the given number.
The exponential function is defined as `e^x`, where `e` is Euler's number (approximately `2.71828`).
### Example
```aurora
print math::exp(0) # 1
print math::exp(1) # 2.718281828459045
```

## `expm1`
```aurora
fn expm1 num -> num
```
### Description
Returns the exponential of the given number minus one.
The exponential function is defined as `e^x`, where `e` is Euler's number (approximately `2.71828`).
### Example
```aurora
print math::expm1(0) # 0
print math::expm1(1) # 1.718281828459045
```

## `ln`
```aurora
fn ln num -> num
```
### Description
Returns the natural logarithm of the given number.
The natural logarithm is the inverse of the exponential function.
### Example
```aurora
print math::ln(1) # 0
print math::ln(2.718281828459045) # 1
```

## `log`
```aurora
fn log num -> num
```
### Description
Returns the base-10 logarithm of the given number.
### Example
```aurora
print math::log(1) # 0
print math::log(10) # 1
```

## `log10`
```aurora
fn log10 num -> num
```
### Description
Returns the base-10 logarithm of the given number.
### Example
```aurora
print math::log10(1) # 0
print math::log10(10) # 1
```

## `log2`
```aurora
fn log2 num -> num
```
### Description
Returns the base-2 logarithm of the given number.
### Example
```aurora
print math::log2(1) # 0
print math::log2(2) # 1
```

## `sqrt`
```aurora
fn sqrt num -> num
```
### Description
Returns the square root of the given number.
### Example
```aurora
print math::sqrt(4) # 2
print math::sqrt(2) # 1.4142135623730951
```

## `cbrt`
```aurora
fn cbrt num -> num
```
### Description
Returns the cube root of the given number.
### Example
```aurora
print math::cbrt(8) # 2
print math::cbrt(2) # 1.2599210498948732
```

## `hypot`
```aurora
fn hypot num, num -> num
```
### Description
Returns the square root of the sum of the squares of the given numbers.
### Example
```aurora
print math::hypot(3, 4) # 5
print math::hypot(2, 2) # 2.8284271247461903
```

## `pow`
```aurora
fn pow num, num -> num
```
### Description
Returns the first number raised to the power of the second number.
### Example
```aurora
print math::pow(2, 3) # 8
print math::pow(2, 0.5) # 1.4142135623730951
```

## `ceil`
```aurora
fn ceil num -> num
```
### Description
Returns the smallest integer greater than or equal to the given number.
### Example
```aurora
print math::ceil(1.5) # 2
print math::ceil(-1.5) # -1
```

## `floor`
```aurora
fn floor num -> num
```
### Description
Returns the largest integer less than or equal to the given number.
### Example
```aurora
print math::floor(1.5) # 1
print math::floor(-1.5) # -2
```

## `round`
```aurora
fn round num -> num
```
### Description
Returns the nearest integer to the given number.
### Example
```aurora
print math::round(1.5) # 2
print math::round(-1.5) # -2
```

## `abs`
```aurora
fn abs num -> num
```
### Description
Returns the absolute value of the given number.
### Example
```aurora
print math::abs(1) # 1
print math::abs(-1) # 1
```

## `NaN`
```aurora
NaN: num
```
### Description
A special value representing "not a number".
### Example
```aurora
print math::NaN # NaN
```
