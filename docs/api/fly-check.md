# Fly Check

This function allows you to check if a specific player is flying.

## Parameters:

| Parameter | Description                                                  | Type     |
| --------- | ------------------------------------------------------------ | -------- |
| plr       | The player of whom you want to check if they are flying.     | Player   |
| time      | The time on how long you can go without touching the ground. | Int      |
| function  | The function to call.                                        | function |

## Example Usage:

```lua hl_lines="4-16" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    gameGuard:flyCheck(plr, 3, function(player, state, detectionType, data)
            print(player) -- Prints the player who was detected.
            print(state) -- Prints a boolean, true or false based on whether or not the player was detected.
            print(detectionType) -- Will print "fly".
            print(data) -- Returns data table:
            -- {
            --     ["prevPos"] = prevPos -- The previous position.
            --     ["lastTouchedFloor"] = lastTouchedFloor -- The last time the player touched the floor.
            -- }
    end)
end)
```
