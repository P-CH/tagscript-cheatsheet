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
<br>
## Not Equal
``!=``
```diff
Checks if the object on the left side is not the same as the one on the right - returns true if they dont match and false if they do
+ Examples:
"hello" != "hey"        --> returns true
true != false           --> returns true
0 != 0                  --> returns false
"this" != "this"        --> returns false
```
<br>
## Greater Than (Greater Than or Equal)
``>`` or ``>=``
```diff
Greater Than: Checks if the number on the left side is greater than the one on the right - returns true if so and false if not
Greater Than or Equal: Checks if the number on the left side is greater than or equal to one on the right - returns true if so and false if not
+ Examples:
1 > 0                   --> returns true
3 >= 3                  --> returns true
2 > 2                   --> returns false
5 >= 6                  --> returns false
```
<br>
## Less Than (Less Than or Equal)
``<`` or ``<=``
```diff
Less Than: Checks if the number on the left side is less than the one on the right - returns true if so and false if not
Less Than or Equal: Checks if the number on the left side is less than or equal to one on the right - returns true if so and false if not
+ Examples:
1 < 2                   --> returns true
3 <= 3                  --> returns true
2 < 2                   --> returns false
5 <= 2                  --> returns false
```