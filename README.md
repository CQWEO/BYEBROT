local library = loadstring(game:GetObjects("rbxassetid://7657867786")[1].Source)()
local Wait = library.subs.Wait -- Only returns if the GUI has not been terminated. For 'while Wait() do' loops

local PepsisWorld = library:CreateWindow({
Name = "YOU HUB",
Themeable = {
Info = "V3"
}
})

local GeneralTab = Main:CreateTab({
Name = "Main"
})
local Main = Main:CreateSection({
Name = "ESP"
})
Main:AddToggle({
Name = "ESP DOORS",
Flag = "Select Esp"
Local Button = room:WaitForChild("Door"):WaitForChild("Door")
            task.wait()
            local h = esp(door,Color3.fromRGB(255,240,0),door,"[DOOR]")
            table.insert(esptable.doors,h)
            door:WaitForChild("Open").Played:Connect(function()
                h.delete()
            end)
            door.AncestryChanged:Connect(function()
                h.delete()
            end)
        end
        local addconnect
        addconnect = workspace.CurrentRooms.ChildAdded:Connect(function(room)
            setup(room)
        end)
        for i,room in pairs(workspace.CurrentRooms:GetChildren()) do
            if room:FindFirstChild("Assets") then
                setup(room) 
            end
        end
        repeat task.wait() until not flags.espdoors
        addconnect:Disconnect()
        for i,v in pairs(esptable.doors) do
            v.delete()
        end 
    end
end
})
FarmingSection:AddToggle({
Name = "Trick Spammer",
Flag = "FarmingSection_TrickSpammer",
Keybind = 1,
Callback = print
})
