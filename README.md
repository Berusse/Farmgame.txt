wait(2)
local MenuPanel = game.CoreGui:FindFirstChild("Op_mizu")
local playerCount = #game.Players:GetPlayers()

pcall(function()
    if MenuPanel then
        return  
    end

    if playerCount > 3 then
        pcall(function()
            if MenuPanel then
                MenuPanel:Destroy()
            end
        end)
        wait(0.5)
        pcall(function()
            game:Shutdown()
        end)
        return  
    end

    if playerCount > 1 then
        pcall(function()
            game.ReplicatedStorage.Package.Events.TP:InvokeServer("Earth")
        end)
    end
end)


local success, fail = pcall(function()
    local player = game.Players.LocalPlayer
    local Players = game:GetService("Players")
    local TweenService = game:GetService("TweenService")
    local ReplicatedStorage = game:GetService("ReplicatedStorage")
    local HttpService = game:GetService("HttpService")
    local TeleportService = game:GetService("TeleportService")
    local ScreenGui = Instance.new("ScreenGui")
    local TextLabel = Instance.new("TextLabel")
    local farmLabel = Instance.new("TextLabel")
    local formsLabel = Instance.new("TextLabel")
    local meleeLabel = Instance.new("TextLabel")
    local tpLabel = Instance.new("TextLabel")
    local Reb = Instance.new("TextLabel")
    local destroyLabel = Instance.new("TextLabel")
    local farmButton = Instance.new("TextButton")
    local formsButton = Instance.new("TextButton")
    local playersButton = Instance.new("TextButton")
    local MinimizeButton = Instance.new("TextButton")
    local MainButton = Instance.new("TextButton")
    local billsButton = Instance.new("TextButton")
    local earthButton = Instance.new("TextButton")
    local leftLine = Instance.new("Frame")
    local rightLine = Instance.new("Frame")
    local topLine = Instance.new("Frame")
    local bottomLine = Instance.new("Frame")
    local centerLine = Instance.new("Frame")
    local upperLine = Instance.new("Frame")
    local middleLine = Instance.new("Frame")
    local frontSwitchLine = Instance.new("Frame")
    local MenuPanel = Instance.new("Frame")
    local ButtonCorner = Instance.new("UICorner")
    local Panel = Instance.new("ImageLabel")
    local panelExpanded = false
    local sound = Instance.new("Sound", game.Workspace)
    local imageLabel = Instance.new("ImageLabel")
    local billsImageLabel = Instance.new("ImageLabel")
    local earthImageLabel = Instance.new("ImageLabel")
    local hbtcButton = Instance.new("TextButton")
    local hbtcImageLabel = Instance.new("ImageLabel")
    local hbtgvButton = Instance.new("TextButton")
    local hbtgvImageLabel = Instance.new("ImageLabel")
    local mle_extLabel = Instance.new("TextLabel")
    local Stats = game:GetService("Stats")
    local RunService = game:GetService("RunService")
    local pingTextLabel = Instance.new("TextLabel")
    local fpsTextLabel = Instance.new("TextLabel")
    local missionTextLabel = Instance.new("TextLabel")
    local timeTextLabel = Instance.new("TextLabel")
    local button = Instance.new("TextButton", screenGui)
    local bestId
    local background = Instance.new("Frame")
    local playerListContainer = Instance.new("ScrollingFrame")
    local containerCorner = Instance.new("UICorner") 
    local corner = Instance.new("UICorner")
    local ballFrame = Instance.new("Frame")


local userId = player.UserId
local thumbnailType = Enum.ThumbnailType.HeadShot
local thumbnailSize = Enum.ThumbnailSize.Size48x48
local thumbnailUrl = Players:GetUserThumbnailAsync(userId, thumbnailType, thumbnailSize)

local UICorner = Instance.new("UICorner")

-- ConfiguraciÃ³n de GUI
ScreenGui.Name = "Op_Mizu"
ScreenGui.Parent = player.PlayerGui
ScreenGui.Parent = game.CoreGui
ScreenGui.ResetOnSpawn = false
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling


TextLabel.Parent = ScreenGui
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.5, -350, 0.4, -130)
TextLabel.Size = UDim2.new(0, 410, 0, 30)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Op_Mizu                                                      "
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextStrokeColor3 = Color3.fromRGB(255, 0, 0)
TextLabel.TextStrokeTransparency = 0
TextLabel.Active = true
TextLabel.Draggable = true

MenuPanel.Parent = TextLabel
MenuPanel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
MenuPanel.BorderSizePixel = 0
MenuPanel.Position = UDim2.new(0, 0, 1, 0)
MenuPanel.Size = UDim2.new(0, 410, 0, 400)
MenuPanel.Visible = false

MinimizeButton.Parent = TextLabel
MinimizeButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
MinimizeButton.BorderSizePixel = 0
MinimizeButton.Position = UDim2.new(0.9, 10, 0.5, -14)
MinimizeButton.Size = UDim2.new(0, 30, 0, 26)
MinimizeButton.Font = Enum.Font.SourceSans
MinimizeButton.Text = "Op"
MinimizeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
MinimizeButton.TextSize = 18






bottomLine.Parent = MenuPanel
bottomLine.Size = UDim2.new(1, 0, 0, 3)
bottomLine.Position = UDim2.new(0, 0, 1, -2)
bottomLine.BackgroundColor3 = Color3.fromRGB(0, 0, 255)
bottomLine.BorderSizePixel = 0.6




farmLabel.Parent = MenuPanel
farmLabel.BackgroundTransparency = 1
farmLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
farmLabel.BorderSizePixel = 0
farmLabel.Position = UDim2.new(0.1, -30, 0, 53)
farmLabel.Size = UDim2.new(0, 89, 0, 60)
farmLabel.Font = Enum.Font.SourceSans
farmLabel.Text = "Autofarm"
farmLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
farmLabel.TextScaled = true
farmLabel.TextStrokeColor3 = Color3.fromRGB(255, 255, 255)
farmLabel.TextStrokeTransparency = 0




