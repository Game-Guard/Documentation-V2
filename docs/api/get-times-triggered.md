# Get Times Triggered
Gives you a table of times the anti-cheat has been triggered for a specific player.

## Parameters:

| Parameter | Description                                                                 | Type   |
| --------- | --------------------------------------------------------------------------- | ------ |
| plr       | The player object of which to get the times triggered for.                  | Player |

## Example Usage:

```lua hl_lines="6-13" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    local timesTriggered = gameGuard:getTimesTriggered(plr)
    -- Returns:
    -- timesTriggered = {
    --     ["speed"] = 0, The amount of speed detections.
    --     ["jp"] = 0, The amount of jump power detections.
    --     ["nc"] = 0, The amount of no-clip detections.
    --     ["total"] = 0, The total amount of detections.
    -- }
end)
```