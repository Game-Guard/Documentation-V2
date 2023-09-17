# Renaming Services
This function allows you to call a loop that will rename services and if an argument is provided, it will rename them every amount of time you inputted.

## Parameters:

| Parameter       | Description                                                     | Type |
| --------------- | --------------------------------------------------------------- | ---- |
| time (optional) | The time between each rename services, default renames it once. | Int  |

## Example Usage:

```lua hl_lines="3" linenums="1"
local gameGuard = require(script.Parent.GameGuard)

gameGuard:renameServices(3) -- Will rename services for the player every 3 seconds.
```