meleeLabel.Parent = MenuPanel
meleeLabel.BackgroundTransparency = 1
meleeLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
meleeLabel.BorderSizePixel = 0
meleeLabel.Position = UDim2.new(0.01, 5, 0.2,22)
meleeLabel.Size = UDim2.new(0, 89, 0, 60)
meleeLabel.Font = Enum.Font.SourceSans
meleeLabel.Text = "Form"
meleeLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
meleeLabel.TextScaled = true
meleeLabel.TextStrokeColor3 = Color3.fromRGB(255, 255, 255)
meleeLabel.TextStrokeTransparency = 0



Reb.Parent = MenuPanel
Reb.BackgroundTransparency = 1
Reb.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Reb.BorderSizePixel = 0
Reb.Position = UDim2.new(0.01, 5, 0.3,24)
Reb.Size = UDim2.new(0, 89, 0, 60)
Reb.Font = Enum.Font.SourceSans
Reb.Text = "Rebirth"
Reb.TextColor3 = Color3.fromRGB(0, 0, 0)
Reb.TextScaled = true
Reb.TextStrokeColor3 = Color3.fromRGB(255, 255, 255)
Reb.TextStrokeTransparency = 0



mle_extLabel.Parent = MenuPanel
mle_extLabel.BackgroundTransparency = 1
mle_extLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
mle_extLabel.BorderSizePixel = 0
mle_extLabel.Position = UDim2.new(0.4, 69, 0.4, 35)
mle_extLabel.Size = UDim2.new(0, 39, 0, 40)
mle_extLabel.Font = Enum.Font.SourceSans
mle_extLabel.Text = "Meles[]"
mle_extLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
mle_extLabel.TextScaled = true
mle_extLabel.TextStrokeColor3 = Color3.fromRGB(205, 255, 255)
mle_extLabel.TextStrokeTransparency = 0

Panel.Parent = ScreenGui
Panel.BackgroundTransparency = 1
Panel.Position = UDim2.new(0.1, 39, 0, 60)
Panel.Size = UDim2.new(0, 70, 0, 0)
Panel.SizeConstraint = Enum.SizeConstraint.RelativeYY 
Panel.ImageColor3 = Color3.fromRGB(255, 255, 255)
Panel.ScaleType = Enum.ScaleType.Fit 
Panel.SliceCenter = Rect.new(10, 10, 10, 10)

 



missionTextLabel.Name = "MissionTextLabel"
missionTextLabel.Size = UDim2.new(0, 200, 0, 30)
missionTextLabel.Position = UDim2.new(0.5, 60, 0, 0)
missionTextLabel.AnchorPoint = Vector2.new(0.5, 0)
missionTextLabel.BackgroundTransparency = 1
missionTextLabel.Font = Enum.Font.SourceSans
missionTextLabel.TextSize = 15
missionTextLabel.TextColor3 = Color3.fromRGB(128, 128, 128)
missionTextLabel.TextStrokeTransparency = 0
missionTextLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 255)
missionTextLabel.Text = "Dragon Blox Ultimate Private"
missionTextLabel.Parent = TextLabel






ballFrame.Size = UDim2.new(0.01592638372826266, 0, 0.22392638372826266, 0) -- Tamaño de la bola
ballFrame.Position = UDim2.new(0.9796319186413133, 0, 0.7796319186413133, 0) -- Centro de la pantalla
ballFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 0) -- Amarillo brillante
ballFrame.BackgroundTransparency = 0 -- Totalmente opaco
ballFrame.Parent = TextLabel 

corner.CornerRadius = UDim.new(0.9, 0)
corner.Parent = ballFrame





local TweenService = game:GetService("TweenService")
local colorChangeTweenInfo = TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)
local blurEffect = Instance.new("BlurEffect")
blurEffect.Size = 5
blurEffect.Parent = game.Lighting


pcall(function()
    ButtonCorner.Parent = MinimizeButton
    sound.SoundId = "rbxassetid://1293432192"
end)

local menuExpanded = false
local expandTweenInfo = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.Out)
local contractTweenInfo = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In)
local expandSize = UDim2.new(0, 410, 0, 400)
local contractSize = UDim2.new(0, 410, 0, 0)

local expandTween = TweenService:Create(MenuPanel, expandTweenInfo, {Size = expandSize})
local contractTween = TweenService:Create(MenuPanel, contractTweenInfo, {Size = contractSize})

local function SaveMenuState(isExpanded)
    local success, err = pcall(function()
        local stateInfo = {
            IsExpanded = isExpanded,
            LastModified = os.time()
        }
        writefile("MenuState.json", HttpService:JSONEncode(stateInfo))
    end)

    if not success then
        warn("Error al guardar el estado del menú: " .. tostring(err))
    end
end

local function SaveMenuState(isExpanded)
    local success, err = pcall(function()
        local stateInfo = {
            IsExpanded = isExpanded,
            LastModified = os.time()
        }
        writefile("MenuState.json", HttpService:JSONEncode(stateInfo))
    end)

    if not success then
        warn("Error al guardar el estado del menú: " .. tostring(err))
    end
end

local function LoadMenuState()
    local success, result = pcall(function()
        if isfile("MenuState.json") then
            local fileContents = readfile("MenuState.json")
            local stateData = HttpService:JSONDecode(fileContents)
            if stateData and stateData.IsExpanded ~= nil then
                return stateData.IsExpanded
            end
        end
        return false
    end)

    if not success then
        warn("Error al cargar el estado del menú: " .. tostring(result))
        return false
    end

    return result
end

menuExpanded = LoadMenuState()
MenuPanel.Visible = menuExpanded

pcall(function()
    if menuExpanded then
        MenuPanel.Size = expandSize
        MinimizeButton.Text = "Op"
    else
        MenuPanel.Size = contractSize
        MinimizeButton.Text = "+"
    end
end)

