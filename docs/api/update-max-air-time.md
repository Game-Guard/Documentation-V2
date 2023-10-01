# Update Max Air Time

This functions sets the amount of time that a player can be in the air for before being detected.

## Parameters:

| Parameter  | Description                                                        | Type   |
| ---------- | ------------------------------------------------------------------ | ------ |
| plr        | The player object of which to get the times triggered for.         | Player |
| maxAirTime | The amount of time in seconds that a player can be in the air for. | Int    |

## Example Usage:

```lua hl_lines="6" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    gameGuard:updateMaxAirTime(plr, 5)
end)
```