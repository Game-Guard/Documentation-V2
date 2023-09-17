# Initialize Client Script

```lua hl_lines="7" linenums="1"
local gameGuard = require(script.Parent.GameGuard)
local Players = game:GetService("Players")

gameGuard:clientSendCheck()

Players.PlayerAdded:Connect(function(plr)
    gameGuard:initClientScript(plr)
end)
```