MinimizeButton.MouseButton1Click:Connect(function()
    local success, err = pcall(function()
        if menuExpanded then
            contractTween:Play()
            MinimizeButton.Text = "+"
            sound:Play()
            wait(0.6)
            MenuPanel.Visible = false
        else
            MenuPanel.Visible = true
            expandTween:Play()
            MinimizeButton.Text = "Op"
            sound:Play()
        end
        menuExpanded = not menuExpanded
        SaveMenuState(menuExpanded)
    end)

    if not success then
        warn("Error al minimizar/expandir el menú: " .. tostring(err))
    end
end)



local function initSwitches(MenuPanel)
    local function createSwitchModel(parent, position, switchName)
        local switchButton = Instance.new("TextButton")
        switchButton.Parent = parent
        switchButton.BackgroundColor3 = Color3.fromRGB(200, 200, 200)
        switchButton.BorderSizePixel = 0
        switchButton.Position = position
        switchButton.Size = UDim2.new(0, 84, 0, 30)
        switchButton.Text = ""

        local switchButtonCorner = Instance.new("UICorner")
        switchButtonCorner.Parent = switchButton
        switchButtonCorner.CornerRadius = UDim.new(0.4, 0)

        local switchBall = Instance.new("Frame")
        switchBall.Parent = switchButton
        switchBall.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
        switchBall.Size = UDim2.new(0, 30, 0, 30)
        switchBall.Position = UDim2.new(0, 5, 0.5, -15)
        switchBall.BorderSizePixel = 0

        local switchBallCorner = Instance.new("UICorner")
        switchBallCorner.Parent = switchBall
        switchBallCorner.CornerRadius = UDim.new(0.5, 0)

        return switchButton, switchBall
    end

    local function safeCreateSwitch(position, switchName)
    local success, button, ball = pcall(function() return createSwitchModel(MenuPanel, position, switchName) end)
    return success and button, ball or nil, nil
end

local switchButton1, switchBall1 = safeCreateSwitch(UDim2.new(0.1, 75, 0, 69), "Switch1")
local switchButton2, switchBall2 = safeCreateSwitch(UDim2.new(0.6, 75, 0, 69), "Switch2")
local switchButton3, switchBall3 = safeCreateSwitch(UDim2.new(0.285, 0, 0.2, 36), "Switch3")
local switchButton5, switchBall5 = safeCreateSwitch(UDim2.new(0.220, 19, 0.2, 81), "Switch5")
local switchButton6, switchBall6 = safeCreateSwitch(UDim2.new(0.239, 19, 0.2, 125), "Switch6")
local switchButton7, switchBall7 = safeCreateSwitch(UDim2.new(0.4, 49, 0.242, 125), "Switch7")

    local function SaveSwitchState(isActive, switchName)
    pcall(function()
        local SwitchInfo = {
            SwitchOn = isActive,
            LastModified = os.time()
        }
        writefile(switchName.."_SwitchState.json", game:GetService("HttpService"):JSONEncode(SwitchInfo))
    end)
end

local function LoadSwitchState(switchName)
    local success, result = pcall(function()
        if isfile(switchName.."_SwitchState.json") then
            local fileContents = readfile(switchName.."_SwitchState.json")
            if fileContents then
                local switchData = game:GetService("HttpService"):JSONDecode(fileContents)
                if switchData and switchData.SwitchOn ~= nil then
                    return switchData.SwitchOn
                end
            end
        end
        return false
    end)

    if success then
        return result
    else
        return false
    end
end

    local function toggleSwitch(isActive, switchBall)
    pcall(function()
        if isActive then
            switchBall.Position = UDim2.new(1, -35, 0.5, -15)
            switchBall.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
        else
            switchBall.Position = UDim2.new(0, 5, 0.5, -15)
            switchBall.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
        end
    end)
end

    local function safeLoadSwitchState(switchName)
    local success, result = pcall(function() return LoadSwitchState(switchName) end)
    return success and result or false
end

