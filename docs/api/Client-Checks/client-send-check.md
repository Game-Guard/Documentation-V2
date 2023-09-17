# Client Send Check

!!! warning
    This can be bypassed by a client sided exploit.

```lua hl_lines="3" linenums="1"
local gameGuard = require(script.Parent.GameGuard)

gameGuard:clientSendCheck()
```