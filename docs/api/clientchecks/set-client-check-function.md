# Set Client Check Function
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).

```lua hl_lines="3-5" linenums="1"
local gameGuard = require(script.Parent.GameGuard)

gameGuard:setClientCheckFunc(function(plr, detectionType)
    plr:Kick("You were detected for " .. detectionType)
end)
```