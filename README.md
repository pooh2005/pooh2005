
function MonLevel() -- Check Level
    lv = game:GetService("Players").LocalPlayer.PlayerStats.Level.Value
    if lv == 1 or lv <= 14 then
        _G.Quest = "Bandit"
        _G.Ms = "Bandit [Lv:5]"
    elseif lv == 15 or lv <= 30000 then
        _G.Quest = "Pirates"
        _G.Ms = "Pirates [Lv:15]"
    end
end


function AutoFarm() -- Auto Farm
    MonLevel()
    if game:GetService("Players").LocalPlayer.PlayerGui.QuestGui.Enabled == false then
    game:GetService("ReplicatedStorage").FuncQuest:InvokeServer(_G.Quest)
    elseif game:GetService("Players").LocalPlayer.PlayerGui.QuestGui.Enabled == true then
        for i,v in pairs(game:GetService("Workspace").Lives:GetChildren()) do
            if v.Name == _G.Ms and v.Torso.Transparency == 0 then
                repeat wait()
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,2)
                game:GetService('VirtualUser'):CaptureController()
                game:GetService('VirtualUser'):ClickButton1(Vector2.new(851, 158), game:GetService("Workspace").Camera.CFrame)
                until _G.AutoFarm == false or v.Humanoid.Health <= 0
            end
        end
    end
end
 
while _G.AutoFarm do wait() -- Loop Auto farm
    pcall(function()
    AutoFarm()
    print("Plususx HUB Beta")
    end)
end
