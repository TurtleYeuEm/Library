# NexusLib
NexusLib A Free UI Library for Roblox

# Usage Example
local NexusLib = loadstring(game:HttpGet("RAW_URL"))()

local Win = NexusLib:CreateWindow({
    Name = "My Script",
    Subtitle = "v1.0",
    Theme = "Dark", -- "Midnight" | "Light"
})

local Tab = Win:CreateTab("Main")

Tab:CreateToggle({
    Name = "Auto Farm",
    CurrentValue = false,
    Callback = function(val)
        print("Toggle:", val)
    end,
})

Tab:CreateSlider({
    Name = "Speed",
    Range = {0, 100},
    Increment = 5,
    CurrentValue = 16,
    Callback = function(val)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = val
    end,
})

Win:Notify({
    Title = "Loaded!",
    Content = "Script activated successfully.",
    Duration = 4,
})

# Elements
CreateTab(name)
Create a new tab
CreateSection(name)
Partition header
CreateButton({})
Button
CreateToggle({})
Toggle switch
CreateSlider({})
Pull rod
CreateInput({})
Input field
CreateDropdown({})
Dropdown menu
CreateKeybind({})
Assign shortcuts
CreateColorPicker({})
Choose a color
CreateLabel(text)
Document
CreateSeparator()
Line
Window:Notify({})
Screen corner notification
