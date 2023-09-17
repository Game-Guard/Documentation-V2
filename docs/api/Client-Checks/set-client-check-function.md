# Set Client Check Function

```lua hl_lines="3-5" linenums="1"
local gameGuard = require(script.Parent.GameGuard)

gameGuard:setClientCheckFunc(function(plr, detectionType)
    plr:Kick("You were detected for " .. detectionType)
end)
```