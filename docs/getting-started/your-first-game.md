# Your First Game
We know for some people, setting up a new module in your game can be quite confusing and documentation can be hard to understand. That's why we've created this page to help you get started with Game Guard in your game.

## Step 1: Installation
The first step to using Game Guard in your game is to install it. You can find the installation instructions [here](installation.md).

## Step 2: Initializing Game Guard in a script
The next step is to initialize Game Guard on the server, in order to do so, create a new server script in server script service and paste the following code into it:
```lua linenums="1"
local gameGuard = require(game:GetService("ReplicatedStorage").GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)
end)
```

## Step 3: Choosing what checks to use
Game Guard offers many check offered in the API section of this documentation that you can check out, in this guide we will be using some of the basic checks in order to demonstrate what Game Guard can do.
Copy and paste the code below into the script you created in step 2:
```lua linenums="1"
--- ^ Code from above ^ ---
Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)

    gameGuard:checkSpeed(plr, 16, function(plrToCheck, state, detectionType, data)
        if state then
            plrToCheck:Kick("You were detected for exploiting in this experience. Detection: " .. detectionType .. ".")
        end
        print(data)
    end)
end)
```
The above code will check the players speed on the server and if it exceeds the second value we passed in (16), it will kick the player from the game with a detection type of "speed". You can read what the data parameter prints by testing it out in your game, or read the check speed documentation [here](api/check-speed.md).

### The code all together for easy copy-and-paste

```lua linenums="1"
local gameGuard = require(game:GetService("ServerScriptService").GameGuard)
local Players = game:GetService("Players")

Players.PlayerAdded:Connect(function(plr)
    gameGuard:init(plr)

    gameGuard:checkSpeed(plr, 16, function(plrToCheck, state, detectionType, data)
        if state then
            plrToCheck:Kick("You were detected for exploiting in this experience. Detection: " .. detectionType .. ".")
        end
        print(data)
    end)
end)
```
