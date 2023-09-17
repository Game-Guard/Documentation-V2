# Initialization
This function allows you to initialize Game Guard.

## Parameters:

| Parameter | Description                                              | Type   |
|-----------|----------------------------------------------------------|--------|
| plr       | The player object in which to initialize Game Guard for. | Player |

## Example Usage:

```lua hl_lines="5" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
end)
```