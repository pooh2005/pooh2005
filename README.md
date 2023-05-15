--[[
Power X HUB YT : https://www.youtube.com/channel/UCzDucd52nWX3GjmCFKORUOw
Power X HUB YT : https://www.youtube.com/channel/UCzDucd52nWX3GjmCFKORUOw
Power X HUB YT : https://www.youtube.com/channel/UCzDucd52nWX3GjmCFKORUOw
Power X HUB YT : https://www.youtube.com/channel/UCzDucd52nWX3GjmCFKORUOw
--]]

_G.Color = Color3.fromRGB(196, 0, 255)
_G.Color2 = Color3.fromRGB(255, 0, 222)
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
local CenterHubNo1 = library:CreateWindow("Plususx Hub | Blox Fruit V.Beta",Enum.KeyCode.RightControl)
local Tab = CenterHubNo1:CreateTab("AutoFarm")
local Sector1 = Tab:CreateSector("Main","left")
Sector1:AddLabel("Auto Farm Level")
Sector1:AddToggle("AutoFarm-Level",false,function(t)
   print(t)
end)

Sector1:AddButton("Auto kaitun",function()
    print("CENTERHUB")
end)
Sector1:AddDropdown("Multi DropdownText by Centerhub",{"None","IDK","odl2"},"None",true,function(t)
    print(t)
end)
Sector1:AddDropdown("DropdownText by Centerhub",{"None","IDK","odl2"},"None",false,function(t)
    print(t)
end)
local Dropdownxd = Sector1:AddToggle("Toggle With Dropdown",false,function(t)
   print(t)
end)
Dropdownxd:AddDropdown({"None","IDK","odl2"},"None",false,function(t)
    print(t)
end)
local Dropdow2nxd = Sector1:AddToggle("Toggle With Dropdown Multi",false,function(t)
   print(t)
end)
Dropdow2nxd:AddDropdown({"None","IDK","odl2"},"None",true,function(t)
    print(t)
end)
local Sector2 = Tab:CreateSector("SECTOR CENTERHUB 2","Right")
 tablexd = {"xd1","table2","pussy3"}
local dropdoxwn = Sector2:AddDropdown("DropdownText Select Weapon",tablexd,"None",false,function(t)
    print(t)
end)
Sector2:AddToggle("AutoFarm-Quest",false,function(t)
    print(t)
 end)
Sector2:AddButton("Refresh Test",function()
    table.clear(tablexd)
    for i,v in pairs(tablexd) do
    dropdoxwn:Add(v)
    end
end)
local Sector3 = Tab:CreateSector("SECTOR CENTERHUB 3","Right")
Sector3:AddSlider("Slider By Center",20,50,100,1,function(x)
    print(x)
end)
local Sector4 = Tab:CreateSector("SECTOR CENTERHUB 4","left")
Sector4:AddColorpicker('Color picker',Color3.fromRGB(255, 255, 255),function(t)
    print(t)
end)
Sector3:AddSeperator("Seperator By Center")
local Tab2 = CenterHubNo1:CreateTab("Config") -- Config แตกนะเดียวค่อยแก้รอเน็ตมาก่อน By MeowX#0001
local Sector1 = Tab2:CreateSector("ADSASD","left")
Sector1:AddToggle("YAY",nil,function(t)
    _G.YAY = t
end)

spawn(function()
    while wait() do 
        pcall(function()
            if _G.YAY then
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1059.44, 16.3627, 1548.57)
                wait(1)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BanditQuest1",1)
            elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if v.Name == "Bandit [Lv. 5]" and v.Humanoid.Health > 0 then
                        local VirtualUser=game:service'VirtualUser'
                        VirtualUser:CaptureController()
                        VirtualUser:ClickButton1(Vector2.new(0,0))
                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                        v.HumanoidRootPart.Transparency = 0.8
                        v.HumanoidRootPart.CanCollide = false
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,5)
                    end
                end
            end
            end
        end)
    end
end)
