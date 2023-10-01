# Enums
A list of enumerators that can be used to configure Game Guard.

## Ignore Next

```lua linenums="1"
local gameGuard = require(script.Parent.GameGuard)
gameGuard.Enums.IgnoreNext = {
    ["WalkSpeed"] = "speed",
    ["JumpPower"] = "jp",
    ["NoClip"] = "nc"
}
```

## Client Check
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).

```lua linenums="1"
["ClientCheck"] = {
    ["WalkSpeed"] = "ws",
    ["JumpPower"] = "jp",
    ["GraphicalUserInterface"] = "gui",
    ["Argument"] = {
        ["Tick"] = "arg (tick)"
    },
    ["Authentication"] = {
        ["Token"] = "auth (token)",
        ["Data"] = "auth (data)"
    }
}
```
