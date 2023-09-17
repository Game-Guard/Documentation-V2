# Ingoring Next Check
This function allows you to initialize Game Guard.

## Parameters:

| Parameter      | Description                                          | Type   |
| -------------- | ---------------------------------------------------- | ------ |
| plr            | The player object in which to ignore next check for. | Player |
| ignoreNextEnum | The check to ignore.                                 | Enum   |

## Example Usage:

```lua hl_lines="5" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:ignoreNextCheck(plr, gameGuard.Enums.IgnoreNext.WalkSpeed)
end)
```
