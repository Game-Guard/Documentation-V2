# Initialize Client Script
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).

```lua hl_lines="7" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

gameGuard:clientSendCheck()

Players.PlayerAdded:Connect(function(plr)
    gameGuard:initClientScript(plr)
end)
```