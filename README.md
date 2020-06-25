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
