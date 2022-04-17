# Logic Operators and Booleans

All logic components are based on boolean algebra. There are only two states - either "true" or "false". I'll provide the boolean comparison operators used in TagScript down below...

## Equal
``==``
```diff
Checks if the object on the left side is the same as the one on the right - returns true if they match and false if not
+ Examples:
"hello" == "hello"      --> returns true
true == true            --> returns true
0 == 2                  --> returns false
"this" == "that"        --> returns false
```