local isLoop1Active = safeLoadSwitchState("Switch1")
local isLoop2Active = safeLoadSwitchState("Switch2")
local isLoop3Active = safeLoadSwitchState("Switch3")
local isLoop5Active = safeLoadSwitchState("Switch5")
local isLoop6Active = safeLoadSwitchState("Switch6")
local isLoop7Active = safeLoadSwitchState("Switch7")

    local function loop1()
        pcall(function()                     
        local player = game.Players.LocalPlayer
local data = game.ReplicatedStorage.Datas[player.UserId]
local events = game:GetService("ReplicatedStorage").Package.Events

local missions = {
    { name = "Klirin", bossName = "Klirin", requiredValue = 0, endRange = 0 },
    { name = "Kid Nohag", bossName = "Kid Nohag", requiredValue = 20000, endRange = 100001 },
    { name = "Radish", bossName = "Radish", requiredValue = 100001, endRange = 200000 },
    { name = "Mapa", bossName = "Mapa", requiredValue = 200001, endRange = 300000 },
    { name = "Citizen", bossName = "Evil Saya", requiredValue = 300001, endRange = 400000 },
    { name = "Top X Fighter", bossName = "X Fighter Master", requiredValue = 400001, endRange = 700000 },
    { name = "Super Vegetable", bossName = "Super Vegetable", requiredValue = 750001, endRange = 1200000 },
    { name = "Perfect Atom", bossName = "Perfect Atom", requiredValue = 3500000, endRange = 5000000 },
    { name = "SSJ2 Wukong", bossName = "SSJ2 Wukong", requiredValue = 5000001, endRange = 8000000 },
    { name = "SSJB Wukong", bossName = "SSJB Wukong", requiredValue = 8000000, endRange = 50000000 },
    { name = "Broccoli", bossName = "Broccoli", requiredValue = 50000001, endRange = 150000000 },
    { name = "SSJG Kakata", bossName = "SSJG Kakata", requiredValue = 150000001, endRange = 200000000 },
    { name = "Vegetable (GoD in-training)", bossName = "Vegetable (GoD in-training)", requiredValue = 200000001, endRange = 300000000 },
    { name = "Wukong (Omen)", bossName = "Wukong (Omen)", requiredValue = 300000001, endRange = 600000000 },
    { name = "Vills (50%)", bossName = "Vills (50%)", requiredValue = 600000001, endRange = 1200000000 },
    { name = "Vis (20%)", bossName = "Vis (20%)", requiredValue = 1200000001, endRange = 1800000000 },
    { name = "Vegetable (LBSSJ4)", bossName = "Vegetable (LBSSJ4)", requiredValue = 1800000001, endRange = 2700000000 },
    { name = "Wukong (LBSSJ4)", bossName = "Wukong (LBSSJ4)", requiredValue = 2700000001, endRange = 4200000000 },
    { name = "Vekuta (LBSSJ4)", bossName = "Vekuta (LBSSJ4)", requiredValue = 4200000001, endRange = 5000000000 },
    { name = "Wukong Rose", bossName = "Wukong Rose", requiredValue = 5000000001, endRange = 5500000000 },
    { name = "Vekuta (SSJBUI)", bossName = "Vekuta (SSJBUI)", requiredValue = 5500000001, endRange = math.huge },
}

local SelectedQuest
local SelectedMob
local firstQuest = true
local lastQuest
local rebirthRemote = events.reb

local function assignQuest()
    local checkValue = math.min(data.Strength.Value, data.Energy.Value, data.Defense.Value, data.Speed.Value)

    if checkValue >= 200000000 and game.placeId ~= 5151400895 and isLoop1Active then
        pcall(function()
            if data.Zeni.Value >= 15000 then
                local A_1 = "Vills Planet"
                local Event = events.TP
                Event:InvokeServer(A_1)
            else
                SelectedQuest = "SSJG Kakata"
                SelectedMob = "SSJG Kakata"
            end
        end)
        return
    end

    if firstQuest == true then
        lastQuest = SelectedQuest
        firstQuest = false
    end

    local lowestStat = math.min(data.Strength.Value, data.Energy.Value, data.Defense.Value, data.Speed.Value)
    for _, mission in ipairs(missions) do
        if lowestStat >= mission.requiredValue and lowestStat <= mission.endRange then
            pcall(function()
                SelectedQuest = mission.name
                SelectedMob = mission.bossName
            end)
            break
        end
    end
end

local function startMission()
    pcall(function()
        local npc = game:GetService("Workspace").Others.NPCs:FindFirstChild(SelectedQuest)
        if npc and npc:FindFirstChild("HumanoidRootPart") and isLoop1Active then
            player.Character.HumanoidRootPart.CFrame = npc.HumanoidRootPart.CFrame
            local args = {npc}
            events.Qaction:InvokeServer(unpack(args))
        end
    end)
end

task.spawn(function()
    while true do
        local lag = game:GetService("RunService").Stepped:Wait()
        local success, errorMessage = pcall(function()
            assignQuest()

            local questValue = game:GetService("ReplicatedStorage").Datas[player.UserId].Quest.Value
            if questValue ~= SelectedQuest then
                startMission()
            end
        end)

        if not success then
            warn("Error en el script: " .. errorMessage)
        end
    end
end)

task.spawn(function()
    while true do
        task.wait(1)
        local success, fallo = pcall(function()
            if data.Strength.Value < 200000000 and game.PlaceId ~= 3311165597 and isLoop1Active then
                local A_1 = "Earth"
                local Event = events.TP
                Event:InvokeServer(A_1)
                task.wait(8)
            end
        end)

        if not success then
            warn("Error al ejecutar la teletransportación: " .. fallo)
        end
    end
end)

task.spawn(function()
    while true do
        task.wait(1)
        if isLoop5Active then
            local success, fallo = pcall(function()
                game:GetService("ReplicatedStorage").Package.Events.reb:InvokeServer()
            end)

            if not success then
                warn("Error al invocar el evento rebirth: " .. fallo)
            end
        end
    end
end)

task.spawn(function()
    while true do
        task.wait(.1)
        if isLoop1Active then
            task.spawn(function()
                local player = game.Players.LocalPlayer
                local data = game.ReplicatedStorage.Datas[player.UserId]
                local mission = data.Quest.Value
                local boss = game.Workspace.Living:FindFirstChild(mission)

                if boss and boss:FindFirstChild("Humanoid") and boss.Humanoid.Health > 0 then
                    task.spawn(function()
                        player.Status.Blocking.Value = true                        
                    end)
                    player.Character.HumanoidRootPart.CFrame = boss.HumanoidRootPart.CFrame
                end
            end)
        end
    end
end)

task.spawn(function()
    while true do
        local ldata = game.ReplicatedStorage:WaitForChild("Datas"):WaitForChild(tostring(game.Players.LocalPlayer.UserId))

        if ldata.Quest.Value ~= "" then
        game.ReplicatedStorage.Package.Events.cha:InvokeServer("Blacknwhite27")
            game:GetService("ReplicatedStorage").Package.Events.p:FireServer("Blacknwhite27", 1)
            game:GetService("ReplicatedStorage").Package.Events.p:FireServer("Blacknwhite27", 2)           
        end

        task.wait(0.2)
    end
end)
            task.wait(0.2)
        end)
    end

   local function loop2()
        while true do
            if isLoop2Active then
    local lplr = game.Players.LocalPlayer
    local ldata = game.ReplicatedStorage:WaitForChild("Datas"):WaitForChild(lplr.UserId)

    local function format_number(number)
        local suffixes = {"", "K", "M", "B", "T", "QD"}
        local suffix_index = 1

        while math.abs(number) >= 1000 and suffix_index < #suffixes do
            number = number / 1000.0
            suffix_index = suffix_index + 1
        end

        return suffix_index > 1 and string.format("%.1f%s", number, suffixes[suffix_index]) or tostring(number)
    end

