# Math

Math blocks are obviously used for basic to intermediate math. The syntax for each math block is:
``{math:operation}`` or ``{m:operation}``

## Basics

### Operations
```diff
 +           --> addition
 -           --> subtraction
 *           --> multiplication
 /           --> division
 %           --> modulo
 ^           --> exponent
+ Examples:
{math:5+5}      --> returns 10
{math:10%3}     --> returns 1
{m:3^3}         --> returns 27
```

### Functions
```diff
abs()           --> absolute value
round()         --> rounded to the nearest integer
trunc()         --> truncates the number (chops off decimals)
+ Examples:
{math:abs(-10)}     --> returns 10
{math:round(5.6)}   --> returns 6
{m:trunc(5.6)}      --> returns 5
```

## Advanced

### Constants
Side note: constants are not case sensitive
```diff
pi              --> equal to 𝜋
e               --> equal to Euler's number
+ Exmaples:
{math:PI}       --> returns 3.141592653589793
{m:e}           --> returns 2.718281828459045
```

### Functions
```diff
sin()           --> sine of a radian
cos()           --> cosine of a radian
tan()           --> tangent of a radian
exp()           --> Euler's number raised to the power of the supplied number
sgn()           --> sign of a number (1 for x > 0; 0 for x = 0; -1 for x < 0)
log()           --> logarithm with base 10
ln()            --> logarithm with base e (Euler's number)
log2()          --> logarithm with base 2
+ Examples:
{math:sin(math:pi)}     --> returns 0
{math:sgn(-5)}          --> returns -1
{m:log(10)}             --> returns 1
```