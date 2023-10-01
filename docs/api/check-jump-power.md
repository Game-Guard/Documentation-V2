# Checking Jump Power

This function will allow you to check a players jump power.

## Parameters:

| Parameter | Description                                                              | Type     |
| --------- | ------------------------------------------------------------------------ | -------- |
| plr       | The player in which Game Guard should check the jump power for.          | Player   |
| jumpPower | The jump power value which Game Guard should detect.                     | Int      |
| Result    | The function that will be called when Game Guard detects the jump power. | function |

## Example Usage:

!!! warning
    This function is not the most accurate.

```lua hl_lines="7-18" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)

    gameGuard:checkJP(plr, 50, function(plrToCheck, state, detectionType, data)
        print(plrToCheck) -- Prints the player who was detected.
        print(state) -- Prints a boolean, true or false based on whether or not the player was detected.
        print(detectionType) -- Will print "jp".
        print(data) -- Returns data table:
        -- {
        --     ["mag"] = mag, -- The magnitude between newPos and prevPos.
        --     ["calc"] = calculatedJP, -- The calculated jump power.
        --     ["prevPos"] = prevPos -- The previous position.
        --     ["newPos"] = newPos -- The new position at the check.
        -- }
    end)
end)
```

# Update Jump Power

This function updates the jump power check for a player.

## Parameters:

| Parameter | Description                                                     | Type   |
| --------- | --------------------------------------------------------------- | ------ |
| plr       | The player in which Game Guard should check the jump power for. | Player |
| jumpPower | The jump power value which Game Guard should detect.            | Int    |

## Example Usage:

```lua hl_lines="7" linenums="1"
local gameGuard = require(script.Parent.gameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    local JumpPower = 100
    gameGuard:updateJP(plr, JumpPower)
end)
```
