# Checking Speed

This function will allow you to check a players speed.

## Parameters:

| Parameter | Description                                                     | Type     |
| --------- | --------------------------------------------------------------- | -------- |
| plr       | The player object of which to check the speed value of.         | Player   |
| WalkSpeed | The amount of walk speed the detection will be run at.          | Int      |
| Result    | The function to call on the result of the check speed function. | function |

## Example Usage:

```lua hl_lines="6-18" linenums="1"
local gameGuard = require(script.Parent.gameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    local WalkSpeed = 16
    gameGuard:checkSpeed(plr, WalkSpeed, function(plrToCheck, state, detectionType, data)
        print(plrToCheck) -- Prints the player who was detected.
        print(state) -- Prints a boolean, true or false based on whether or not the player was detected.
        print(detectionType) -- Will print "speed".
        print(data) -- Returns data table:
        -- {
        --     ["mag"] = mag, -- The magnitude between newPos and prevPos.
        --     ["calc"] = calculatedSpeed, -- The calculated speed.
        --     ["prevPos"] = prevPos -- The previous position.
        --     ["newPos"] = newPos -- The new position at the check.
        -- }
    end)
end)
```

# Update Speed
This function updates the walk speed check for a player.

## Parameters:

| Parameter | Description                                             | Type   |
| --------- | ------------------------------------------------------- | ------ |
| plr       | The player object of which to check the speed value of. | Player |
| WalkSpeed | The amount of walk speed the detection will be run at.  | Int    |

## Example Usage:

```lua hl_lines="7" linenums="1"
local gameGuard = require(script.Parent.gameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    local WalkSpeed = 20
    gameGuard:updateSpeed(plr, WalkSpeed)
end)
```