local function updateStatsGui()
    local success, err = pcall(function()
        local MainFrame = lplr.PlayerGui:WaitForChild("Main"):WaitForChild("MainFrame")
        local StatsFrame = MainFrame:WaitForChild("Frames"):WaitForChild("Stats")
        local ZeniLabel = MainFrame.Indicator:FindFirstChild("Zeni")
        local Bars = MainFrame:WaitForChild("Bars")
        local HPText = Bars.Health:FindFirstChild("TextLabel")
        local EnergyText = Bars.Energy:FindFirstChild("TextLabel")

        local health = lplr.Character and lplr.Character:FindFirstChild("Humanoid") and lplr.Character.Humanoid.Health or 0
        local maxHealth = lplr.Character and lplr.Character:FindFirstChild("Humanoid") and lplr.Character.Humanoid.MaxHealth or 0
        local ki = lplr.Character and lplr.Character:FindFirstChild("Stats") and lplr.Character.Stats.Ki.Value or 0
        local maxKi = lplr.Character and lplr.Character:FindFirstChild("Stats") and lplr.Character.Stats.Ki.MaxValue or 0

        pcall(function()
            HPText.Text = "VIE: " .. format_number(health) .. " / " .. format_number(maxHealth)
        end)
        pcall(function()
            EnergyText.Text = "ENERGIE: " .. format_number(ki) .. " / " .. format_number(maxKi)
        end)
        pcall(function()
            ZeniLabel.Text = format_number(ldata.Zeni.Value) .. " Zeni"
        end)

        for _, stat in pairs({"Strength", "Speed", "Defense", "Energy"}) do
            local statLabel = StatsFrame:FindFirstChild(stat)
            if statLabel then
                pcall(function()
                    statLabel.Text = stat .. ": " .. format_number(ldata[stat].Value)
                end)
            end
        end
    end)

    if not success then
        warn("Error al actualizar GUI de estadísticas:", err)
    end
end

pcall(function()
    updateStatsGui()
end)

game:GetService("RunService").Heartbeat:Connect(function()
    if lplr.Character and lplr.Character:FindFirstChild("Humanoid") and isLoop2Active then
        pcall(function()
            updateStatsGui()
        end)
    end
end)
            end
            task.wait(.5)
        end
    end

 local function loop3()
        pcall(function()                   
       task.spawn(function()
    while true do
        task.wait(.05)

        local succes, fallo = pcall(function()
            local Forms = {'Divine Rose Prominence','Astral Instinct','Ultra Ego','SSJB4','True God of Creation','True God of Destruction','Super Broly', 
                           'LSSJG','LSSJ4','SSJG4','LSSJ3','Mystic Kaioken','LSSJ Kaioken','SSJR3','SSJB3','God Of Destruction','God Of Creation',
                           'Jiren Ultra Instinct', 'Mastered Ultra Instinct','Godly SSJ2', 'Ultra Instinct Omen', 'Evil SSJ','Blue Evolution',
                           'Dark Rose','Kefla SSJ2','SSJ Berserker','True Rose', 'SSJB Kaioken','SSJ Rose', 'SSJ Blue','Corrupt SSJ',
                           'SSJ Rage','SSJG','SSJ4','Mystic','LSSJ','SSJ3','Spirit SSJ','SSJ2 Majin','SSJ2','SSJ Kaioken','SSJ','FSSJ','Kaioken'}

            local equipRemote = game:GetService("ReplicatedStorage").Package.Events.equipskill
            local player = game:GetService("Players").LocalPlayer

            local function transform()
                task.spawn(function()
                    for i, v in pairs(Forms) do
                        if equipRemote:InvokeServer(v) then
                            break
                        end
                    end

                    repeat
                        task.wait()
                        local success1 = pcall(function()
                            if player.Status.SelectedTransformation.Value ~= player.Status.Transformation.Value then
                                game:GetService("ReplicatedStorage").Package.Events.ta:InvokeServer()
                            end
                        end)

                        if not success1 then
                            local success2 = pcall(function()
                                if game.Workspace.Living[player.Name].Status.SelectedTransformation.Value ~= game.Workspace.Living[player.Name].Status.Transformation.Value then
                                    game:GetService("ReplicatedStorage").Package.Events.ta:InvokeServer()
                                end
                            end)

                            if not success2 then
                                warn("Ambos métodos fallaron al verificar las transformaciones.")
                            end
                        end
                    until game.Workspace.Living[player.Name].Status.SelectedTransformation.Value ==
                        game.Workspace.Living[player.Name].Status.Transformation.Value
                end)
            end

            local stats = player.Character:WaitForChild("Stats")
            if stats.Strength.Value > 5000 and stats.Defense.Value > 5000 and stats.Energy.Value > 5000 and stats.Speed.Value > 5000 then
                transform()
            end
        end)

        if not succes then
            warn(fallo)
        end
    end
end)


        task.wait(.1)
        end)
    end

    local function loop5()
        while true do
            pcall(function()
                if isLoop3Active then
local Players = game:GetService("Players")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Workspace = game:GetService("Workspace")

local lplr = Players.LocalPlayer

pcall(function()
    if lplr.PlayerGui:FindFirstChild("Start") then
        ReplicatedStorage.Package.Events.Start:InvokeServer()

        if Workspace.Others:FindFirstChild("Title") then
            Workspace.Others.Title:Destroy()
        end

        local cam = Workspace.CurrentCamera
        cam.CameraType = Enum.CameraType.Custom
        cam.CameraSubject = lplr.Character.Humanoid

        _G.Ready = true
        game.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.All, true)

        lplr.PlayerGui.Main.Enabled = true

        if lplr.PlayerGui:FindFirstChild("Start") then
            lplr.PlayerGui.Start:Destroy()
        end

        pcall(function()
            lplr.PlayerGui.Main.bruh.Enabled = false
        end)
        pcall(function()
            lplr.PlayerGui.Main.bruh.Enabled = true
        end)
    end
end)
                    local s = game.Players.LocalPlayer.PlayerGui.Main.MainFrame.Frames.Quest
