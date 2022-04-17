# Conditional Statements

Conditional Statements are used when an action is only supposed to happen when a certain condition is met. Therfore, these statements rely on [boolean comparisons](https://github.com/P-CH/tagscript-cheatsheet/blob/master/logic/ "Boolean Comparisons explained").

#### General Structure of a Conditional Block
``{type(boolean):then|else}``

Unfortunately, you cannot just supply "true" or "false" as boolean, it always needs to be a comparison "made on the fly".
If you dont need an else-statement, you can just leave out the pipe character and the else-statement after it.

## If
```diff
Checks if a single condition is met. If so, it continues with the "then-part" of the statement and if not, with the "else-part".
+ Examples:
{if("this" == "this"): this executes| this never executes}
{if(0 == 1): this never executes| this executes}
{if(3 > 1): this executes| this never executes}
```

## Any/Or
```diff
Checks if at least one of multiple conditions condition is met. If so, it continues with the "then-part" of the statement and if not, with the "else-part".
Different conditions are seperated with the pipe character "|"
+ Examples:
{any("this" == "this" | 0 == 0): this executes| this never executes}        --> both conditions are true
{or(0 == 1 | "hello" == "hey"): this never executes| this executes}         --> neither of the conditions is true
{any(3 != 1 | true == false): this executes| this never executes}           --> the first condition is true
```

## And/All
```diff
Checks if all conditions are met. If so, it continues with the "then-part" of the statement and if not, with the "else-part".
Different conditions are seperated with the pipe character "|"
+ Examples:
{and("this" == "this" | 0 == 0): this executes| this never executes}        --> both conditions are true
{all(0 == 1 | "hello" == "hey"): this never executes| this executes}        --> neither of the conditions is true
{and(3 != 1 | true == false): this never executes| this executes}           --> the first condition is true
```

## Break/Shortcircuit
```diff
Breaks the code if the condition is met, meaning nothing else than the payload gets executed. Therefore, this does not have an else-statement.
+ Examples:
{shortcircuit(1 == 1): only this executes}
{short(true == false:) nothing happens here, the tag will continue like nothing happened}
{break("hey" == "hey"): only this executes}