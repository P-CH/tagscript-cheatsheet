# Conditional Statements

Conditional Statements are used when an action is only supposed to happen when a certain condition is met. Therfore, these statements rely on [boolean comparisons](https://github.com/P-CH/tagscript-cheatsheet/blob/master/logic/ "Boolean Comparisons explained").

#### General Structure of a Conditional Block
``{type(boolean):then|else}``
Unfortunately, you cannot just supply "true" or "false" as boolean, it always needs to be a comparison "made on the fly".

## If
```diff
Checks if a single condition is met. If so, it continues with the "then-part" of the statement and if not, with the "else-part".
+ Examples:
{if("this" == "this"): this executes| this never executes}
{if(0 == 1): this never executes| this executes}
{if(3 > 1): this executes| this never executes}
```
