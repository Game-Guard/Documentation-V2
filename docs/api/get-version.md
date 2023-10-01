# Getting Version
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).
This function will allow you to retrieve Game Guards current version and tag.

## Parameters:

| Parameter | Description | Type |
| --------- | ----------- | ---- |
| None      | None.       | nil  |

## Example Usage:

```lua hl_lines="5-9" linenums="1"
local gameGuard = require(script.Parent.gameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function()
    print(gameGuard:getVersion()) -- Will print table:
        -- {
        --     ["version"] = version, -- The version of Game Guard.
        --     ["tag"] = tag, -- The current tag of Game Guard.
        -- }
end)
```