s.Visible = false
s.Position = UDim2.new(0.01, 0, 0.4, 0)

spawn(function()
    while true do
        local success, err = pcall(function()
            s.Position = UDim2.new(2, 0, 0, 0)
            task.wait(0.4)
        end)

        if not success then
            warn("Error en loop5: " .. err)
        end
        task.wait()
    end
end)
                end
            end)
            task.wait(1)
        end
    end

    local function loop6()
        pcall(function()
firstquest = true
autostack = false

local Settings = {Tables = {Forms = {}}; Variables = {Farm = false}}
setmetatable(Settings, {__index = function() warn('Dumbass') end})

local equipRemote = game:GetService("ReplicatedStorage").Package.Events.equipskill
local player = game.Players.LocalPlayer
local data = game.ReplicatedStorage.Datas[player.UserId]
local events = game:GetService("ReplicatedStorage").Package.Events
local rs = game:GetService("RunService")

local quests = {
    { name = "X Fighter Trainer", nickname = "X Fighter", requiredValue = 0, endRange = 25000 },
    { name = "Oozaru", nickname = "Oozaru", requiredValue = 25000, endRange = math.huge },
}

function target()
    local success, fallo = pcall(function()
        targetted = game:GetService("Players").LocalPlayer.Name
    end)

    if not success then
        warn("Error en target: " .. fallo)
    end
end

target()

local function autoquest()
    local success, fallo = pcall(function()
        repeat
            task.wait(0.1)  -- Pequeño retraso para evitar la sobrecarga
        until game.workspace.Living[targetted]

        local a, b, c, d = data.Strength.Value, data.Energy.Value, data.Defense.Value, data.Speed.Value
        local smallest = math.min(a, b, c, d)

        for _, quest in ipairs(quests) do
            if smallest >= quest.requiredValue and smallest <= quest.endRange then
                SelectedQuests = quest.name
                SelectedMobs = quest.nickname
                break
            end
        end

        if firstquest then
            lastquest = SelectedQuests
            firstquest = false
        end

        if autostack and smallest > 8000 then
            if lastquest ~= SelectedQuests and isLoop6Active then
                game.workspace.Living[targetted].UpperTorso:Destroy()
                getgenv().stacked = false
                repeat
                    task.wait(0.5)  -- Pausa entre cada ciclo
                until player.Character.Humanoid.Health > 0
            end
            lastquest = SelectedQuests
        end
    end)

    if not success then
        warn("Error en autoquest: " .. fallo)
    end
end


getgenv().stacked = false

local function quest()
    local success, fallo = pcall(function()
        local npc = game:GetService("Workspace").Others.NPCs:FindFirstChild(SelectedQuests)

        if game:GetService("ReplicatedStorage").Datas[player.UserId].Quest.Value ~= SelectedQuests and isLoop6Active then
            if npc and npc:FindFirstChild("HumanoidRootPart") then
                player.Character.HumanoidRootPart.CFrame = npc.HumanoidRootPart.CFrame
                local args = {npc} -- Se pasa el NPC encontrado como argumento
                game:GetService("ReplicatedStorage").Package.Events.Qaction:InvokeServer(unpack(args))
            end
        end
    end)

    if not success then
        warn("Error en quest: " .. fallo)
    end
end

task.spawn(autoquest)
task.spawn(quest)

local function tpToBoss(boss)
    local success, fallo = pcall(function()
        if player.Character:FindFirstChild("HumanoidRootPart") and boss:FindFirstChild("HumanoidRootPart") then
            player.Character.HumanoidRootPart.CFrame = boss.HumanoidRootPart.CFrame * CFrame.new(0, 0, 4)
        end
    end)

    if not success then
        warn("Error en tpToBoss: " .. fallo)
    end
end

task.spawn(function()
    while true do
        task.wait()
        pcall(function()
            while true do
                task.wait()
                if game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
                    for i, v in ipairs(game:GetService("Workspace").Living:GetChildren()) do
                        autoquest()
                        if v.Name:lower() == SelectedMobs:lower() and player.Character and player.Character:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and isLoop6Active then
                            quest()
                            getgenv().farm = true
                            repeat
                                task.wait()
                                player.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 0, 4)
                            until getgenv().farm == false or v == nil or v.Humanoid.Health <= 0 or player.Character.Humanoid.Health <= 0
                            if player.Character.Humanoid.Health <= 0 then
                                getgenv().farm = false
                                getgenv().stacked = false
                                repeat
                                    task.wait()
                                until player.Character.Humanoid.Health >= 0
                                task.wait()
                            end
                        end
                    end
                end
            end
        end)
    end
end)


task.spawn(function()
    while true do
        task.wait(0.4)
        local succes,fallo = pcall(function()
            if data.Strength.Value >= 25000 and game:GetService("ReplicatedStorage").Datas[player.UserId].Quest.Value == "" and isLoop6Active then
                local kidNohag = game:GetService("Workspace").Others.NPCs["Kid Nohag"]
                if kidNohag and kidNohag:FindFirstChild("HumanoidRootPart") and isLoop6Active then
                    player.Character.HumanoidRootPart.CFrame = kidNohag.HumanoidRootPart.CFrame
                    local args = { kidNohag }
                    game:GetService("ReplicatedStorage").Package.Events.Qaction:InvokeServer(unpack(args)) -- Inicia la misión
                end
            end
        end)
        if not succes then
            warn(fallo)
        end
    end
end)

