# Removing No Clip Exclusions
This function will allow you to remove a players no clip exclusion parts.

## Parameters:

| Parameter     | Description                                                                      | Type   |
| ------------- | -------------------------------------------------------------------------------- | ------ |
| plr           | The player of which the no clip part will be removed for.                        | Player |
| excludeObject | The part that will be removed from the exclusion list in no clip for the player. | Part   |

## Example Usage:

```lua hl_lines="6" linenums="1"
local gameGuard = require(script.Parent.gameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
    gameGuard:ncRemoveExclusion(player, Workspace:WaitForChild("Exclude")) -- Will remove exclusion for part in workspace called "Exclude".
end)
```
