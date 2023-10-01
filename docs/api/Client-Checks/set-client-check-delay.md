# Set Client Check State
!!! warning
    **⭐Pro Feature:** This function is a pro feature and requires a pro license to use. You can purchase a pro license [here](https://discord.gg/2F4CJFhVwv).

Sets the delay for the client check.

## Parameters:

| Parameter | Description                                                | Type    |
| --------- | ---------------------------------------------------------- | ------- |
| delay     | The delay between checks.                       | Int |

!!! warning
    We do not recommend setting this under 3 seconds as this will cause more false positives for people who have a high ping. We also do not encourage using this function frequently because it may cause issues with the client anti-cheat.

## Example Usage:

```lua hl_lines="4" linenums="1"
local gameGuard = require(script.Parent.GameGuard)

gameGuard:init(plr)
gameGuard:setClientCheckDelay(10) -- Sets the delay to 10 seconds.
```