task.spawn(function()
    while true do
        task.wait(0.3)
        local succes, fallo = pcall(function()
            if isLoop6Active then
                local currentGameHour = math.floor(game.Lighting.ClockTime)
                local playerCount = #game.Players:GetPlayers()
                if currentGameHour >= 6 and currentGameHour < 12 then
                    game.ReplicatedStorage.Package.Events.TP:InvokeServer("Earth")
                elseif playerCount > 1 then
                    game.ReplicatedStorage.Package.Events.TP:InvokeServer("Earth")
                end                
            end
        end)
        if not succes then
            warn(fallo)
        end
    end
end)

task.spawn(function()
    while true do
        if isLoop6Active then
            task.wait(0.1)


            local yo = game.Players.LocalPlayer
            local mission = ReplicatedStorage.Datas[yo.UserId].Quest


            if not mission or mission.Value == "" then
                task.wait(.05)  
                continue
            end

            local currentGameHour = math.floor(game.Lighting.ClockTime)

            if currentGameHour >= 20 or currentGameHour < 6 then
                continue  
            end

            local success, fallo = pcall(function()
                local maxDist = 50
                local bossName = "Halloween Boss"

                yo.Character:SetPrimaryPartCFrame(CFrame.new(-35233.1953125, 18.168001174926758, -28942.220703125))

                local boss = nil
                for _, v in ipairs(game.Workspace.Living:GetChildren()) do
                    if v:IsA("Model") and v.Name == bossName and v:FindFirstChild("HumanoidRootPart") then
                        if (yo.Character.HumanoidRootPart.Position - v.HumanoidRootPart.Position).Magnitude <= maxDist then
                            boss = v
                            break
                        end
                    end
                end

                yo.Character:SetPrimaryPartCFrame(boss and CFrame.new(boss.HumanoidRootPart.Position) or CFrame.new(-35233.1953125, 18.168001174926758, -28942.220703125))
            end)

            if not success then
                warn("Error al invocar el evento rebirth: " .. fallo)
            end
        end
        task.wait(0.1)
    end
end)

task.spawn(function()
    local tpCount = 0

    while true do
        local currentGameHour = math.floor(game.Lighting.ClockTime)

        if currentGameHour == 20 and tpCount < 2 then
            if tpCount == 0 then
                local success, errorMsg = pcall(function()
                    game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-41388.765625, 92.34290313720703, -29013.48046875))
                end)
                if success then
                    tpCount = tpCount + 1
                    task.wait(5)
                    if tpCount == 1 then
                        local success2, errorMsg2 = pcall(function()
                            game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-41388.765625, 92.34290313720703, -29013.48046875))
                        end)
                        if not success2 then
                            warn("Error al realizar el segundo teletransporte: " .. errorMsg2)
                        else
                            tpCount = tpCount + 1
                        end
                    end
                else
                    warn("Error al realizar el primer teletransporte: " .. errorMsg)
                end
            end
        end

        task.wait(0.1)
    end
end)

            task.wait(.1)
    end)
end

local function loop7()
pcall(function()
    task.spawn(function()
    -- Espera 12 segundos antes de comenzar
    task.wait(12)

    while true do
        task.wait(0.1)

        if isLoop7Active then  -- Verifica si el bucle está activo

            task.spawn(function()
                for _, player in ipairs(game.Players:GetPlayers()) do
                    local ldata = game.ReplicatedStorage.Datas[player.UserId]
                    local lplr = game.Players.LocalPlayer
                    local Ki = lplr.Character:WaitForChild("Stats"):WaitForChild("Ki")
                    local humanoid = lplr.Character:WaitForChild("Humanoid")


                    task.spawn(function()
                        if ldata.Quest.Value ~= "" and ldata.Strength.Value > 40000 and ldata.Energy.Value > 40000 and ldata.Defense.Value > 40000 and ldata.Speed.Value > 40000 then
                            local closestBoss, closestDistance = nil, math.huge
                            local playerPos = player.Character and player.Character:FindFirstChild("HumanoidRootPart") and player.Character.HumanoidRootPart.Position or nil

                            if playerPos then
                                task.spawn(function()
                                    for _, v in ipairs(game.Workspace.Living:GetChildren()) do
                                        if v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                            local distance = (playerPos - v.HumanoidRootPart.Position).magnitude
                                            if distance < closestDistance and v.Humanoid.Health > 0 and v.Name ~= player.Character.Name then
                                                closestDistance, closestBoss = distance, v
                                            end
                                        end
                                    end
                                end)

                                task.spawn(function()
                                    if closestBoss and closestDistance <= 12 and closestBoss.Humanoid.Health > 0 then
                                        local attacks = {
                                            
                                                "Super Dragon Fist", "God Slicer", "Spirit Barrage", "Mach Kick",
                                                "Wolf Fang Fist", "High Power Rush", "Meteor Strike", "Meteor Charge", 
                                          
                                            function() 
                                                game.ReplicatedStorage.Package.Events.voleys:InvokeServer("Energy Volley", {FaceMouse = false, MouseHit = CFrame.new()}, "Blacknwhite27")
                                            end
                                        }

                                        for _, attackName in ipairs(attacks) do
                                            task.spawn(function() 
                                                if type(attackName) == "string" then
                                                    game.ReplicatedStorage.Package.Events.mel:InvokeServer(attackName, "Blacknwhite27")
                                                elseif type(attackName) == "function" then
                                                    attackName()
                                                end
                                            end)
                                        end
                                    end
                                end)
                            else
                                warn("Error: No se pudo encontrar la posición del jugador.")
                            end
                        end
                    end)
                end
            end)

            task.wait(0.05)
        end
    end
end)
        task.wait(.2) -- Aumentar la espera entre iteraciones principales para reducir la frecuencia de ejecuciÃ³n
    end)
