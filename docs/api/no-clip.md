# No Clip
This function will allow you to check when a player is no clipping.

## Parameters:

| Parameter         | Description                                           | Type     |
| ----------------- | ----------------------------------------------------- | -------- |
| plr               | The player in which to check if they are no clipping. | Player   |
| hitbox (optional) | The size of the hitbox, an optional parameter.        | Vector3  |
| Result            | The function that will be called every frame.         | function |

## Example Usage:

```lua hl_lines="7-11" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)

    gameGuard:noclip(plr, Vector3.new(1.5, 1.9, 0.8), function(plrToCheck, state, detectionType)
        print(plrToCheck) -- Prints the player who was detected.
        print(state) -- Prints a boolean, true or false based on whether or not the player was detected.
        print(detectionType) -- Will print "noclip".
    end)
end)
```
