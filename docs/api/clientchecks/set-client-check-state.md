# Set Client Check State
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).

Sets the state for the client anti-cheat.

## Parameters:

| Parameter | Description                                                | Type    |
| --------- | ---------------------------------------------------------- | ------- |
| plr       | The player object of which to get the times triggered for. | Player  |
| state     | The state of the client anti-cheat.                        | boolean |

## Example Usage:

```lua hl_lines="6" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    gameGuard:setClientCheckState(plr, false)
end)
```
