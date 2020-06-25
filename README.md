# bash
Things to know about bash scripting.

## Return Codes / Exit Statuses
There are return codes in bash also called exit statuses.

Every command returns an a code ranging from 0 to 255.
By convention a zero status code indicates a success.
Documentation on error codes can be found via man.

```
echo "$?"
```
Returns the return code of the previously executed command.

## Chaining commands
There are are different operators to chain commands in bash.

```
;
```
Will execute both commands unless the first one exits.
```
&&
```
Will execute the second command only if the first one succeeded.
```
||
```
Will execute the second command only if the first one fails.
```
|
```
Taking the first commands output as the second commands input.
```
&
```
The second command wont wait for the first one to execute.

## Variable Scope

There are global variables in bash, as well as local variables within functions.

Variables can be declared with a function scope using the *local* keyword.
Otherwise variables are declared in a global scope.

´´´
local VARIABLE
´´´