end


    switchButton1.MouseButton1Click:Connect(function()
        pcall(function()
            isLoop1Active = not isLoop1Active
            toggleSwitch(isLoop1Active, switchBall1)
            SaveSwitchState(isLoop1Active, "Switch1")
        end)
    end)

    switchButton2.MouseButton1Click:Connect(function()
        pcall(function()
            isLoop2Active = not isLoop2Active
            toggleSwitch(isLoop2Active, switchBall2)
            SaveSwitchState(isLoop2Active, "Switch2")
        end)
    end)

    switchButton3.MouseButton1Click:Connect(function()
    pcall(function()
    isLoop3Active = not isLoop3Active
    toggleSwitch(isLoop3Active, switchBall3)
    SaveSwitchState(isLoop3Active, "Switch3")
    end)
end)

    switchButton5.MouseButton1Click:Connect(function()
        pcall(function()
            isLoop5Active = not isLoop5Active
            toggleSwitch(isLoop5Active, switchBall5)
            SaveSwitchState(isLoop5Active, "Switch5")
        end)
    end)

    switchButton6.MouseButton1Click:Connect(function()
        pcall(function()
            isLoop6Active = not isLoop6Active
            toggleSwitch(isLoop6Active, switchBall6)
            SaveSwitchState(isLoop6Active, "Switch6")
        end)
    end)

    switchButton7.MouseButton1Click:Connect(function()
        pcall(function()
            isLoop7Active = not isLoop7Active
            toggleSwitch(isLoop7Active, switchBall7)
            SaveSwitchState(isLoop7Active, "Switch7")
        end)
    end)

    toggleSwitch(isLoop1Active, switchBall1)
    toggleSwitch(isLoop2Active, switchBall2)
    toggleSwitch(isLoop3Active, switchBall3)
    toggleSwitch(isLoop5Active, switchBall5)
    toggleSwitch(isLoop6Active, switchBall6)
    toggleSwitch(isLoop7Active, switchBall7)

    coroutine.wrap(loop1)()
    coroutine.wrap(loop2)()
    coroutine.wrap(loop3)()
    coroutine.wrap(loop5)()
    coroutine.wrap(loop6)()
    coroutine.wrap(loop7)()
end

initSwitches(MenuPanel)

MainButton.MouseButton1Click:Connect(function()
    pcall(togglePanel)
end)

earthButton.MouseButton1Click:Connect(function()
    pcall(function()
        local playerCount = #game.Players:GetPlayers()
        print("Número de jugadores: " .. playerCount)  -- Para depuración
        if playerCount > 3 then
            game:GetService("TeleportService"):Teleport(3311165597, game.Players.LocalPlayer)
        elseif playerCount < 3 then
            game.ReplicatedStorage.Package.Events.TP:InvokeServer("Earth")
        end
    end)
end)

billsButton.MouseButton1Click:Connect(function()
    pcall(function()
        local playerCount = #game.Players:GetPlayers()
        print("Número de jugadores: " .. playerCount)  -- Para depuración
        if playerCount > 3 then
            game:GetService("TeleportService"):Teleport(5151400895, game.Players.LocalPlayer)
        elseif playerCount < 3 then
            game.ReplicatedStorage.Package.Events.TP:InvokeServer("Vills Planet")
        end
    end)
end)

hbtcButton.MouseButton1Click:Connect(function()
    pcall(function() game.ReplicatedStorage.Package.Events.TP:InvokeServer("Hyperbolic Time Chamber") end)
end)

hbtgvButton.MouseButton1Click:Connect(function()
    pcall(function() game.ReplicatedStorage.Package.Events.TP:InvokeServer("Gravity Room") end)
end)

farmButton.MouseButton1Click:Connect(function()
    pcall(onFarmButtonClick)
end)

formsButton.MouseButton1Click:Connect(function()
    pcall(onFormsButtonClick)
end)

local function Cal()
    local function updateFPS()
        local count, lastUpdate = 0, tick()

        RunService.RenderStepped:Connect(function()
            count = count + 1
            if tick() - lastUpdate >= 1 then
                pcall(function() 
                    fpsTextLabel.Text = "FPS: " .. count
                end)
                count, lastUpdate = 0, tick()
            end
        end)
    end

    local function Serverping()
        local success, servers = pcall(function()
            return HttpService:JSONDecode(game:HttpGet("https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100")).data
        end)
        if not success then return "Error" end

        local bestPing = math.huge
        for _, server in ipairs(servers) do
            local ping = math.min((function() 
                local start = tick() 
                RunService.Stepped:wait() 
                return (tick() - start) * 1000 
            end)(), 1500)
            if ping < bestPing then 
                bestPing, bestId = ping, server.id 
            end
        end
        return bestPing < math.huge and math.floor(bestPing) .. "/Srv.." or "N/A"
    end

    button.MouseButton1Click:Connect(function()
        pcall(function() 
            if bestId and #game.Players:GetPlayers() > 2 then
                TeleportService:TeleportToPlaceInstance(game.PlaceId, bestId) 
            end
        end)
    end)

    local function updateBallColor()
    local currentHour = math.floor(game.Lighting.ClockTime)
    local currentMinute = math.floor((game.Lighting.ClockTime % 1) * 60)

    pcall(function()
        if currentHour == 15 and currentMinute >= 40 then
            ballFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Morado brillante
        elseif currentHour == 15 and currentMinute >= 0 and currentMinute < 40 then
            if (tick() % 1) < 0.5 then
                ballFrame.BackgroundColor3 = Color3.fromRGB(255, 0, 255) -- Amarillo brillante
            else
                ballFrame.BackgroundColor3 = Color3.fromRGB(255, 0, 255) -- Morado brillante
            end
        else
            ballFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Amarillo brillante
        end

        task.spawn(function()
            local bb = game:service 'VirtualUser'
            game:service 'Players'.LocalPlayer.Idled:connect(function()
                bb:CaptureController()
                bb:ClickButton2(Vector2.new())
            end)
        end)
    end)
end


end

pcall(Cal)
pcall(showPlayerThumbnail)

 end)

if not success then
    warn("Error en la inicialización: " .. tostring(fail))
end 
