local Pedo = {
    1135910299,520944,43247021,2350183594,1338963426,1276541545,587649463,245586741,679804290,174941504,174941504}

for _, v in pairs(game:GetService("Players"):GetPlayers()) do
    for _, v1 in pairs(Pedo) do
        if v.UserId == v1 then
            game:GetService("Players").LocalPlayer:Kick("Admin is in the server")
        end
    end
end

game:GetService("Players").PlayerAdded:Connect(function(r)
    for _, v in pairs(Pedo) do
        if r.UserId == v then
            game:GetService("Players").LocalPlayer:Kick("Admin has joined the server")
        end
    end
end)  
local listed = {
2529508762, -- ChauBaolam29
1347848913, -- cucsilau345
1544046636, -- nghiahahi
1855776836, -- hungfc573
1165679906, -- duy08duy08
4850255262, -- 160kdaycnb109
3381622523, -- 160kdaycnb1
1254144943, -- khanhkaido9999
1312230152, -- gigadian123
4723792084, -- clmm98b
1480130154, -- tokuda_jabanvn
1129631079, -- apexbes2
4736342091, -- nzxz5
4736344396, -- nzxz6
4736346104, -- nzxz7
1490665232, -- DFGHTRU10
3246732830, -- Hainclone2
146022306, -- hainha0123456
1810614004, -- Shadow_MainNoob
1957434850, -- clonepk5
4027558815, -- accquaydffirstsea1
1423316156, -- ACE_xXAZPROGOD123Xx
4048427595, --accquaydffirstsea21
1322815101, -- azpro2k7
2221229319, -- duongthai366
1175626557, -- zxcandyxzz
1821277569, -- Jack_Sama123
1928941615, -- King_RareBox
226801418, -- hieubom123
660629515, -- LHPGamingVN
170895715, -- ductx2004
1075665647, -- khang20297
1813673746, -- MagnusDiggory1
175021965, -- huyduy909090
3146985482, -- bl4ck1105
4494066040, -- SimulatorDotio
936844900, -- aztrear2
4802073978, -- tuantuantuantuang
1832777631, --EvilNumBer_1
4254731743 --AHD_SIEUVIP
1574447607, -- cacchutuoitom2000
1069596493, -- ChiThanh_12
1221321256, -- bibimbin1
2572841200, -- 4532Demon
1421912436, -- TNAE_SsLiemDemonsS
1782620303, -- NHD_ZxKhangSenPaixZ
1461551082, -- tranvanvu17
1067471780, -- GasFruit1
1480395031, -- nhat8a10
892917079, -- baxuan1242
1426606839, -- hackcc16
3899214734, -- chemhan78121
3896699123, -- chemhan21323
1370768463 -- hackcc11
}
_G.WhiteListed = false
        for _, v1 in pairs(listed) do
            if game.Players.LocalPlayer.UserId == v1 then
_G.WhiteListed = true
            end
        end
if _G.WhiteListed then
  if game.placeId == 8569358381 or game.placeId == 3237168 then
    local vu = game:GetService("VirtualUser")
    game:GetService("Players").LocalPlayer.Idled:connect(function()
       vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
       wait(1)
       vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
    end)
    
    
    local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    getgenv().firstfruit = game.Workspace.UserData["User_"..Final].Data["DevilFruit"].Value
    getgenv().secondfruit = game.Workspace.UserData["User_"..Final].Data["DevilFruit2"].Value
    

    do  
    local safezonedestroyspace =  game:GetService("Workspace"):FindFirstChild("SafeZoneOuterSpacePart")  
    if safezonedestroyspace then 
    safezonedestroyspace:Destroy() 
    end 
    end
    local SafeZoneOuterSpace = Instance.new("Part",game.Workspace)
    SafeZoneOuterSpace.Name = "SafeZoneOuterSpacePart"
    SafeZoneOuterSpace.Size = Vector3.new(200,3,200)
    SafeZoneOuterSpace.Position = Vector3.new((math.random(-100000, 100000)), 10000, (math.random(-100000, 100000)))
    SafeZoneOuterSpace.Anchored = true
    
        if game.CoreGui:FindFirstChild("LagoGui") then
            game.CoreGui:FindFirstChild("LagoGui"):Destroy()
        end
        local Flux = {RainbowColorValue = 0, HueSelectionPosition = 0}
        local PresetColor = Color3.fromRGB(66, 134, 255)
        local UserInputService = game:GetService("UserInputService")
        local TweenService = game:GetService("TweenService")
        local RunService = game:GetService("RunService")
        local LocalPlayer = game:GetService("Players").LocalPlayer
        local Mouse = LocalPlayer:GetMouse()
        local CloseBind = Enum.KeyCode.RightControl
        
        local Lago = Instance.new("ScreenGui")
        Lago.Name = "LagoGui"
        Lago.Parent = game.CoreGui
        Lago.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        
        coroutine.wrap(
            function()
                while wait() do
                    Flux.RainbowColorValue = Flux.RainbowColorValue + 1 / 255
                    Flux.HueSelectionPosition = Flux.HueSelectionPosition + 1
        
                    if Flux.RainbowColorValue >= 1 then
                        Flux.RainbowColorValue = 0
                    end
        
                    if Flux.HueSelectionPosition == 80 then
                        Flux.HueSelectionPosition = 0
                    end
                end
            end
        )()
        
        local function MakeDraggable(topbarobject, object)
            local Dragging = nil
            local DragInput = nil
            local DragStart = nil
            local StartPosition = nil
        
            local function Update(input)
                local Delta = input.Position - DragStart
                local pos =
                    UDim2.new(
                        StartPosition.X.Scale,
                        StartPosition.X.Offset + Delta.X,
                        StartPosition.Y.Scale,
                        StartPosition.Y.Offset + Delta.Y
                    )
                local Tween = TweenService:Create(object, TweenInfo.new(0.2), {Position = pos})
                Tween:Play()
            end
        
            topbarobject.InputBegan:Connect(
                function(input)
                    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
                        Dragging = true
                        DragStart = input.Position
                        StartPosition = object.Position
        
                        input.Changed:Connect(
                            function()
                                if input.UserInputState == Enum.UserInputState.End then
                                    Dragging = false
                                end
                            end
                        )
                    end
                end
            )
        
            topbarobject.InputChanged:Connect(
                function(input)
                    if
                        input.UserInputType == Enum.UserInputType.MouseMovement or
                        input.UserInputType == Enum.UserInputType.Touch
                    then
                        DragInput = input
                    end
                end
            )
        
            UserInputService.InputChanged:Connect(
                function(input)
                    if input == DragInput and Dragging then
                        Update(input)
                    end
                end
            )
        end
        
        
        
        function Flux:Window(text, bottom,mainclr,toclose)
            CloseBind = toclose or Enum.KeyCode.RightControl
            PresetColor = mainclr or Color3.fromRGB(0, 254, 252)
            local fs = false
            local MainFrame = Instance.new("Frame")
            local MainCorner = Instance.new("UICorner")
            local LeftFrame = Instance.new("Frame")
            local LeftCorner = Instance.new("UICorner")
            local GlowTabHolder = Instance.new("ImageLabel")
            local Title = Instance.new("TextLabel")
            local BottomText = Instance.new("TextLabel")
            local TabHold = Instance.new("Frame")
            local TabLayout = Instance.new("UIListLayout")
            local Drag = Instance.new("Frame")
            local ContainerFolder = Instance.new("Folder")
        
            MainFrame.Name = "MainFrame"
            MainFrame.Parent = Lago
            MainFrame.AnchorPoint = Vector2.new(0.5, 0.5)
            MainFrame.BackgroundColor3 = Color3.fromRGB(22, 29, 31)
            MainFrame.ClipsDescendants = true
            MainFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
            MainFrame.Size = UDim2.new(0, 0, 0, 0)
        
            MainCorner.CornerRadius = UDim.new(0, 5)
            MainCorner.Name = "MainCorner"
            MainCorner.Parent = MainFrame
        
            LeftFrame.Name = "LeftFrame"
            LeftFrame.Parent = MainFrame
            LeftFrame.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
            LeftFrame.Size = UDim2.new(0, 190, 0, 484)
        
            LeftCorner.CornerRadius = UDim.new(0, 5)
            LeftCorner.Name = "LeftCorner"
            LeftCorner.Parent = LeftFrame
        
            GlowTabHolder.Name = "GlowTabHolder"
            GlowTabHolder.Parent = LeftFrame
            GlowTabHolder.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            GlowTabHolder.BackgroundTransparency = 1.000
            GlowTabHolder.BorderSizePixel = 0
            GlowTabHolder.Position = UDim2.new(0, -15, 0, -15)
            GlowTabHolder.Size = UDim2.new(1, 30, 1, 30)
            GlowTabHolder.ZIndex = 0
            GlowTabHolder.Image = "rbxassetid://4996891970"
            GlowTabHolder.ImageColor3 = Color3.fromRGB(15, 15, 15)
            GlowTabHolder.ScaleType = Enum.ScaleType.Slice
            GlowTabHolder.SliceCenter = Rect.new(20, 20, 280, 280)
            
            
            Title.Name = "Title"
            Title.Parent = LeftFrame
            Title.BackgroundColor3 = Color3.fromRGB(255, 0, 11)
            Title.BackgroundTransparency = 1.000
            Title.Position = UDim2.new(0.097560972, 0, 0.0475206636, 0)
            Title.Size = UDim2.new(0, 111, 0, 34)
            Title.Font = Enum.Font.GothamBold
            Title.Text = text
            Title.TextColor3 = Color3.fromRGB(0, 166, 50)
            Title.TextSize = 25.000
            Title.TextXAlignment = Enum.TextXAlignment.Left
        
            BottomText.Name = "BottomText"
            BottomText.Parent = LeftFrame
            BottomText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            BottomText.BackgroundTransparency = 1.000
            BottomText.Position = UDim2.new(0.097560972, 0, 0.0889999792, 0)
            BottomText.Size = UDim2.new(0, 113, 0, 28)
            BottomText.Font = Enum.Font.Gotham
            BottomText.Text = bottom
            BottomText.TextColor3 = Color3.fromRGB(255, 255, 255)
            BottomText.TextSize = 14.000
            BottomText.TextTransparency = 0.300
            BottomText.TextXAlignment = Enum.TextXAlignment.Left
        
            TabHold.Name = "TabHold"
            TabHold.Parent = LeftFrame
            TabHold.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TabHold.BackgroundTransparency = 1.000
            TabHold.Position = UDim2.new(0, 0, 0.167355374, 0)
            TabHold.Size = UDim2.new(0, 190, 0, 403)
        
            TabLayout.Name = "TabLayout"
            TabLayout.Parent = TabHold
            TabLayout.SortOrder = Enum.SortOrder.LayoutOrder
            TabLayout.Padding = UDim.new(0, 3)
        
            Drag.Name = "Drag"
            Drag.Parent = MainFrame
            Drag.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Drag.BackgroundTransparency = 1.000
            Drag.Position = UDim2.new(0.290368259, 0, 0, 0)
            Drag.Size = UDim2.new(0, 501, 0, 23)
        
            ContainerFolder.Name = "ContainerFolder"
            ContainerFolder.Parent = MainFrame
        
            MakeDraggable(Drag,MainFrame)
            MakeDraggable(LeftFrame,MainFrame)
            MainFrame:TweenSize(UDim2.new(0, 706, 0, 484), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
        
            local uitoggled = false
            UserInputService.InputBegan:Connect(
                function(io, p)
                    if io.KeyCode == CloseBind then
                        if uitoggled == false then
                            MainFrame:TweenSize(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            uitoggled = true
                            wait(.5)
                            Lago.Enabled = false
                        else
                            MainFrame:TweenSize(UDim2.new(0, 706, 0, 484), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            Lago.Enabled = true
                            uitoggled = false
                        end
                    end
                end
            )
        
            function Flux:Notification(desc,buttontitle)
                for i, v in next, MainFrame:GetChildren() do
                    if v.Name == "NotificationBase" then
                        v:Destroy()
                    end
                end
                local NotificationBase = Instance.new("TextButton")
                local NotificationBaseCorner = Instance.new("UICorner")
                local NotificationFrame = Instance.new("Frame")
                local NotificationFrameCorner = Instance.new("UICorner")
                local NotificationFrameGlow = Instance.new("ImageLabel")
                local NotificationTitle = Instance.new("TextLabel")
                local CloseBtn = Instance.new("TextButton")
                local CloseBtnCorner = Instance.new("UICorner")
                local NotificationDesc = Instance.new("TextLabel")
        
                NotificationBase.Name = "NotificationBase"
                NotificationBase.Parent = MainFrame
                NotificationBase.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                NotificationBase.BackgroundTransparency = 1
                NotificationBase.Size = UDim2.new(0, 706, 0, 484)
                NotificationBase.AutoButtonColor = false
                NotificationBase.Font = Enum.Font.SourceSans
                NotificationBase.Text = ""
                NotificationBase.TextColor3 = Color3.fromRGB(0, 0, 0)
                NotificationBase.TextSize = 14.000
                NotificationBase.Visible = true
        
                NotificationBaseCorner.CornerRadius = UDim.new(0, 5)
                NotificationBaseCorner.Name = "NotificationBaseCorner"
                NotificationBaseCorner.Parent = NotificationBase
        
                NotificationFrame.Name = "NotificationFrame"
                NotificationFrame.Parent = NotificationBase
                NotificationFrame.AnchorPoint = Vector2.new(0.5, 0.5)
                NotificationFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                NotificationFrame.ClipsDescendants = true
                NotificationFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
                NotificationFrame.Size = UDim2.new(0, 0, 0, 0)
        
                NotificationFrameCorner.CornerRadius = UDim.new(0, 5)
                NotificationFrameCorner.Name = "NotificationFrameCorner"
                NotificationFrameCorner.Parent = NotificationFrame
        
                NotificationFrameGlow.Name = "NotificationFrameGlow"
                NotificationFrameGlow.Parent = NotificationFrame
                NotificationFrameGlow.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                NotificationFrameGlow.BackgroundTransparency = 1.000
                NotificationFrameGlow.BorderSizePixel = 0
                NotificationFrameGlow.Position = UDim2.new(0, -15, 0, -15)
                NotificationFrameGlow.Size = UDim2.new(1, 30, 1, 30)
                NotificationFrameGlow.ZIndex = 0
                NotificationFrameGlow.Image = "rbxassetid://4996891970"
                NotificationFrameGlow.ImageColor3 = Color3.fromRGB(15, 15, 15)
                NotificationFrameGlow.ScaleType = Enum.ScaleType.Slice
                NotificationFrameGlow.SliceCenter = Rect.new(20, 20, 280, 280)
        
                NotificationTitle.Name = "NotificationTitle"
                NotificationTitle.Parent = NotificationFrame
                NotificationTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                NotificationTitle.BackgroundTransparency = 1.000
                NotificationTitle.Position = UDim2.new(0.0400609747, 0, 0.0761325806, 0)
                NotificationTitle.Size = UDim2.new(0, 111, 0, 34)
                NotificationTitle.Font = Enum.Font.GothamBold
                NotificationTitle.Text = Title.Text .. " | NOTIFICATION"
                NotificationTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
                NotificationTitle.TextSize = 24.000
                NotificationTitle.TextXAlignment = Enum.TextXAlignment.Left
                NotificationTitle.TextTransparency = 1
        
                CloseBtn.Name = "CloseBtn"
                CloseBtn.Parent = NotificationFrame
                CloseBtn.BackgroundColor3 = Color3.fromRGB(21, 21, 21)
                CloseBtn.ClipsDescendants = true
                CloseBtn.Position = UDim2.new(0.0403124988, 0, 0.720855951, 0)
                CloseBtn.Size = UDim2.new(0, 366, 0, 43)
                CloseBtn.AutoButtonColor = false
                CloseBtn.Font = Enum.Font.Gotham
                CloseBtn.Text = buttontitle
                CloseBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
                CloseBtn.TextSize = 15.000
                CloseBtn.TextTransparency = 1
                CloseBtn.BackgroundTransparency = 1
        
                CloseBtnCorner.CornerRadius = UDim.new(0, 4)
                CloseBtnCorner.Name = "CloseBtnCorner"
                CloseBtnCorner.Parent = CloseBtn
        
                NotificationDesc.Name = "NotificationDesc"
                NotificationDesc.Parent = NotificationFrame
                NotificationDesc.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                NotificationDesc.BackgroundTransparency = 1.000
                NotificationDesc.Position = UDim2.new(0.112499997, 0, 0.266355127, 0)
                NotificationDesc.Size = UDim2.new(0, 309, 0, 82)
                NotificationDesc.Font = Enum.Font.Gotham
                NotificationDesc.Text = desc
                NotificationDesc.TextColor3 = Color3.fromRGB(255, 255, 255)
                NotificationDesc.TextSize = 15.000
                NotificationDesc.TextWrapped = true
                NotificationDesc.TextTransparency = 1
        
                CloseBtn.MouseEnter:Connect(function()
                    TweenService:Create(
                        CloseBtn,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {TextTransparency = 0}
                    ):Play()
                end)
        
                CloseBtn.MouseLeave:Connect(function()
                    TweenService:Create(
                        CloseBtn,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {TextTransparency = 0.3}
                    ):Play()
                end)
        
                CloseBtn.MouseButton1Click:Connect(function()
        
                    TweenService:Create(
                        NotificationDesc,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {TextTransparency = 1}
                    ):Play()
                    TweenService:Create(
                        CloseBtn,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {TextTransparency = 1}
                    ):Play()
                    TweenService:Create(
                        NotificationTitle,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {TextTransparency = 1}
                    ):Play()
                    TweenService:Create(
                        CloseBtn,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {BackgroundTransparency = 1}
                    ):Play()
        
                    wait(.4)
                    CloseBtn.Visible = false
                    NotificationFrame:TweenSize(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
        
                    wait(.2)
        
                    TweenService:Create(
                        NotificationBase,
                        TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                        {BackgroundTransparency = 1}
                    ):Play()
        
                    wait(.2)
        
                    NotificationBase.Visible = false
                end)
        
        
                TweenService:Create(
                    NotificationBase,
                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                    {BackgroundTransparency = 0.550}
                ):Play()
        
                wait(.1)
        
                NotificationFrame:TweenSize(UDim2.new(0, 400, 0, 214), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
        
                wait(.4)
                TweenService:Create(
                    NotificationDesc,
                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                    {TextTransparency = .3}
                ):Play()
                TweenService:Create(
                    CloseBtn,
                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                    {TextTransparency = .3}
                ):Play()
                TweenService:Create(
                    NotificationTitle,
                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                    {TextTransparency = 0}
                ):Play()
                TweenService:Create(
                    CloseBtn,
                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                    {BackgroundTransparency = 0}
                ):Play()
            end
            local Tabs = {}
            function Tabs:Tab(text,ico)
                local Tab = Instance.new("TextButton")
                local TabIcon = Instance.new("ImageLabel")
                local TabTitle = Instance.new("TextLabel")
        
        
                Tab.Name = "Tab"
                Tab.Parent = TabHold
                Tab.BackgroundColor3 = PresetColor
                Tab.BorderSizePixel = 0
                Tab.Size = UDim2.new(0, 190, 0, 40)
                Tab.AutoButtonColor = false
                Tab.Font = Enum.Font.SourceSans
                Tab.Text = ""
                Tab.TextColor3 = Color3.fromRGB(0, 0, 0)
                Tab.TextSize = 14.000
                Tab.BackgroundTransparency = 1
        
                TabIcon.Name = "TabIcon"
                TabIcon.Parent = Tab
                TabIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                TabIcon.BackgroundTransparency = 1.000
                TabIcon.Position = UDim2.new(0.0634146333, 0, 0.25, 0)
                TabIcon.Size = UDim2.new(0, 20, 0, 20)
                TabIcon.Image = ico
                TabIcon.ImageTransparency = .3
        
                TabTitle.Name = "TabTitle"
                TabTitle.Parent = Tab
                TabTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                TabTitle.BackgroundTransparency = 1.000
                TabTitle.Position = UDim2.new(0.1902439, 0, 0.25, 0)
                TabTitle.Size = UDim2.new(0, 113, 0, 19)
                TabTitle.Font = Enum.Font.Gotham
                TabTitle.Text = text
                TabTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
                TabTitle.TextSize = 15.000
                TabTitle.TextXAlignment = Enum.TextXAlignment.Left
                TabTitle.TextTransparency = .3
        
                local Container = Instance.new("ScrollingFrame")
                local ContainerLayout = Instance.new("UIListLayout")
        
        
                Container.Name = "Container"
                Container.Parent = ContainerFolder
                Container.Active = true
                Container.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                Container.BackgroundTransparency = 1.000
                Container.BorderSizePixel = 0
                Container.Position = UDim2.new(0.321529746, 0, 0.0475206599, 0)
                Container.Size = UDim2.new(0, 470, 0, 438)
                Container.CanvasSize = UDim2.new(0, 0, 0, 0)
                Container.ScrollBarThickness = 5
                Container.Visible = false
                Container.ScrollBarImageColor3 = Color3.fromRGB(71, 76, 84)
        
                ContainerLayout.Name = "ContainerLayout"
                ContainerLayout.Parent = Container
                ContainerLayout.SortOrder = Enum.SortOrder.LayoutOrder
                ContainerLayout.Padding = UDim.new(0, 15)
                if fs == false then
                    fs = true
                    TabTitle.TextTransparency = 0
                    TabIcon.ImageTransparency = 0
                    Tab.BackgroundTransparency = 0
                    Container.Visible = true
                end
        
                Tab.MouseButton1Click:Connect(function()
                    for i, v in next, ContainerFolder:GetChildren() do
                        if v.Name == "Container" then
                            v.Visible = false
                        end
                        Container.Visible = true
                    end
                    for i, v in next, TabHold:GetChildren() do
                        if v.Name == "Tab" then
                            TweenService:Create(
                                v,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                v.TabIcon,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                v.TabTitle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                Tab,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                TabIcon,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                TabTitle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                        end
                    end
                end)
                local ContainerContent = {}
                function ContainerContent:Button(text,callback)
                    local BtnDescToggled = false
                    local Button = Instance.new("TextButton")
                    local ButtonCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
        
                    Button.Name = "Button"
                    Button.Parent = Container
                    Button.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Button.ClipsDescendants = true
                    Button.Position = UDim2.new(0.370312512, 0, 0.552631557, 0)
                    Button.Size = UDim2.new(0, 457, 0, 43)
                    Button.AutoButtonColor = false
                    Button.Font = Enum.Font.SourceSans
                    Button.Text = ""
                    Button.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Button.TextSize = 14.000
        
                    ButtonCorner.CornerRadius = UDim.new(0, 4)
                    ButtonCorner.Name = "ButtonCorner"
                    ButtonCorner.Parent = Button
        
                    Title.Name = "Title"
                    Title.Parent = Button
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(255,255,255)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
        
                    Button.MouseEnter:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0}
                        ):Play()
                    end)
        
                    Button.MouseLeave:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0.3}
                        ):Play()
                    end)
        
                    Button.MouseButton1Click:Connect(function()
                        pcall(callback)
                    end)
        
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
                function ContainerContent:Toggle(text, default, callback)
                    local ToggleDescToggled = false
                    local Toggled = false
                    local Toggle = Instance.new("TextButton")
                    local ToggleCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local ToggleFrame = Instance.new("Frame")
                    local ToggleFrameCorner = Instance.new("UICorner")
                    local ToggleCircle = Instance.new("Frame")
                    local ToggleCircleCorner = Instance.new("UICorner")
        
                    Toggle.Name = "Toggle"
                    Toggle.Parent = Container
                    Toggle.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Toggle.ClipsDescendants = true
                    Toggle.Position = UDim2.new(0.110937506, 0, 0.67653507, 0)
                    Toggle.Size = UDim2.new(0, 457, 0, 43)
                    Toggle.AutoButtonColor = false
                    Toggle.Font = Enum.Font.SourceSans
                    Toggle.Text = ""
                    Toggle.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Toggle.TextSize = 14.000
        
                    ToggleCorner.CornerRadius = UDim.new(0, 4)
                    ToggleCorner.Name = "ToggleCorner"
                    ToggleCorner.Parent = Toggle
        
                    Title.Name = "Title"
                    Title.Parent = Toggle
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(64, 68, 75)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
                    ToggleFrame.Name = "ToggleFrame"
                    ToggleFrame.Parent = Circle
                    ToggleFrame.BackgroundColor3 = Color3.fromRGB(226, 227, 227)
                    ToggleFrame.Position = UDim2.new(33.0856934, 0, 0, 0)
                    ToggleFrame.Size = UDim2.new(0, 27, 0, 11)
        
                    ToggleFrameCorner.Name = "ToggleFrameCorner"
                    ToggleFrameCorner.Parent = ToggleFrame
        
                    ToggleCircle.Name = "ToggleCircle"
                    ToggleCircle.Parent = ToggleFrame
                    ToggleCircle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ToggleCircle.Position = UDim2.new(0, 0, -0.272727281, 0)
                    ToggleCircle.Selectable = true
                    ToggleCircle.Size = UDim2.new(0, 17, 0, 17)
        
                    ToggleCircleCorner.CornerRadius = UDim.new(2, 8)
                    ToggleCircleCorner.Name = "ToggleCircleCorner"
                    ToggleCircleCorner.Parent = ToggleCircle
        
        
                    Toggle.MouseEnter:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0}
                        ):Play()
                    end)
        
                    Toggle.MouseLeave:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0.3}
                        ):Play()
                    end)
        
                    Toggle.MouseButton1Click:Connect(function()
                        if Toggled == false then
                            ToggleCircle:TweenPosition(UDim2.new(0.37, 0,-0.273, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .3, true)
                            TweenService:Create(
                                ToggleCircle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 =PresetColor}
                            ):Play()
                        else
                            ToggleCircle:TweenPosition(UDim2.new(0, 0,-0.273, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .3, true)
                            TweenService:Create(
                                ToggleCircle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                        end
                        Toggled = not Toggled
                        pcall(callback, Toggled)
                    end)
                    if default == true then
                        ToggleCircle:TweenPosition(UDim2.new(0.37, 0,-0.273, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .3, true)
                        TweenService:Create(
                            ToggleCircle,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {BackgroundColor3 =PresetColor}
                        ):Play()
                        Toggled = not Toggled
                        pcall(callback, Toggled)
                    end
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
        
                function ContainerContent:Slider(text,min,max,start,callback)
                    local SliderFunc = {}
                    local SliderDescToggled = false
                    local dragging = false
                    local Slider = Instance.new("TextButton")
                    local SliderCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local SlideFrame = Instance.new("Frame")
                    local CurrentValueFrame = Instance.new("Frame")
                    local SlideCircle = Instance.new("ImageButton")
                    local Value = Instance.new("TextLabel")
        
                    Slider.Name = "Slider"
                    Slider.Parent = Container
                    Slider.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Slider.ClipsDescendants = true
                    Slider.Position = UDim2.new(0.189062506, 0, 0.648612201, 0)
                    Slider.Size = UDim2.new(0, 457, 0, 60)
                    Slider.AutoButtonColor = false
                    Slider.Font = Enum.Font.SourceSans
                    Slider.Text = ""
                    Slider.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Slider.TextSize = 14.000
        
                    SliderCorner.CornerRadius = UDim.new(0, 4)
                    SliderCorner.Name = "SliderCorner"
                    SliderCorner.Parent = Slider
        
                    Title.Name = "Title"
                    Title.Parent = Slider
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(64, 68, 75)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
        
                    SlideFrame.Name = "SlideFrame"
                    SlideFrame.Parent = Title
                    SlideFrame.BackgroundColor3 = Color3.fromRGB(235, 234, 235)
                    SlideFrame.BorderSizePixel = 0
                    SlideFrame.Position = UDim2.new(-0.197140202, 0, 0.986091495, 0)
                    SlideFrame.Size = UDim2.new(0, 426, 0, 3)
        
                    CurrentValueFrame.Name = "CurrentValueFrame"
                    CurrentValueFrame.Parent = SlideFrame
                    CurrentValueFrame.BackgroundColor3 = PresetColor
                    CurrentValueFrame.BorderSizePixel = 0
                    CurrentValueFrame.Size = UDim2.new((start or 0) / max, 0, 0, 3)
        
                    SlideCircle.Name = "SlideCircle"
                    SlideCircle.Parent = SlideFrame
                    SlideCircle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    SlideCircle.BackgroundTransparency = 1.000
                    SlideCircle.Position = UDim2.new((start or 0)/max, -6,-1.30499995, 0)
                    SlideCircle.Size = UDim2.new(0, 11, 0, 11)
                    SlideCircle.Image = "rbxassetid://3570695787"
                    SlideCircle.ImageColor3 = PresetColor
        
                    Value.Name = "Value"
                    Value.Parent = Title
                    Value.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Value.BackgroundTransparency = 1.000
                    Value.Position = UDim2.new(2.27693367, 0, 0, 0)
                    Value.Size = UDim2.new(0, 113, 0, 41)
                    Value.Font = Enum.Font.Gotham
                    Value.Text = tostring(start and math.floor((start / max) * (max - min) + min) or 0)
                    Value.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Value.TextSize = 15.000
                    Value.TextTransparency = 0.300
                    Value.TextXAlignment = Enum.TextXAlignment.Right
        
        
                    local function move(input)
                        local pos =
                            UDim2.new(
                                math.clamp((input.Position.X - SlideFrame.AbsolutePosition.X) / SlideFrame.AbsoluteSize.X, 0, 1),
                                -6,
                                -1.30499995,
                                0
                            )
                        local pos1 =
                            UDim2.new(
                                math.clamp((input.Position.X - SlideFrame.AbsolutePosition.X) / SlideFrame.AbsoluteSize.X, 0, 1),
                                0,
                                0,
                                3
                            )
                        CurrentValueFrame:TweenSize(pos1, "Out", "Sine", 0.1, true)
                        SlideCircle:TweenPosition(pos, "Out", "Sine", 0.1, true)
                        local value = math.floor(((pos.X.Scale * max) / max) * (max - min) + min)
                        Value.Text = tostring(value)
                        pcall(callback, value)
                    end
                    SlideCircle.InputBegan:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                dragging = true
                            end
                        end
                    )
                    SlideCircle.InputEnded:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                dragging = false
                            end
                        end
                    )
                    game:GetService("UserInputService").InputChanged:Connect(
                    function(input)
                        if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
                            move(input)
                        end
                    end
                    )
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                    function SliderFunc:Change(tochange)
                        CurrentValueFrame.Size = UDim2.new((tochange or 0) / max, 0, 0, 3)
                        SlideCircle.Position = UDim2.new((tochange or 0)/max, -6,-1.30499995, 0)
                        Value.Text = tostring(tochange and math.floor((tochange / max) * (max - min) + min) or 0)
                        pcall(callback,tochange)
                    end
                    return SliderFunc
                end
                function ContainerContent:Dropdown(text,list,callback)
                    local DropFunc = {}
                    local Selected = text
                    local FrameSize = 43
                    local ItemCount = 0
                    local DropToggled = false
                    local Dropdown = Instance.new("TextButton")
                    local DropdownCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local ArrowIco = Instance.new("ImageLabel")
                    local DropItemHolder = Instance.new("ScrollingFrame")
                    local DropLayout = Instance.new("UIListLayout")
        
                    Dropdown.Name = "Dropdown"
                    Dropdown.Parent = Container
                    Dropdown.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Dropdown.ClipsDescendants = true
                    Dropdown.Position = UDim2.new(0.110937499, 0, 0.67653507, 0)
                    Dropdown.Size = UDim2.new(0, 457, 0, 43)
                    Dropdown.AutoButtonColor = false
                    Dropdown.Font = Enum.Font.SourceSans
                    Dropdown.Text = ""
                    Dropdown.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Dropdown.TextSize = 14.000
        
                    DropdownCorner.CornerRadius = UDim.new(0, 4)
                    DropdownCorner.Name = "DropdownCorner"
                    DropdownCorner.Parent = Dropdown
        
                    Title.Name = "Title"
                    Title.Parent = Dropdown
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
                    ArrowIco.Name = "ArrowIco"
                    ArrowIco.Parent = Title
                    ArrowIco.AnchorPoint = Vector2.new(0.5, 0.5)
                    ArrowIco.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ArrowIco.BackgroundTransparency = 1.000
                    ArrowIco.Position = UDim2.new(3.45979357, 0, 0.508096159, 0)
                    ArrowIco.Selectable = true
                    ArrowIco.Size = UDim2.new(0, 28, 0, 24)
                    ArrowIco.Image = "http://www.roblox.com/asset/?id=6035047377"
                    ArrowIco.ImageTransparency = .3
        
                    DropItemHolder.Name = "DropItemHolder"
                    DropItemHolder.Parent = Title
                    DropItemHolder.Active = true
                    DropItemHolder.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    DropItemHolder.BackgroundTransparency = 1.000
                    DropItemHolder.BorderSizePixel = 0
                    DropItemHolder.Position = UDim2.new(-0.203539819, 0, 1.02380955, 0)
                    DropItemHolder.Size = UDim2.new(0, 436, 0, 82)
                    DropItemHolder.CanvasSize = UDim2.new(0, 0, 0, 0)
                    DropItemHolder.ScrollBarThickness = 5
                    DropItemHolder.ScrollBarImageColor3 = Color3.fromRGB(31, 41, 43)
        
                    DropLayout.Name = "DropLayout"
                    DropLayout.Parent = DropItemHolder
                    DropLayout.SortOrder = Enum.SortOrder.LayoutOrder
                    DropLayout.Padding = UDim.new(0, 2)
        
                    Dropdown.MouseEnter:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0}
                        ):Play()
                    end)
        
                    Dropdown.MouseLeave:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0.3}
                        ):Play()
                    end)
        
        
                    Dropdown.MouseButton1Click:Connect(function()
                        if DropToggled == false then
                            Title.Text = Selected
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, FrameSize), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 180}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        else
                            Title.Text = Selected
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 0}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end
                        DropToggled = not DropToggled
                    end)
        
                    for i,v in next, list do
                        ItemCount = ItemCount + 1
        
                        if ItemCount == 1 then
                            FrameSize = 78
                        elseif ItemCount == 2 then
                            FrameSize = 107
                        elseif ItemCount >= 3 then
                            FrameSize = 133
                        end
                        local Item = Instance.new("TextButton")
                        local ItemCorner = Instance.new("UICorner")
        
                        Item.Name = "Item"
                        Item.Parent = DropItemHolder
                        Item.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                        Item.ClipsDescendants = true
                        Item.Size = UDim2.new(0, 427, 0, 25)
                        Item.AutoButtonColor = false
                        Item.Font = Enum.Font.Gotham
                        Item.Text = v
                        Item.TextColor3 = Color3.fromRGB(255, 255, 255)
                        Item.TextSize = 15.000
                        Item.TextTransparency = 0.300
        
                        ItemCorner.CornerRadius = UDim.new(0, 4)
                        ItemCorner.Name = "ItemCorner"
                        ItemCorner.Parent = Item
                        DropItemHolder.CanvasSize = UDim2.new(0, 0, 0, DropLayout.AbsoluteContentSize.Y)
        
                        Item.MouseEnter:Connect(function()
                            TweenService:Create(
                                Item,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                        end)
        
                        Item.MouseLeave:Connect(function()
                            TweenService:Create(
                                Item,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                        end)
        
                        Item.MouseButton1Click:Connect(function()
                            pcall(callback, v)
                            Title.Text = text
                            Selected = v
                            DropToggled = not DropToggled
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 0}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
        
                        end)
                    end
                    function DropFunc:Add(addtext)
                        ItemCount = ItemCount + 1
        
                        if ItemCount == 1 then
                            FrameSize = 78
                        elseif ItemCount == 2 then
                            FrameSize = 107
                        elseif ItemCount >= 3 then
                            FrameSize = 133
                        end
                        local Item = Instance.new("TextButton")
                        local ItemCorner = Instance.new("UICorner")
        
                        Item.Name = "Item"
                        Item.Parent = DropItemHolder
                        Item.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                        Item.ClipsDescendants = true
                        Item.Size = UDim2.new(0, 427, 0, 25)
                        Item.AutoButtonColor = false
                        Item.Font = Enum.Font.Gotham
                        Item.Text = addtext
                        Item.TextColor3 = Color3.fromRGB(255, 255, 255)
                        Item.TextSize = 15.000
                        Item.TextTransparency = 0.300
        
                        ItemCorner.CornerRadius = UDim.new(0, 4)
                        ItemCorner.Name = "ItemCorner"
                        ItemCorner.Parent = Item
                        DropItemHolder.CanvasSize = UDim2.new(0, 0, 0, DropLayout.AbsoluteContentSize.Y)
        
                        Item.MouseEnter:Connect(function()
                            TweenService:Create(
                                Item,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                        end)
        
                        Item.MouseLeave:Connect(function()
                            TweenService:Create(
                                Item,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                        end)
        
                        Item.MouseButton1Click:Connect(function()
                            pcall(callback, addtext)
                            Title.Text = text
                            Selected = addtext
                            DropToggled = not DropToggled
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 0}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end)
                        if DropToggled == true then
                            Title.Text = Selected
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 0}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end
                    end
                    function DropFunc:Clear()
                        Title.Text = text
                        FrameSize = 0
                        ItemCount = 0
                        for i, v in next, DropItemHolder:GetChildren() do
                            if v.Name == "Item" then
                                v:Destroy()
                            end
                        end
                        if DropToggled == true then
                            Title.Text = Selected
                            Dropdown:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {ImageTransparency = .3}
                            ):Play()
                            TweenService:Create(
                                ArrowIco,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {Rotation = 0}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end
                    end
                    return DropFunc
                end
                function ContainerContent:Colorpicker(text,preset,callback)
                    local ColorPickerToggled = false
                    local OldToggleColor = Color3.fromRGB(0, 0, 0)
                    local OldColor = Color3.fromRGB(0, 0, 0)
                    local OldColorSelectionPosition = nil
                    local OldHueSelectionPosition = nil
                    local ColorH, ColorS, ColorV = 1, 1, 1
                    local RainbowColorPicker = false
                    local ColorPickerInput = nil
                    local ColorInput = nil
                    local HueInput = nil
        
                    local Colorpicker = Instance.new("Frame")
                    local ColorpickerCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local Hue = Instance.new("ImageLabel")
                    local HueCorner = Instance.new("UICorner")
                    local HueGradient = Instance.new("UIGradient")
                    local HueSelection = Instance.new("ImageLabel")
                    local Color = Instance.new("ImageLabel")
                    local ColorCorner = Instance.new("UICorner")
                    local ColorSelection = Instance.new("ImageLabel")
                    local Toggle = Instance.new("TextLabel")
                    local ToggleFrame = Instance.new("Frame")
                    local ToggleFrameCorner = Instance.new("UICorner")
                    local ToggleCircle = Instance.new("Frame")
                    local ToggleCircleCorner = Instance.new("UICorner")
                    local Confirm = Instance.new("TextButton")
                    local ConfirmCorner = Instance.new("UICorner")
                    local ConfirmTitle = Instance.new("TextLabel")
                    local BoxColor = Instance.new("Frame")
                    local BoxColorCorner = Instance.new("UICorner")
                    local ColorpickerBtn = Instance.new("TextButton")
                    local ToggleBtn = Instance.new("TextButton")
        
        
                    Colorpicker.Name = "Colorpicker"
                    Colorpicker.Parent = Container
                    Colorpicker.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Colorpicker.ClipsDescendants = true
                    Colorpicker.Position = UDim2.new(0.110937499, 0, 0.67653507, 0)
                    Colorpicker.Size = UDim2.new(0, 457, 0, 43)
        
                    ColorpickerCorner.CornerRadius = UDim.new(0, 4)
                    ColorpickerCorner.Name = "ColorpickerCorner"
                    ColorpickerCorner.Parent = Colorpicker
        
                    Title.Name = "Title"
                    Title.Parent = Colorpicker
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = "UI Color Setting"
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
        
                    ColorpickerBtn.Name = "ColorpickerBtn"
                    ColorpickerBtn.Parent = Title
                    ColorpickerBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ColorpickerBtn.BackgroundTransparency = 1.000
                    ColorpickerBtn.Position = UDim2.new(-0.336283177, 0, 0, 0)
                    ColorpickerBtn.Size = UDim2.new(0, 457, 0, 42)
                    ColorpickerBtn.Font = Enum.Font.SourceSans
                    ColorpickerBtn.Text = ""
                    ColorpickerBtn.TextColor3 = Color3.fromRGB(0, 0, 0)
                    ColorpickerBtn.TextSize = 14.000
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(64, 68, 75)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
                    Hue.Name = "Hue"
                    Hue.Parent = Title
                    Hue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Hue.Position = UDim2.new(0, 229, 0, 46)
                    Hue.Size = UDim2.new(0, 25, 0, 80)
        
                    HueCorner.CornerRadius = UDim.new(0, 3)
                    HueCorner.Name = "HueCorner"
                    HueCorner.Parent = Hue
        
                    HueGradient.Color = ColorSequence.new {
                        ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 0, 4)),
                        ColorSequenceKeypoint.new(0.20, Color3.fromRGB(234, 255, 0)),
                        ColorSequenceKeypoint.new(0.40, Color3.fromRGB(21, 255, 0)),
                        ColorSequenceKeypoint.new(0.60, Color3.fromRGB(0, 255, 255)),
                        ColorSequenceKeypoint.new(0.80, Color3.fromRGB(0, 17, 255)),
                        ColorSequenceKeypoint.new(0.90, Color3.fromRGB(255, 0, 251)),
                        ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 0, 4))
                    }			
                    HueGradient.Rotation = 270
                    HueGradient.Name = "HueGradient"
                    HueGradient.Parent = Hue
        
                    HueSelection.Name = "HueSelection"
                    HueSelection.Parent = Hue
                    HueSelection.AnchorPoint = Vector2.new(0.5, 0.5)
                    HueSelection.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    HueSelection.BackgroundTransparency = 1.000
                    HueSelection.Position = UDim2.new(0.48, 0, 1 - select(1, Color3.toHSV(preset)))
                    HueSelection.Size = UDim2.new(0, 18, 0, 18)
                    HueSelection.Image = "http://www.roblox.com/asset/?id=4805639000"
                    HueSelection.Visible = false
        
                    Color.Name = "Color"
                    Color.Parent = Title
                    Color.BackgroundColor3 = Color3.fromRGB(255, 0, 4)
                    Color.Position = UDim2.new(0, -23, 0, 46)
                    Color.Size = UDim2.new(0, 246, 0, 80)
                    Color.ZIndex = 10
                    Color.Image = "rbxassetid://4155801252"
        
                    ColorCorner.CornerRadius = UDim.new(0, 3)
                    ColorCorner.Name = "ColorCorner"
                    ColorCorner.Parent = Color
        
                    ColorSelection.Name = "ColorSelection"
                    ColorSelection.Parent = Color
                    ColorSelection.AnchorPoint = Vector2.new(0.5, 0.5)
                    ColorSelection.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ColorSelection.BackgroundTransparency = 1.000
                    ColorSelection.Position = UDim2.new(preset and select(3, Color3.toHSV(preset)))
                    ColorSelection.Size = UDim2.new(0, 18, 0, 18)
                    ColorSelection.Image = "http://www.roblox.com/asset/?id=4805639000"
                    ColorSelection.ScaleType = Enum.ScaleType.Fit
                    ColorSelection.Visible = false
        
                    Toggle.Name = "Toggle"
                    Toggle.Parent = Title
                    Toggle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Toggle.BackgroundTransparency = 1.000
                    Toggle.Position = UDim2.new(2.37430048, 0, 1.07157099, 0)
                    Toggle.Size = UDim2.new(0, 137, 0, 38)
                    Toggle.Font = Enum.Font.Gotham
                    Toggle.Text = "Rainbow"
                    Toggle.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Toggle.TextSize = 15.000
                    Toggle.TextTransparency = 0.300
                    Toggle.TextXAlignment = Enum.TextXAlignment.Left
        
                    ToggleFrame.Name = "ToggleFrame"
                    ToggleFrame.Parent = Toggle
                    ToggleFrame.BackgroundColor3 = Color3.fromRGB(226, 227, 227)
                    ToggleFrame.Position = UDim2.new(0.778387249, 0, 0.357142866, 0)
                    ToggleFrame.Size = UDim2.new(0, 27, 0, 11)
        
                    ToggleFrameCorner.Name = "ToggleFrameCorner"
                    ToggleFrameCorner.Parent = ToggleFrame
        
                    ToggleCircle.Name = "ToggleCircle"
                    ToggleCircle.Parent = ToggleFrame
                    ToggleCircle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ToggleCircle.Position = UDim2.new(0, 0, -0.273000002, 0)
                    ToggleCircle.Selectable = true
                    ToggleCircle.Size = UDim2.new(0, 17, 0, 17)
        
                    ToggleCircleCorner.CornerRadius = UDim.new(2, 8)
                    ToggleCircleCorner.Name = "ToggleCircleCorner"
                    ToggleCircleCorner.Parent = ToggleCircle
        
                    Confirm.Name = "Confirm"
                    Confirm.Parent = Title
                    Confirm.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Confirm.ClipsDescendants = true
                    Confirm.Position = UDim2.new(2.3791616, 0, 1.97633278, 0)
                    Confirm.Size = UDim2.new(0, 144, 0, 42)
                    Confirm.AutoButtonColor = false
                    Confirm.Font = Enum.Font.SourceSans
                    Confirm.Text = ""
                    Confirm.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Confirm.TextSize = 14.000
        
                    ConfirmCorner.CornerRadius = UDim.new(0, 4)
                    ConfirmCorner.Name = "ConfirmCorner"
                    ConfirmCorner.Parent = Confirm
        
                    ConfirmTitle.Name = "ConfirmTitle"
                    ConfirmTitle.Parent = Confirm
                    ConfirmTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ConfirmTitle.BackgroundTransparency = 1.000
                    ConfirmTitle.Size = UDim2.new(0, 116, 0, 40)
                    ConfirmTitle.Font = Enum.Font.Gotham
                    ConfirmTitle.Text = "Confirm"
                    ConfirmTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
                    ConfirmTitle.TextSize = 15.000
                    ConfirmTitle.TextTransparency = 0.300
                    ConfirmTitle.TextXAlignment = Enum.TextXAlignment.Left
        
                    BoxColor.Name = "BoxColor"
                    BoxColor.Parent = Title
                    BoxColor.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    BoxColor.Position = UDim2.new(3.26915574, 0, 0.261904776, 0)
                    BoxColor.Size = UDim2.new(0, 35, 0, 19)
        
                    BoxColorCorner.CornerRadius = UDim.new(0, 4)
                    BoxColorCorner.Name = "BoxColorCorner"
                    BoxColorCorner.Parent = BoxColor
        
                    ToggleBtn.Name = "ToggleBtn"
                    ToggleBtn.Parent = Toggle
                    ToggleBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    ToggleBtn.BackgroundTransparency = 1.000
                    ToggleBtn.Size = UDim2.new(0, 137, 0, 38)
                    ToggleBtn.Font = Enum.Font.SourceSans
                    ToggleBtn.Text = ""
                    ToggleBtn.TextColor3 = Color3.fromRGB(0, 0, 0)
                    ToggleBtn.TextSize = 14.000
        
                    ColorpickerBtn.MouseEnter:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0}
                        ):Play()
                    end)
        
                    ColorpickerBtn.MouseLeave:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0.3}
                        ):Play()
                    end)
        
                    ColorpickerBtn.MouseButton1Click:Connect(function()
                        if ColorPickerToggled == false then
                            ColorSelection.Visible = true
                            HueSelection.Visible = true
                            Colorpicker:TweenSize(UDim2.new(0, 457, 0, 138), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        else
                            ColorSelection.Visible = false
                            HueSelection.Visible = false
                            Colorpicker:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end
                        ColorPickerToggled = not ColorPickerToggled
                    end)
        
        
                    local function UpdateColorPicker(nope)
                        BoxColor.BackgroundColor3 = Color3.fromHSV(ColorH, ColorS, ColorV)
                        Color.BackgroundColor3 = Color3.fromHSV(ColorH, 1, 1)
        
                        pcall(callback, BoxColor.BackgroundColor3)
                    end
        
                    ColorH =
                        1 -
                        (math.clamp(HueSelection.AbsolutePosition.Y - Hue.AbsolutePosition.Y, 0, Hue.AbsoluteSize.Y) /
                            Hue.AbsoluteSize.Y)
                    ColorS =
                        (math.clamp(ColorSelection.AbsolutePosition.X - Color.AbsolutePosition.X, 0, Color.AbsoluteSize.X) /
                            Color.AbsoluteSize.X)
                    ColorV =
                        1 -
                        (math.clamp(ColorSelection.AbsolutePosition.Y - Color.AbsolutePosition.Y, 0, Color.AbsoluteSize.Y) /
                            Color.AbsoluteSize.Y)
        
                    BoxColor.BackgroundColor3 = preset
                    Color.BackgroundColor3 = preset
                    pcall(callback, BoxColor.BackgroundColor3)
        
                    Color.InputBegan:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                if RainbowColorPicker then
                                    return
                                end
        
                                if ColorInput then
                                    ColorInput:Disconnect()
                                end
        
                                ColorInput =
                                    RunService.RenderStepped:Connect(
                                        function()
                                        local ColorX =
                                            (math.clamp(Mouse.X - Color.AbsolutePosition.X, 0, Color.AbsoluteSize.X) /
                                                Color.AbsoluteSize.X)
                                        local ColorY =
                                            (math.clamp(Mouse.Y - Color.AbsolutePosition.Y, 0, Color.AbsoluteSize.Y) /
                                                Color.AbsoluteSize.Y)
        
                                        ColorSelection.Position = UDim2.new(ColorX, 0, ColorY, 0)
                                        ColorS = ColorX
                                        ColorV = 1 - ColorY
        
                                        UpdateColorPicker(true)
                                    end
                                    )
                            end
                        end
                    )
        
                    Color.InputEnded:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                if ColorInput then
                                    ColorInput:Disconnect()
                                end
                            end
                        end
                    )
        
                    Hue.InputBegan:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                if RainbowColorPicker then
                                    return
                                end
        
                                if HueInput then
                                    HueInput:Disconnect()
                                end
        
                                HueInput =
                                    RunService.RenderStepped:Connect(
                                        function()
                                        local HueY =
                                            (math.clamp(Mouse.Y - Hue.AbsolutePosition.Y, 0, Hue.AbsoluteSize.Y) /
                                                Hue.AbsoluteSize.Y)
        
                                        HueSelection.Position = UDim2.new(0.48, 0, HueY, 0)
                                        ColorH = 1 - HueY
        
                                        UpdateColorPicker(true)
                                    end
                                    )
                            end
                        end
                    )
        
                    Hue.InputEnded:Connect(
                        function(input)
                            if input.UserInputType == Enum.UserInputType.MouseButton1 then
                                if HueInput then
                                    HueInput:Disconnect()
                                end
                            end
                        end
                    )
        
                    ToggleBtn.MouseButton1Down:Connect(
                        function()
                            RainbowColorPicker = not RainbowColorPicker
        
                            if ColorInput then
                                ColorInput:Disconnect()
                            end
        
                            if HueInput then
                                HueInput:Disconnect()
                            end
        
                            if RainbowColorPicker then
                                ToggleCircle:TweenPosition(UDim2.new(0.37, 0,-0.273, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .3, true)
                                TweenService:Create(
                                    ToggleCircle,
                                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                    {BackgroundColor3 =PresetColor}
                                ):Play()
        
                                OldToggleColor = BoxColor.BackgroundColor3
                                OldColor = Color.BackgroundColor3
                                OldColorSelectionPosition = ColorSelection.Position
                                OldHueSelectionPosition = HueSelection.Position
        
                                while RainbowColorPicker do
                                    BoxColor.BackgroundColor3 = Color3.fromHSV(Flux.RainbowColorValue, 1, 1)
                                    Color.BackgroundColor3 = Color3.fromHSV(Flux.RainbowColorValue, 1, 1)
        
                                    ColorSelection.Position = UDim2.new(1, 0, 0, 0)
                                    HueSelection.Position = UDim2.new(0.48, 0, 0, Flux.HueSelectionPosition)
        
                                    pcall(callback, BoxColor.BackgroundColor3)
                                    wait()
                                end
                            elseif not RainbowColorPicker then
                                ToggleCircle:TweenPosition(UDim2.new(0, 0,-0.273, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .3, true)
                                TweenService:Create(
                                    ToggleCircle,
                                    TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                    {BackgroundColor3 = Color3.fromRGB(255,255,255)}
                                ):Play()
        
                                BoxColor.BackgroundColor3 = OldToggleColor
                                Color.BackgroundColor3 = OldColor
        
                                ColorSelection.Position = OldColorSelectionPosition
                                HueSelection.Position = OldHueSelectionPosition
        
                                pcall(callback, BoxColor.BackgroundColor3)
                            end
                        end
                    )
        
                    Confirm.MouseButton1Click:Connect(
                        function()
                            ColorPickerToggled = not ColorPickerToggled
                            Colorpicker:TweenSize(UDim2.new(0, 457, 0, 43), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            wait(.4)
                            Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                        end
                    )
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
                function ContainerContent:Line()
                    local Line = Instance.new("TextButton")
                    local LineCorner = Instance.new("UICorner")
        
                    Line.Name = "Line"
                    Line.Parent = Container
                    Line.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Line.ClipsDescendants = true
                    Line.Position = UDim2.new(0, 0, 0.70091325, 0)
                    Line.Size = UDim2.new(0, 457, 0, 4)
                    Line.AutoButtonColor = false
                    Line.Font = Enum.Font.SourceSans
                    Line.Text = ""
                    Line.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Line.TextSize = 14.000
        
                    LineCorner.CornerRadius = UDim.new(0, 4)
                    LineCorner.Name = "LineCorner"
                    LineCorner.Parent = Line
        
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
                function ContainerContent:Label(text)
                    local labelfunc = {}
                    local Label = Instance.new("TextButton")
                    local LabelCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
        
                    Label.Name = "Label"
                    Label.Parent = Container
                    Label.BackgroundColor3 = Color3.fromRGB(0, 166, 58)
                    Label.ClipsDescendants = true
                    Label.Position = UDim2.new(0.370312512, 0, 0.552631557, 0)
                    Label.Size = UDim2.new(0, 457, 0, 43)
                    Label.AutoButtonColor = false
                    Label.Font = Enum.Font.SourceSans
                    Label.Text = ""
                    Label.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Label.TextSize = 14.000
        
                    LabelCorner.CornerRadius = UDim.new(0, 4)
                    LabelCorner.Name = "LabelCorner"
                    LabelCorner.Parent = Label
        
                    Title.Name = "Title"
                    Title.Parent = Label
                    Title.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.038480062, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(0,0,0)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                    function labelfunc:Refresh(tochange)
                        Title.Text = tochange
                    end
                    return labelfunc
                end
                function ContainerContent:Textbox(text,desc,disapper,callback)
                    if desc == "" then
                        desc = "There is no description for this textbox."
                    end
                    local TextboxDescToggled = false
                    local Textbox = Instance.new("TextButton")
                    local TextboxCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local Description = Instance.new("TextLabel")
                    local TextboxFrame = Instance.new("Frame")
                    local TextboxFrameCorner = Instance.new("UICorner")
                    local TextBox = Instance.new("TextBox")
        
                    Textbox.Name = "Textbox"
                    Textbox.Parent = Container
                    Textbox.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Textbox.ClipsDescendants = true
                    Textbox.Position = UDim2.new(0.0459499061, 0, 0.734449744, 0)
                    Textbox.Size = UDim2.new(0, 457, 0, 43)
                    Textbox.AutoButtonColor = false
                    Textbox.Font = Enum.Font.SourceSans
                    Textbox.Text = ""
                    Textbox.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Textbox.TextSize = 14.000
        
                    TextboxCorner.CornerRadius = UDim.new(0, 4)
                    TextboxCorner.Name = "TextboxCorner"
                    TextboxCorner.Parent = Textbox
        
                    Title.Name = "Title"
                    Title.Parent = Textbox
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(64, 68, 75)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
                    Description.Name = "Description"
                    Description.Parent = Title
                    Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Description.BackgroundTransparency = 1.000
                    Description.Position = UDim2.new(-0.200942323, 0, 0.985714269, 0)
                    Description.Size = UDim2.new(0, 432, 0, 31)
                    Description.Font = Enum.Font.Gotham
                    Description.Text = desc
                    Description.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Description.TextSize = 15.000
                    Description.TextTransparency = 1
                    Description.TextWrapped = true
                    Description.TextXAlignment = Enum.TextXAlignment.Left
        
                    TextboxFrame.Name = "TextboxFrame"
                    TextboxFrame.Parent = Title
                    TextboxFrame.BackgroundColor3 = Color3.fromRGB(50, 53, 59)
                    TextboxFrame.Position = UDim2.new(1.82300889, 0, 0.202380955, 0)
                    TextboxFrame.Size = UDim2.new(0, 161, 0, 26)
        
                    TextboxFrameCorner.CornerRadius = UDim.new(0, 4)
                    TextboxFrameCorner.Name = "TextboxFrameCorner"
                    TextboxFrameCorner.Parent = TextboxFrame
        
                    TextBox.Parent = TextboxFrame
                    TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    TextBox.BackgroundTransparency = 1.000
                    TextBox.Size = UDim2.new(0, 161, 0, 26)
                    TextBox.Font = Enum.Font.Gotham
                    TextBox.Text = ""
                    TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
                    TextBox.TextSize = 15.000
                    TextBox.TextTransparency = 0.300
        
                    TextBox.FocusLost:Connect(
                        function(ep)
                            if ep then
                                if #TextBox.Text > 0 then
                                    pcall(callback, TextBox.Text)
                                    if disapper then
                                        TextBox.Text = ""
                                    end
                                end
                            end
                        end
                    )
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
                function ContainerContent:Bind(text,presetbind,callback)
                    local Key = presetbind.Name
                    local Bind = Instance.new("TextButton")
                    local BindCorner = Instance.new("UICorner")
                    local Title = Instance.new("TextLabel")
                    local Circle = Instance.new("Frame")
                    local CircleCorner = Instance.new("UICorner")
                    local CircleSmall = Instance.new("Frame")
                    local CircleSmallCorner = Instance.new("UICorner")
                    local BindLabel = Instance.new("TextLabel")
        
                    Bind.Name = "Bind"
                    Bind.Parent = Container
                    Bind.BackgroundColor3 = Color3.fromRGB(31, 41, 43)
                    Bind.ClipsDescendants = true
                    Bind.Position = UDim2.new(0.40625, 0, 0.828947306, 0)
                    Bind.Size = UDim2.new(0, 457, 0, 43)
                    Bind.AutoButtonColor = false
                    Bind.Font = Enum.Font.SourceSans
                    Bind.Text = ""
                    Bind.TextColor3 = Color3.fromRGB(0, 0, 0)
                    Bind.TextSize = 14.000
        
                    BindCorner.CornerRadius = UDim.new(0, 4)
                    BindCorner.Name = "BindCorner"
                    BindCorner.Parent = Bind
        
                    Title.Name = "Title"
                    Title.Parent = Bind
                    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    Title.BackgroundTransparency = 1.000
                    Title.Position = UDim2.new(0.0822437406, 0, 0, 0)
                    Title.Size = UDim2.new(0, 113, 0, 42)
                    Title.Font = Enum.Font.Gotham
                    Title.Text = text
                    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
                    Title.TextSize = 15.000
                    Title.TextTransparency = 0.300
                    Title.TextXAlignment = Enum.TextXAlignment.Left
        
                    Circle.Name = "Circle"
                    Circle.Parent = Title
                    Circle.Active = true
                    Circle.AnchorPoint = Vector2.new(0.5, 0.5)
                    Circle.BackgroundColor3 = Color3.fromRGB(211, 211, 211)
                    Circle.Position = UDim2.new(-0.150690272, 0, 0.503000021, 0)
                    Circle.Size = UDim2.new(0, 11, 0, 11)
        
                    CircleCorner.CornerRadius = UDim.new(2, 6)
                    CircleCorner.Name = "CircleCorner"
                    CircleCorner.Parent = Circle
        
                    CircleSmall.Name = "CircleSmall"
                    CircleSmall.Parent = Circle
                    CircleSmall.Active = true
                    CircleSmall.AnchorPoint = Vector2.new(0.5, 0.5)
                    CircleSmall.BackgroundColor3 = Color3.fromRGB(64, 68, 75)
                    CircleSmall.BackgroundTransparency = 1.000
                    CircleSmall.Position = UDim2.new(0.485673368, 0, 0.503000021, 0)
                    CircleSmall.Size = UDim2.new(0, 9, 0, 9)
        
                    CircleSmallCorner.CornerRadius = UDim.new(2, 6)
                    CircleSmallCorner.Name = "CircleSmallCorner"
                    CircleSmallCorner.Parent = CircleSmall
        
                    BindLabel.Name = "BindLabel"
                    BindLabel.Parent = Title
                    BindLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
                    BindLabel.BackgroundTransparency = 1.000
                    BindLabel.Position = UDim2.new(2.56011987, 0, 0, 0)
                    BindLabel.Size = UDim2.new(0, 113, 0, 42)
                    BindLabel.Font = Enum.Font.Gotham
                    BindLabel.Text = Key
                    BindLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
                    BindLabel.TextSize = 15.000
                    BindLabel.TextTransparency = 0.300
                    BindLabel.TextXAlignment = Enum.TextXAlignment.Right
        
                    Bind.MouseEnter:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0}
                        ):Play()
                    end)
        
                    Bind.MouseLeave:Connect(function()
                        TweenService:Create(
                            Title,
                            TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                            {TextTransparency = 0.3}
                        ):Play()
                    end)
        
                    Bind.MouseButton1Click:connect(
                        function()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                BindLabel,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = PresetColor}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                            TweenService:Create(
                                BindLabel,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0}
                            ):Play()
                            BindLabel.Text = "..."
                            local inputwait = game:GetService("UserInputService").InputBegan:wait()
                            if inputwait.KeyCode.Name ~= "Unknown" then
                                BindLabel.Text = inputwait .KeyCode.Name
                                Key = inputwait .KeyCode.Name
                            end
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                BindLabel,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextColor3 = Color3.fromRGB(255,255,255)}
                            ):Play()
                            TweenService:Create(
                                Circle,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundColor3 = Color3.fromRGB(211, 211, 211)}
                            ):Play()
                            TweenService:Create(
                                CircleSmall,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {BackgroundTransparency = 1}
                            ):Play()
                            TweenService:Create(
                                Title,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                            TweenService:Create(
                                BindLabel,
                                TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
                                {TextTransparency = 0.3}
                            ):Play()
                        end
                    )
        
                    game:GetService("UserInputService").InputBegan:connect(
                    function(current, pressed)
                        if not pressed then
                            if current.KeyCode.Name == Key then
                                pcall(callback)
                            end
                        end
                    end
                    )
        
                    Container.CanvasSize = UDim2.new(0, 0, 0, ContainerLayout.AbsoluteContentSize.Y)
                end
                return ContainerContent
            end
            return Tabs
            end
                local win = Flux:Window("Iren Hub (A1)", "MADE BY IRENKISS", Color3.fromRGB(0,166,58), Enum.KeyCode.F2)
                Flux:Notification("ANTI-STAFF AUTOMATICALLY TURNED ON PRESS F2 TO HIDE/SHOW GUI","OK")
        local page2 = win:Tab("FARMING", "http://www.roblox.com/asset/?id=9391995844")
        local page3 = win:Tab("ISLAND/TELEPORT", "http://www.roblox.com/asset/?id=9391995844")
        local page9 = win:Tab("FRUIT/DEF FARM", "http://www.roblox.com/asset/?id=9391995844")
        local page4 = win:Tab("SHOP", "http://www.roblox.com/asset/?id=9391995844")
        local page5 = win:Tab("PLAYER", "http://www.roblox.com/asset/?id=9391995844")
        local page7 = win:Tab("MOB BRING", "http://www.roblox.com/asset/?id=9391995844")
        local page6 = win:Tab("AUTO SKILL", "http://www.roblox.com/asset/?id=9391995844")
       local page1 = win:Tab("MISC", "http://www.roblox.com/asset/?id=9391995844")
        local page8 = win:Tab("SERVER", "http://www.roblox.com/asset/?id=9391995844")
        Weapon = {}
        function FindWeapon()
            for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
                if v:IsA("Tool") then
                   table.insert(Weapon, v.Name)
                end
             end
        end
    
        setfflag("HumanoidParallelRemoveNoPhysics", "False")
        setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
        
        function EquipWeapon(ToolSe)
            if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
                local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
                wait(.1)
                game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
            end
        end
        function Skill(use)
            game:GetService("VirtualInputManager"):SendKeyEvent(true,use,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
            wait(.1)
            game:GetService("VirtualInputManager"):SendKeyEvent(false,use,false,game.Players.LocalPlayer.Character.HumanoidRootPart)
        end
        if not game:GetService("Workspace"):FindFirstChild("LOL") then
            local LOL = Instance.new("Part")
            LOL.Name = "LOL"
            LOL.Parent = game.Workspace
            LOL.Anchored = true
            LOL.Transparency = 0
            LOL.Size = Vector3.new(50,0.5,50)
            game.Workspace["LOL"].CFrame = CFrame.new(0,50000,0)
        end
        Wapon = {}
        for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
            if v:IsA("Tool") then
                table.insert(Wapon ,v.Name)
            end
        end
        for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
            if v:IsA("Tool") then
                table.insert(Wapon, v.Name)
            end
        end
        page1:Line()
        page1:Label("┇ ANTI STUN ┇")
                page1:Line()
                            page1:Toggle("Anti Stun", false, function(bool)
        getgenv().antistun = bool
        while getgenv().antistun do wait()
            pcall(function()
                local hoangashdeptrai = game.Players.LocalPlayer.Character
    repeat
    hoangashdeptrai["DF_Disabled"].Value = false
    hoangashdeptrai.HeartStolen.Value = true
    hoangashdeptrai.Returned.Value = false
    hoangashdeptrai.Hobbied.Value = false
    hoangashdeptrai.HMS.Value = false
    hoangashdeptrai.ChillyPunched.Value = false
    hoangashdeptrai.CandyTouched.Value = false
    hoangashdeptrai.Negative.Value = false
    hoangashdeptrai.OpeSevered.Value = false
    hoangashdeptrai.SnowTouched.Value = false
    hoangashdeptrai.RumbleStun.Value = false
    hoangashdeptrai.GravityCrushed.Value = false

    wait(0.06)
    until hoangashdeptrai.Humanoid.Health == 0
    end)
    end
    end)
    page9:Line()
        page9:Label("┇ WEAPON SPAM (YORU FOR DEF FARMING) ┇")
    page9:Line()
        page9:Slider("Yoru Speed",0,1000,0,function(to)
            Speeds = to
            end)
            page9:Toggle("Yoru Spam (Equip Tool Before Turn On)", false, function(yoru)
            if yoru then
    _G.Yoru = true
    local Players = game:GetService("Players")
    local Plr = Players.LocalPlayer
    local Character = Plr.Character
    local Yoru = Character:FindFirstChild("Yoru")
    local Environment
while _G.Yoru do
wait()
pcall(function()
for i,v in pairs(getconnections(Yoru["RequestAnimation"].OnClientEvent)) do 
    Environment = getsenv(Yoru["AnimationController"])
end
    wait()
for i = 1, Speeds do
Yoru["RequestAnimation"]:FireServer(Environment.PlaceId)
end
end)
wait()
end
else
    _G.Yoru = false
end
end)
 page9:Line()
  page9:Line()
  page9:Slider("Cestus Speed",0,1000,0,function(too)
            Speedss = too
            end)
            page9:Toggle("Seastone Spam (Equip Tool Before Turn On)",false, function(seastone)
if seastone then
    _G.Cestus = true
    local Players = game:GetService("Players")
    local Plr = Players.LocalPlayer
    local Character = Plr.Character
    local Cestus = Character:FindFirstChild("Seastone Cestus")
    local Environment
while _G.Cestus do
wait()
pcall(function()
for i,v in pairs(getconnections(Cestus["RequestAnimation"].OnClientEvent)) do 
    Environment = getsenv(Cestus["AnimationController"])
end
    wait()
for i = 1, Speedss do
Cestus["RequestAnimation"]:FireServer(Environment.PlaceId)
end
end)
end
else
    _G.Cestus = false
end
end)
    page9:Line()
        page9:Label("┇ QUAKE FARM ┇")
    page9:Line()
    page9:Toggle("Quake Farm" , false, function(quakefarm)  --Quake
getgenv().quakefarm1 = quakefarm
        while getgenv().quakefarm1 do wait()
    pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Quake)
local v = x.VTCebvc
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1848.4346923828125, 222, -450.0833740234375), Vector3.new(-0.5347824096679688, -0.43560168147087097, -0.7240573167800903)),100,Vector3.new(-1848.4346923828125, 222, -450.0833740234375), Vector3.new(-0.5347824096679688, -0.43560168147087097, -0.7240573167800903))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1898.96728515625, 225.03367614746094, -200.6829071044922), Vector3.new(-0.9484627842903137, -0.18392488360404968, 0.25805023312568665)),100,Vector3.new(-1898.96728515625, 225.03367614746094, -200.6829071044922), Vector3.new(-0.9484627842903137, -0.18392488360404968, 0.25805023312568665))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1749.58203125, 224.88922119140625, -134.49240112304688), Vector3.new(-0.6882264614105225, -0.40487319231033325, 0.6020150184631348)),100,Vector3.new(-1749.58203125, 224.88922119140625, -134.49240112304688), Vector3.new(-0.6882264614105225, -0.40487319231033325, 0.6020150184631348))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1622.5482177734375, 225.85337829589844, -200.26828002929688), Vector3.new(-0.3189719319343567, -0.7127735018730164, 0.6246685981750488)),100,Vector3.new(-1622.5482177734375, 225.85337829589844, -200.26828002929688), Vector3.new(-0.3189719319343567, -0.7127735018730164, 0.6246685981750488))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(1002.1565551757812, 214, 3349.3857421875), Vector3.new(-0.2978745698928833, -0.6442758440971375, 0.7044001221656799)),100,Vector3.new(1002.1565551757812, 214, 3349.3857421875), Vector3.new(-0.2978745698928833, -0.6442758440971375, 0.7044001221656799))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(2167.46923828125, 213, -631.9636840820312), Vector3.new(0.6589730978012085, -0.6376858949661255, -0.3988874852657318)),100,Vector3.new(2167.46923828125, 213, -631.9636840820312), Vector3.new(0.6589730978012085, -0.6376858949661255, -0.3988874852657318))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(1178.6993408203125, 212.26193237304688, -263.04681396484375), Vector3.new(0.04516664147377014, -0.9571055173873901, 0.28619781136512756)),100,Vector3.new(1178.6993408203125, 212.26193237304688, -263.04681396484375), Vector3.new(0.04516664147377014, -0.9571055173873901, 0.28619781136512756))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1040.117919921875, 215, 1662.1202392578125), Vector3.new(0.9582481980323792, -0.13812202215194702, 0.2503652274608612)), 100,Vector3.new(-1040.117919921875, 215, 1662.1202392578125), Vector3.new(0.9582481980323792, -0.13812202215194702, 0.2503652274608612))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-988.4560546875, 283, 1616.5068359375), Vector3.new(-0.44781866669654846, -0.36267393827438354, 0.8172675371170044)), 100,Vector3.new(-988.4560546875, 283, 1616.5068359375), Vector3.new(-0.44781866669654846, -0.36267393827438354, 0.8172675371170044))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1037.58544921875, 215.7229461669922, 1508.449951171875), Vector3.new(-0.7139230966567993, -0.5779988169670105, 0.39526084065437317)),100,Vector3.new(-1037.58544921875, 215.7229461669922, 1508.449951171875), Vector3.new(-0.7139230966567993, -0.5779988169670105, 0.39526084065437317))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-908.2176513671875, 214, 1621.364990234375), Vector3.new(-0.21460314095020294, -0.40479180216789246, 0.88886958360672)),100,Vector3.new(-908.2176513671875, 214, 1621.364990234375), Vector3.new(-0.21460314095020294, -0.40479180216789246, 0.88886958360672))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-248.8604736328125, 273.4266052246094, 355.64453125), Vector3.new(0.6645273566246033, -0.5016912817955017, -0.5538134574890137)),100,Vector3.new(-248.8604736328125, 273.4266052246094, 355.64453125), Vector3.new(0.6645273566246033, -0.5016912817955017, -0.5538134574890137))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-319.3795471191406, 272.3931884765625, 388.7362060546875), Vector3.new(0.5347911715507507, -0.7442643046379089, -0.40008631348609924)),100,Vector3.new(-319.3795471191406, 272.3931884765625, 388.7362060546875), Vector3.new(0.5347911715507507, -0.7442643046379089, -0.40008631348609924))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-315.74334716796875, 270.4518737792969, 307.21185302734375), Vector3.new(0.4924789369106293, -0.6783868670463562, -0.5452118515968323)),100,Vector3.new(-315.74334716796875, 270.4518737792969, 307.21185302734375), Vector3.new(0.4924789369106293, -0.6783868670463562, -0.5452118515968323))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-178.00997924804688, 272.4919128417969, 390.1238708496094), Vector3.new(0.6851771473884583, -0.678036093711853, -0.26608139276504517)),100,Vector3.new(-178.00997924804688, 272.4919128417969, 390.1238708496094), Vector3.new(0.6851771473884583, -0.678036093711853, -0.26608139276504517))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-159.9521026611328, 269.81768798828125, 312.1455993652344), Vector3.new(0.6065837144851685, -0.7200759649276733, -0.33696722984313965)),100,Vector3.new(-159.9521026611328, 269.81768798828125, 312.1455993652344), Vector3.new(0.6065837144851685, -0.7200759649276733, -0.33696722984313965))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(89.97474670410156, 299.3000183105469, -936.1035766601562), Vector3.new(0.2870140075683594, -0.6174480319023132, -0.7323803305625916)),100,Vector3.new(89.97474670410156, 299.3000183105469, -936.1035766601562), Vector3.new(0.2870140075683594, -0.6174480319023132, -0.7323803305625916))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1169.5670166015625, 219.90908813476562, -1588.0274658203125), Vector3.new(0.015137090347707272, -0.6970996260643005, -0.7168144583702087)),100,Vector3.new(-1169.5670166015625, 219.90908813476562, -1588.0274658203125), Vector3.new(0.015137090347707272, -0.6970996260643005, -0.7168144583702087))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1201.4923095703125, 254.11367797851562, -1660.2674560546875), Vector3.new(0.04675392061471939, -0.6955714225769043, -0.7169341444969177)),100,Vector3.new(-1201.4923095703125, 254.11367797851562, -1660.2674560546875), Vector3.new(0.04675392061471939, -0.6955714225769043, -0.7169341444969177))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1288.0887451171875, 245.90695190429688, -1653.00537109375), Vector3.new(0.025024037808179855, -0.7537118196487427, -0.6567284464836121)),100,Vector3.new(-1288.0887451171875, 245.90695190429688, -1653.00537109375))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1339.789306640625, 245.81817626953125, -1634.641845703125), Vector3.new(0.07458476722240448, -0.6587507128715515, -0.7486552596092224)),100,Vector3.new(-1339.789306640625, 245.81817626953125, -1634.641845703125), Vector3.new(0.07458476722240448, -0.6587507128715515, -0.7486552596092224))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1432.3958740234375, 256.3514709472656, -1652.33984375), Vector3.new(0.007446270436048508, -0.6148971319198608, -0.7885722517967224)),100,Vector3.new(-1432.3958740234375, 256.3514709472656, -1652.33984375), Vector3.new(0.007446270436048508, -0.6148971319198608, -0.7885722517967224))
wait(0.1)
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(v,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,CFrame.new(Vector3.new(-1270.039794921875, 263.09088134765625, -1793.016357421875), Vector3.new(0.32165566086769104, -0.4306340515613556, -0.8432627320289612)),100,Vector3.new(-1270.039794921875, 263.09088134765625, -1793.016357421875), Vector3.new(0.32165566086769104, -0.4306340515613556, -0.8432627320289612))
wait(0.1)
local args = {
    [1] = 939731.82,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandCaver"):WaitForChild("Stones"):WaitForChild("Stone"),
    [5] = CFrame.new(-1049.37659, 215, 1646.53479, 0.999993384, 0.00298895454, -0.00207511522, -0, 0.570294261, 0.821440458, 0.00363867474, -0.821435034, 0.570290446),
    [6] = 100,
    [7] = Vector3.new(-43.01959991455078, 216.19691467285156, -200.375732421875)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(-1048.52368, 215, 1683.08154, 0.969707072, 0.241547287, -0.0363770761, -0, 0.148920938, 0.988849103, 0.244271129, -0.958893955, 0.144409657),
    [6] = 100,
    [7] = Vector3.new(-47.42127990722656, 215.7339324951172, -202.49114990234375)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(-987.150879, 215, 1667.19971, 0.914944112, 0.390497267, -0.101927787, -0, 0.252558649, 0.96758157, 0.403580725, -0.885283053, 0.231077015),
    [6] = 100,
    [7] = Vector3.new(-42.87627029418945, 216.94845581054688, -200.90744018554688)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = 939731.82,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(4572.08203, 219.497177, 5281.18506, 0.653541863, -0.156973243, 0.740433991, -0, 0.978257895, 0.207392335, -0.756890297, -0.135539576, 0.639332533),
    [6] = 100,
    [7] = Vector3.new(-47.45362854003906, 217.59515380859375, -201.30079650878906)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(2150.41626, 216.977631, -620.214966, 0.542576551, -0.533092737, 0.649170995, -1.49011612e-08, 0.772816777, 0.634629369, -0.840006411, -0.34433502, 0.419312209),
    [6] = 100,
    [7] = Vector3.new(-45.78693389892578, 215.7545623779297, -203.71022033691406)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(2168.10864, 215.442368, -648.2948, 0.999150634, 0.0168674383, -0.0375972874, -9.31322686e-10, 0.912387192, 0.409328282, 0.0412076041, -0.408980608, 0.911612153),
    [6] = 100,
    [7] = Vector3.new(-46.27024459838867, 217.59515380859375, -199.48678588867188)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(2195.74121, 214.947037, -633.380371, 0.627761662, 0.333073497, -0.703546286, 1.49011612e-08, 0.903829932, 0.42789197, 0.778405607, -0.268614173, 0.567389786),
    [6] = 100,
    [7] = Vector3.new(-46.923622131347656, 217.59515380859375, -202.7979278564453)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(1135.47461, 221.200058, -3280.20483, 0.816403747, -0.3288019, 0.474736094, -0, 0.822080135, 0.569371998, -0.577481687, -0.464837432, 0.671149135),
    [6] = 100,
    [7] = Vector3.new(-80.33919525146484, 215.00575256347656, -884.0109252929688)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(1118.67578, 221.866333, -3374.4729, -0.639936566, -0.691518486, 0.33508715, 1.49011612e-08, 0.436068505, 0.89991349, -0.76842773, 0.575887561, -0.279056191),
    [6] = 100,
    [7] = Vector3.new(-76.82958221435547, 216.3629913330078, -881.9810791015625)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(1069.92468, 221.200027, -3394.1084, -0.861241043, 0.33216387, -0.384618104, -0, 0.756829202, 0.653612733, 0.508196771, 0.562918127, -0.651812315),
    [6] = 100,
    [7] = Vector3.new(-76.7877426147461, 216.2060546875, -882.0983276367188)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(995.937073, 221.200043, -3273.97607, -0.255309492, 0.30323121, -0.918078482, -7.45057971e-09, 0.949547052, 0.313624918, 0.9668594, 0.0800714269, -0.242428377),
    [6] = 100,
    [7] = Vector3.new(-81.3091049194336, 216.05020141601562, -884.2357788085938)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(-368.032806, 229.199478, -483.861359, -0.0814099088, 0.579163373, -0.811136484, -3.72528985e-09, 0.813837826, 0.581092179, 0.996680737, 0.0473066643, -0.0662544593),
    [6] = 100,
    [7] = Vector3.new(-80.90997314453125, 216.20582580566406, -884.9806518554688)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(-420.017883, 216.896423, -200.341003, 0.0463441163, 0.618907869, -0.784095347, -1.86264515e-09, 0.784938812, 0.619573534, 0.998925626, -0.0287135858, 0.0363772884),
    [6] = 100,
    [7] = Vector3.new(-81.10070037841797, 216.1497344970703, -884.7239379882812)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(61.3417625, 224.774521, -23.4785957, 0.00760989357, 0.389301956, -0.921078801, -2.32830644e-10, 0.921105444, 0.389313221, 0.999971032, -0.00296263187, 0.00700951461),
    [6] = 100,
    [7] = Vector3.new(-76.59005737304688, 216.6658477783203, -884.2120361328125)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(217.870819, 216.467972, 3.97104454, -0.0854031295, 0.680155993, -0.728075624, -0, 0.730745435, 0.682650089, 0.996346474, 0.0583004542, -0.0624079481),
    [6] = 100,
    [7] = Vector3.new(-81.43997955322266, 216.1997833251953, -882.7205200195312)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(78.618309, 225.43338, -250.790756, -0.931004524, -0.221155539, 0.290380716, -1.4901163e-08, 0.795546651, 0.605892539, -0.365007848, 0.564088702, -0.740657389),
    [6] = 100,
    [7] = Vector3.new(3.1437907218933105, 215.29119873046875, -200.572509765625)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)
local args = {
    [1] = v,
    [2] = "QuakePower4",
    [3] = "StopCharging",
    [4] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [5] = CFrame.new(-82.7837143, 213.28685, -292.159271, -0.953455389, -0.273064911, 0.127900094, -0, 0.424164504, 0.90558517, -0.301534206, 0.86343509, -0.404421896),
    [6] = 100,
    [7] = Vector3.new(-46.6608772277832, 215.0364990234375, -201.5364227294922)
}

game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(unpack(args))
wait(0.1)

end)
end
end)
    page9:Toggle("Refresh For Balance Lag (Every 30mins)",false,function(fc)
        getgenv().qw = fc
        while getgenv().qw do wait(1800)
            pcall(function()
game.Players.LocalPlayer.Character.Humanoid.Health = 0
game:GetService("Workspace").LocalPlayer.CharacterTrait.Health = 0
            end)
        end
    end)
       page9:Toggle("Auto Spawn",_G.AutoSpawn,function(spawn)
            _G.AutoSpawn = spawn
        end)
            spawn(function()
            while wait() do
                if _G.AutoSpawn then
                    pcall(function()
                        if game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == true then
                            repeat wait(3)
                                for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Load.MouseButton1Click)) do
                                    v.Function()
                                end
                            until game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == false
                        end
                    end)
                end
            end
            end)
    page9:Line()
        page9:Label("┇ LIGHT FARM ┇")
    page9:Line()
    page9:Toggle("Light Farm" , false, function(farmlight)  --Light
getgenv().farmlight1 = farmlight
 while getgenv().farmlight1 do wait()
pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Light)
local v = x.VTCrv
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-988.4560546875, 283, 1616.5068359375), Vector3.new(-0.44781866669654846, -0.36267393827438354, 0.8172675371170044)),workspace.IslandCaver.Stones.Stone, 100)
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1037.58544921875, 215.7229461669922, 1508.449951171875), Vector3.new(-0.7139230966567993, -0.5779988169670105, 0.39526084065437317)),workspace.IslandCaver.Stones.Stone, 100)
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-908.2176513671875, 214, 1621.364990234375), Vector3.new(-0.21460314095020294, -0.40479180216789246, 0.88886958360672)),workspace.IslandCaver.Stones.Stone, 100)
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-248.8604736328125, 273.4266052246094, 355.64453125), Vector3.new(0.6645273566246033, -0.5016912817955017, -0.5538134574890137)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-319.3795471191406, 272.3931884765625, 388.7362060546875), Vector3.new(0.5347911715507507, -0.7442643046379089, -0.40008631348609924)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-315.74334716796875, 270.4518737792969, 307.21185302734375), Vector3.new(0.4924789369106293, -0.6783868670463562, -0.5452118515968323)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-178.00997924804688, 272.4919128417969, 390.1238708496094), Vector3.new(0.6851771473884583, -0.678036093711853, -0.26608139276504517)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-159.9521026611328, 269.81768798828125, 312.1455993652344), Vector3.new(0.6065837144851685, -0.7200759649276733, -0.33696722984313965)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(89.97474670410156, 299.3000183105469, -936.1035766601562), Vector3.new(0.2870140075683594, -0.6174480319023132, -0.7323803305625916)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1169.5670166015625, 219.90908813476562, -1588.0274658203125), Vector3.new(0.015137090347707272, -0.6970996260643005, -0.7168144583702087)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1201.4923095703125, 254.11367797851562, -1660.2674560546875), Vector3.new(0.04675392061471939, -0.6955714225769043, -0.7169341444969177)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1288.0887451171875, 245.90695190429688, -1653.00537109375), Vector3.new(0.025024037808179855, -0.7537118196487427, -0.6567284464836121)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1339.789306640625, 245.81817626953125, -1634.641845703125), Vector3.new(0.07458476722240448, -0.6587507128715515, -0.7486552596092224)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1432.3958740234375, 256.3514709472656, -1652.33984375), Vector3.new(0.007446270436048508, -0.6148971319198608, -0.7885722517967224)),workspace.IslandCaver.Stones.Stone, 100)

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StopCharging",CFrame.new(Vector3.new(-1270.039794921875, 263.09088134765625, -1793.016357421875), Vector3.new(0.32165566086769104, -0.4306340515613556, -0.8432627320289612)),workspace.IslandCaver.Stones.Stone, 100)

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(1006.49609, 214, 3343.88672, -0.658374071, 0.456948608, -0.598114967, 1.49011612e-08, 0.794635653, 0.607086658, 0.752690911, 0.399690121, -0.523167491),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(63.7783852, 224.092834, -22.6948109, 0.880218983, -0.199063435, 0.430799752, -0, 0.907772779, 0.419462502, -0.47456789, -0.369218856, 0.799038708),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(78.0910568, 224.257538, -250.038528, -0.929546118, 0.140650496, -0.340824872, 7.4505806e-09, 0.924381137, 0.381470531, 0.368706048, 0.354594439, -0.859254777),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-83.3654709, 213.507431, -291.45694, -0.803052127, 0.286845595, -0.522328377, -1.49011647e-08, 0.876523972, 0.481358171, 0.59590888, 0.386555701, -0.703894377),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-361.610687, 226.601395, -483.790314, -0.127329662, -0.748218894, 0.651118755, -7.4505806e-09, 0.656462073, 0.754359066, -0.991860449, 0.0960522816, -0.0835870951),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-417.081055, 215.650604, -199.940262, -0.999979317, 0.00165595487, -0.00622563809, -0, 0.966397822, 0.257051706, 0.00644210819, 0.257046402, -0.966377676),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(1189.82031, 209.504807, -253.076477, -0.0244355015, 0.911407471, -0.410779238, -9.31322575e-10, 0.410901964, 0.911679626, 0.9997015, 0.0222773496, -0.0100405924),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(997.100281, 221.200043, -3273.66992, -0.999911904, 0.00796189532, -0.0106200371, 4.65661287e-10, 0.80011332, 0.599848986, 0.0132731665, 0.599796116, -0.800042808),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(1135.32324, 221.200058, -3279.3938, -0.962248683, 0.192036361, -0.192872062, -1.49011612e-08, 0.708640337, 0.705569923, 0.272172004, 0.67893374, -0.681888163),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(1069.11377, 221.200027, -3392.5415, -0.242442578, 0.617383361, -0.748371243, -0, 0.771385014, 0.636368871, 0.970165849, 0.154282913, -0.187016517),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(1119.41455, 221, -3377.73682, -0.973147631, 0.127094254, -0.191913262, -7.45057971e-09, 0.833746493, 0.552147388, 0.230181754, 0.537320912, -0.811358511),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1848.74072, 222, -445.570709, -0.737809598, -0.349238694, 0.577641249, -0, 0.855753541, 0.517383814, -0.675008953, 0.381730735, -0.631383121),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1934.89453, 222.827698, -287.688354, -0.201752827, 0.466540843, -0.86118263, 7.45058149e-09, 0.87926352, 0.476335943, 0.979436576, 0.0961021185, -0.177393854),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1902.58936, 225.020691, -200.327271, 0.482329607, 0.390431523, -0.784169197, 1.49011612e-08, 0.895180702, 0.445703268, 0.875989795, -0.214975893, 0.431772202),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(219.922928, 216.962555, 5.62356806, 0.7696684, -0.491379827, 0.407622814, -0, 0.63846314, 0.769652426, -0.638443828, -0.592377126, 0.491404891),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1750.64819, 226.240067, -135.158188, 0.741380215, -0.609925508, 0.279904127, -0, 0.417091757, 0.908864439, -0.671085238, -0.673814118, 0.309223562),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1622.35095, 225.656448, -196.633286, 0.243688434, -0.768282771, 0.591910183, -0, 0.610308826, 0.79216361, -0.96985364, -0.193041116, 0.148725212),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))

local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1011.52802, 325.579163, 1688.44336, 0.0565236248, -0.625209868, 0.778407216, -1.86264515e-09, 0.779653728, 0.626210988, -0.998401344, -0.0353957154, 0.0440688469),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))
wait(0.2)
end)
end
end)
page9:Button("Create Light Farm Spot", function()
baseplatee = Instance.new("Part", workspace)
baseplatee.Size = Vector3.new(50, 1, 50)
baseplatee.CFrame = CFrame.new(100, 2998, 800)
baseplatee.Anchored = true
end)
page9:Button("Teleport To Farm Spot", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(100, 3000, 800)
end)
page9:Toggle("Auto Teleport To Farm Spot (Light)",false, function(tpspotlight)
getgenv().lightttt2 = tpspotlight
        while getgenv().lightttt2 do wait()
    pcall(function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(100, 3000, 800)
end)
    end
    end)

page9:Toggle("Light Farm Teleport To Mob",false, function(tpmodelight)
getgenv().lightttt = tpmodelight
        while getgenv().lightttt do wait()
    pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Light)
local v = x.VTCrv
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StartCharging",CFrame.new(Vector3.new(-1037.58544921875, 215.7229461669922, -5000.449951171875), Vector3.new(-0.7139230966567993, -0.5779988169670105, 0.39526084065437317)),workspace.IslandCaver.Stones.Stone, 100)
local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1084.59033, -9763.44336, 501.375885, -0, 0.995015204, 0.0997241139, 0.0880244896, -0.099337019, 0.991152883, 0.996118307, 0.00877816416, -0.08758571),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))
wait(0.01)
end)
end
end)
page9:Line()
page9:Label("┇ OTHER FRUIT FARM ┇")
page9:Line()
page9:Toggle("Teleport To Mob (Include Krizma Cave)",false,function(req)
        getgenv().bringmob01 = req
        while getgenv().bringmob01 do wait()
    pcall(function()
 for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
            if string.find(v.Name, "Crab") or string.find(v.Name, "Bandit") or string.find(v.Name, "Thief") or string.find(v.Name, "Bruno") or string.find(v.Name, "Bucky") 
              or string.find(v.Name, " Vokun") or string.find(v.Name, "Fred") or string.find(v.Name, "Frey") or string.find(v.Name, "Fri") or string.find(v.Name, "Fru") or string.find(v.Name, "Angry") 
             or string.find(v.Name, "Cave ") or string.find(v.Name, "Thug") or string.find(v.Name, "Gunslinger") or string.find(v.Name, "Gunner") or string.find(v.Name, "Buster") or string.find(v.Name, "Boar")
              and v:FindFirstChild("HumanoidRootPart") then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v:FindFirstChild("HumanoidRootPart").CFrame + Vector3.new(0, 15, 0)
wait(0.5)
end
end
    end)
    end
    end)
    page9:Toggle("Teleport To Mob (Except Krizma Cave)",false,function(mob)
        getgenv().bringmob04 = mob
        while getgenv().bringmob04 do wait()
    pcall(function()
 for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
            if string.find(v.Name, "Crab") or string.find(v.Name, "Bandit") or string.find(v.Name, "Thief") 
              or string.find(v.Name, " Vokun") or string.find(v.Name, "Fred") or string.find(v.Name, "Frey") or string.find(v.Name, "Fri") or string.find(v.Name, "Fru") or string.find(v.Name, "Angry") 
             or string.find(v.Name, "Cave ") or string.find(v.Name, "Thug") or string.find(v.Name, "Gunslinger") or string.find(v.Name, "Boar")
              and v:FindFirstChild("HumanoidRootPart") then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v:FindFirstChild("HumanoidRootPart").CFrame + Vector3.new(0, 15, 0)
wait(0.5)
end
end
    end)
    end
    end)
page9:Toggle("Float with platform (turn on when farm)", false, function(plat)
getgenv().flat11 = plat
        while getgenv().flat11 do wait()
    pcall(function()
 local char = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,-3.125,0)
	    local b101 = Instance.new("Part")
	    b101.Shape = "Block"
	    b101.Material = "Glass"
	    b101.BrickColor = BrickColor.new("Hot Pink")
        b101.Anchored = true
	    b101.Parent = game.Workspace
	    b101.CFrame = char
        b101.Size = Vector3.new(10, 0.65, 10)
wait()
        b101:Destroy()

end)
   end
    end)
    
page1:Line()
        page1:Label("┇ FAKE THING ┇")
        page1:Line()
        page1:Button("Hide Name", function()
game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Nametag.TextColor3 = Color3.new(255,0,0)
game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Nametag.Text = "Irenkiss"
game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Header.Text = "MADE BY"
end)
        page1:Button("Fake Reset Stats",function()
        local Players = game:GetService("Players") local cache = {} function lol(name) if cache[name] then return cache[name] end local player = Players:FindFirstChild(name) if player then cache[name] = player.UserId return player.UserId end local id pcall(function () id = Players:lol(name) end) cache[name] = id return id end local ehh = game.Players.LocalPlayer.Name local Final = lol(ehh) 
    game.Workspace.UserData["User_"..Final].Data.MeleeLevel.Value = 1
    game.Workspace.UserData["User_"..Final].Data.SniperLevel.Value = 1
    game.Workspace.UserData["User_"..Final].Data.DefenseLevel.Value = 1
    game.Workspace.UserData["User_"..Final].Data.SwordLevel.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.Cash.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.Bounty.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.DevilFruit.Value = "None"
    game:GetService("Workspace").UserData["User_"..Final].Data.DevilFruit2.Value = "None"
    game:GetService("Workspace").UserData["User_"..Final].Data.Kills.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.DefenseExp.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.MeleeExp.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.SniperExp.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.SwordExp.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.HakiLevel.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.HakiExp.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT1Defense.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT2Defense.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT1Melee.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT2Melee.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT1Sniper.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT2Sniper.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT1Sword.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.DFT2Sword.Value = 1
    game:GetService("Workspace").UserData["User_"..Final].Data.FishCaught.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.ExpertiseLevel.Value = 0
    game:GetService("Workspace").UserData["User_"..Final].Data.ExpertiseExp.Value = 0
    game.Players.LocalPlayer.Character.CharacterTrait.HealthMax.Value = 119
    game:GetService("Workspace").UserData["User_"..Final].HakiBar.Value = 0
    end)
            page1:Textbox("Fake Level", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.TotalLevel.Text = "Total Level: "..Value
        end)
            page1:Textbox("Fake Defense", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Defense.Text = "Defense: "..Value
            end)
        page1:Textbox("Fake Melee", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Melee.Text = "Melee: "..Value
        end)
            page1:Textbox("Fake Sniper", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Sniper.Text = "Sniper: "..Value
            end)
        page1:Textbox("Fake Sword", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Sword.Text = "Sword: "..Value
        end)
        page1:Textbox("Fake Haki", "", true, function(Value)
            game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.Haki.Text = "Haki: "..Value
    end)
                page1:Textbox("Fake Gems", "", true, function(Value)
       game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.A.Gems.GemsAmount.Text = "" ..Value
    end)
            page1:Textbox("Fake Beri", "", true, function(Value)
       game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.A.Beri.BeriAmount.Text = "" ..Value
    end)
        page1:Textbox("Fake Bounty", "", true, function(Value)
       game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.A.Bounty.BountyAmount.Text = "" ..Value
    end)
         page1:Textbox("Fake Kills", "", true, function(Value)
       game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.A.Kills.KillsAmount.Text = "" ..Value
    end)   
        page1:Textbox("Fake Fish", "", true, function(Value)
       game:GetService("Players").LocalPlayer.PlayerGui.Menu.Frame.C.Frame.A.Fish.FishAmount.Text = "" ..Value
    end)
    page4:Line()
             page4:Label("┇ DRINK BUYING ┇")
                 page4:Line()
        local tabledrink = {
            "Lemonade+",
            "Lemonade",
            "Smoothie+",
            "Smoothie",
            "Juice+",
            "Juice",
            "Cider+",
            "Cider",
        }
        page4:Dropdown("Select Drink",tabledrink,function(drink)
            getgenv().selectdrink = drink
        end)
        
            page4:Textbox("Amount","Amount",true,function(amount)
          getgenv().amountdrink = amount
        end)
        
        page4:Button("Buy Drink",function()
            local buydrink = getgenv().selectdrink
            local amountdrinkbuy = getgenv().amountdrink
            if buydrink == "Cider+" then
    for i = 1,amountdrink do
    local args = {
        [1] = "Cider+"
    }
    
    workspace.Merchants.BetterDrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    elseif buydrink == "Lemonade+" then
        
    for i = 1,amountdrink do
    local args = {
        [1] = "Lemonade+"
    }
    
    workspace.Merchants.BetterDrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
            elseif buydrink == "Juice+" then
    for i = 1,amountdrink do
    local args = {
        [1] = "Juice+"
    }
    
    workspace.Merchants.BetterDrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    elseif buydrink == "Smoothie+" then
        for i = 1,amountdrink do
    
    local args = {
        [1] = "Smoothie+"
    }
    
    workspace.Merchants.BetterDrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    
    
            elseif buydrink == "Cider" then
    for i = 1,amountdrink do
    local args = {
        [1] = "Cider"
    }
    
    workspace.Merchants.DrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    elseif buydrink == "Lemonade" then
        for i = 1,amountdrink do
    
    local args = {
        [1] = "Lemonade"
    }
    
    workspace.Merchants.DrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    elseif buydrink == "Juice" then
            for i = 1,amountdrink do
    local args = {
        [1] = "Juice"
    }
    
    workspace.Merchants.DrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    elseif buydrink == "Smoothie" then
        for i = 1,amountdrink do
    
    local args = {
        [1] = "Smoothie"
    }
    
    workspace.Merchants.DrinkMerchant.Clickable.Retum:FireServer(unpack(args))
    end
    end
        end)
        page4:Button("Instant Drink",function()
                    for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                    if v:IsA("Tool") and string.find(v.Name, "Juice") or string.find(v.Name, "Milk") or string.find(v.Name, "Cider") or string.find(v.Name, "Lemonade") or string.find(v.Name, "Smoothie") or string.find(v.Name, "Golden") then
                                            game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                                            game:GetService'VirtualUser':CaptureController()
                                            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                    end
        end)
        

    page2:Line()
        page2:Label("┇ ABOUT WEAPON ┇")
            page2:Line()
        function FindWeapon()
            for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
                if v:IsA("Tool") then
                   table.insert(Weapon, v.Name)
                end
             end
        end
        FindWeapon()
        local findweapon1 = page2:Dropdown("Sellect Weapon", Weapon, function(v)
            _G.weapon = v
        end)
        page2:Button("Refresh Weapon", function()
            findweapon1:Clear()
            Wapon = {}
            for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
                if v:IsA("Tool") then
                    findweapon1:Add(v.Name)
                end
            end
            for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
                if v:IsA("Tool") then
                    findweapon1:Add(v.Name)
                end
            end
        end)
        page2:Toggle("Auto Equip",false,function(bool)
            _G.Equip = bool
        end)
            spawn(function()
            while wait() do
                if _G.Equip then
                    EquipWeapon(_G.weapon)
                end
            end
        end)
        
        page2:Toggle("Auto Attack", false, function(v)
            getgenv().autoattack = v
            while getgenv().autoattack do wait()
                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                    if v.Name == _G.weapon then v:Activate() 
                    end
                end
            end
        end)
        
    page2:Line()
    page2:Label("┇  ALT FARMING ┇ ")
        page2:Line()
    page2:Toggle("Auto Spawn",_G.AutoSpawn,function(spawn)
            _G.AutoSpawn = spawn
        end)
            spawn(function()
            while wait() do
                if _G.AutoSpawn then
                    pcall(function()
                        if game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == true then
                            repeat wait(4)
                                for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Load.MouseButton1Click)) do
                                    v.Function()
                                end
                            until game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == false
                        end
                    end)
                end
            end
            end)
                page2:Toggle("Auto Teleport To Farm Spot",false,function(fg)
        getgenv().qw = fg
        while getgenv().qw do wait()
            pcall(function()
    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1589.06714, 215.999954, 9941.59766, -0.0209177006, -8.02182285e-08, -0.999781191, 4.7343427e-08, 1, -8.1226311e-08, 0.999781191, -4.90321348e-08, -0.0209177006)
            end)
        end
    end)
     page2:Toggle("Auto Die For Farming",false,function(fr)
        getgenv().autodiee = fr
        while getgenv().autodiee do wait()
            pcall(function()
                        if game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == true then
                            repeat wait(5)
game.Players.LocalPlayer.Character.Humanoid.Health = 0
                            until game:GetService("Players").LocalPlayer.PlayerGui.Load.Frame.Visible == false
                        end
                    end)
            end
            end)
 page2:Button("Teleport To Farm Spot (MAIN)",function()
     game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1589.06714, 215.999954, 9941.59766, -0.0209177006, -8.02182285e-08, -0.999781191, 4.7343427e-08, 1, -8.1226311e-08, 0.999781191, -4.90321348e-08, -0.0209177006)
     end)
         page2:Line()
            
    page2:Label("┇  AUTO FARM STATS ┇ ")
    page2:Toggle("Auto Barrels",false, function(state)
if state then
     _G.AutoMixer = true
local user = tostring(game.Players.LocalPlayer.Name)
local StoredLocation = game.workspace[""..user].HumanoidRootPart.CFrame 

spawn(function()
local plrid = tostring(game.Players.LocalPlayer.UserId)
local plr = tostring(game.Players.LocalPlayer)
while _G.AutoMixer do
wait()
pcall(function()
repeat task.wait() until game.Players[""..plr].PlayerGui.Challenges.Frame.Frame.ChallengesFrame.ScrollingFrame["Challenge_13"].Claim.AutoButtonColor == true
workspace.UserData["User_"..plrid].ChallengesRemote:FireServer("Claim","Challenge13")
workspace.UserData["User_"..plrid].ChallengesRemote:FireServer("Claim","Challenge14")
end)
end
end)

function amongus()
for i,v in pairs(game:GetService("Workspace").Barrels:GetDescendants()) do
if v:IsA("ClickDetector") then
fireclickdetector(v)
end
end
for i,v in pairs(game:GetService("Workspace").Island8.Kitchen:GetDescendants()) do
if v:IsA("ClickDetector") then
fireclickdetector(v)
end
end
end

while _G.AutoMixer do
pcall(function()
for i,v in pairs(game:GetService("Workspace").Barrels.Barrels:GetDescendants()) do
if v.Name == "Barrel" then
game.workspace[""..user].HumanoidRootPart.CFrame = v.CFrame + Vector3.new(0, 5, 0)
amongus()
wait(0.1)
end
end
for i,v in pairs(game:GetService("Workspace").Barrels:GetDescendants()) do
if v.Name == "Crate" then
game.workspace[""..user].HumanoidRootPart.CFrame = v.CFrame + Vector3.new(0, 5, 0)
amongus()
wait(0.1)
end
end
game.workspace[""..user].HumanoidRootPart.CFrame = game:GetService("Workspace")["SafeZoneOuterSpacePart"].CFrame * CFrame.new(0, 5, 0)
end)
wait(15)
end
else
   _G.AutoMixer = false
end
end)
page2:Toggle(
        "Auto Drink Mixer",false,function(bool)
        getgenv().autodrinkmixer = bool
        while getgenv().autodrinkmixer do wait(3)
            pcall(function()
                for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                    if v:IsA("Tool") and string.find(v.Name, "Juice") or string.find(v.Name, "Milk") or string.find(v.Name, "Cider") or string.find(v.Name, "Lemonade") or string.find(v.Name, "Smoothie") or string.find(v.Name, "Golden") then
                                            game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                                            game:GetService'VirtualUser':CaptureController()
                                            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        end
                                    end
            end)
    end
    end)
    
    
    
    
    page2:Line()
            
    page2:Label("┇  CHEST AND PRESENT ┇ ")
        page2:Line()
    page2:Toggle("Auto Claim Daily/Hourly Presents",false,function(bool)
        getgenv().claim = bool
        while getgenv().claim do wait()
            pcall(function()
                local Players = game:GetService("Players") local cache = {} function lol(name) if cache[name] then return cache[name] end local player = Players:FindFirstChild(name) if player then cache[name] = player.UserId return player.UserId end local id pcall(function () id = Players:lol(name) end) cache[name] = id return id end local ehh = game.Players.LocalPlayer.Name local Final = lol(ehh) 
                
                local A_1 = "RewardMark"
    local Event = game:GetService("Workspace").UserData["User_"..Final].ClaimRewardDaily
    Event:FireServer(A_1)
    
                local A_1 = "RewardMark"
    local Event = game:GetService("Workspace").UserData["User_"..Final].ClaimRewardHourly
    Event:FireServer(A_1)
    end)
    end
    end)
    page2:Toggle("Auto Collect Chest",false,function(bool)
            getgenv().autochest = bool
            while getgenv().autochest do wait(10)
                pcall(function()
    local apis = game.workspace:GetDescendants()
    for i, v in pairs(apis) do
    if v.Name == "Touch" and v.Parent.Name == "TreasureChestPart" then
    v.Parent.CFrame = game.workspace[game.Players.LocalPlayer.Name].HumanoidRootPart.CFrame
    end
    end
    end)
    end
    end)
    page2:Line()
    page2:Label("┇  COMPASS ┇ ")
        page2:Line()
    page2:Toggle("Auto Claim 1",false,function(bool)
                getgenv().autosam = bool
                while getgenv().autosam do wait(1)
                    pcall(function()
workspace.Merchants.QuestMerchant.Clickable.Retum:FireServer("Claim1")        
end)
                end
    end)
    page2:Toggle("Auto Claim 10",false,function(bool)
        getgenv().claim = bool
        while getgenv().claim do wait(1)
            pcall(function()
                workspace.Merchants.QuestMerchant.Clickable.Retum:FireServer("Claim10")
            end)
        end
    end)
    page2:Toggle("Auto Find Compass",false,function(bool)
            getgenv().autofindsam = bool
            while getgenv().autofindsam do wait()
                pcall(function()
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Compass") and not game.Players.LocalPlayer.Character:FindFirstChild("Compass") then
                            game.Players.LocalPlayer.Backpack:FindFirstChild("Compass").Parent = game.Players.LocalPlayer.Character
                        elseif game.Players.LocalPlayer.Character:FindFirstChild("Compass") then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character:FindFirstChild("Compass").Poser.Value)
                        end
        local args = {
            [1] = getgenv().autofindsam
        }
        local vu = game:GetService("VirtualUser")
    vu:ClickButton1(Vector2.new(500,0))
    local humroot = game.Players.LocalPlayer.Character.HumanoidRootPart
    humroot.CFrame = CFrame.new(v.HitBox.Position)
    
       end)
    end
    end)
    page2:Line()
        page2:Label("┇  DEVIL FRUIT ┇ (F9 TO CHECK FRUIT AND BOX) ")
            page2:Line()
            page2:Toggle("Auto Pickup Fruit", false, function(fruitty)
getgenv().pickkk = fruitty
while getgenv().pickkk do wait()
    pcall(function()
for i,v in pairs(game:GetService("Workspace").Trees.Tree:GetDescendants()) do
if v:IsA("ClickDetector") then
fireclickdetector(v)
end
end
end)
end
end)
page2:Toggle("Rare and Ultra Rare Fruit Checking", false, function(rnu)
getgenv().checkrnu = rnu
while getgenv().checkrnu do wait()
    pcall(function()
    for i, player in pairs(game.Players:GetChildren()) do 
	    for i, backpack in pairs(player:GetChildren()) do
	        if backpack.Name == "Backpack" then 
	            for i, v in pairs(backpack:GetChildren()) do
	                if v.Name == ("Gravity Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Ope Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Venom Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Candy Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Hollow Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Chilly Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Gas Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Flare Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Light Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Smoke Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Sand Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Rumble Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Magma Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Snow Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Quake Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Phoenix Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Dark Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Vampire Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
end	                
end
end
end
wait(2)
end)
end
end)
page2:Toggle("Common and Uncommon Fruit Checking", false, function(cnu)
getgenv().checkcnu = cnu
while getgenv().checkcnu do wait()
    pcall(function()
for i, player in pairs(game.Players:GetChildren()) do 
	    for i, backpack in pairs(player:GetChildren()) do
	        if backpack.Name == "Backpack" then 
	            for i, v in pairs(backpack:GetChildren()) do
	                if v.Name == ("Order Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Gum Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Love Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Bomb Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Smelt Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Diamond Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Barrier Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("String Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Hobby Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Slip Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Chop Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Clone Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Hot Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Clear Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Float Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Spring Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Swim Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Spin Fruit") then
	                print("================================================================================")
	                print(player, v)
	               end
	               if v.Name == ("Luck Fruit") then
	                print("================================================================================")
	                print(player, v)
	               end
	               if v.Name == ("More Fruit") then
	                print("================================================================================")
	                print(player, v)
	               end
	               if v.Name == ("Return Fruit") then
	                print("================================================================================")
	                print(player, v)
	               end
	               if v.Name == ("Alice Fruit") then
	                print("================================================================================")
	                print(player, v)
	                end
end	                
end
end
end
wait(2)
end)
end
end)
page2:Toggle("Fruit Box Checking", false, function(fruitbox)
getgenv().checkfruitbox = fruitbox
while getgenv().checkfruitbox do wait()
    pcall(function()
    for i, player in pairs(game.Players:GetChildren()) do 
	    for i, backpack in pairs(player:GetChildren()) do
	        if backpack.Name == "Backpack" then 
	            for i, v in pairs(backpack:GetChildren()) do
	               if v.Name == ("Common Box") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Uncommon Box") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Rare Box") then
	                print("================================================================================")
	                print(player, v)
	                end
	               if v.Name == ("Ultra Rare Box") then
	                print("================================================================================")
	                print(player, v)
	                end
end
end
end
end
wait(2)
end)
end
end)
page2:Toggle("Compass Checking", false, function(complr)
getgenv().checkcom = complr
while getgenv().checkcom do wait()
    pcall(function()
for i, player in pairs(game.Players:GetChildren()) do 
	    for i, backpack in pairs(player:GetChildren()) do
	        if backpack.Name == "Backpack" then 
	            for i, v in pairs(backpack:GetChildren()) do
	               if v.Name == ("Compass") then
	                print("================================================================================")
	                print(player, v)
	                end
end
end
end
end
wait(2)
end)
end
end)

    page2:Line()
        page2:Label("┇  EXPERTISE ┇ ")
            page2:Line()
         page2:Toggle("Auto Get Expertise",false,function(bool)
                getgenv().autoexp = bool
                while getgenv().autoexp do wait(5)
                    pcall(function()
workspace:WaitForChild("Merchants"):WaitForChild("ExpertiseMerchant"):WaitForChild("Clickable"):WaitForChild("Retum"):FireServer()
end)
                end
    end)
     page2:Line()
    page2:Label(" ┇ HAKI FARM ┇ ")
        page2:Line()
    
    page2:Toggle("Haki Drain", false, function(bool)
            getgenv().autohaki = bool
    function hakiauto()
       local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "Off",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    local args = {
        [1] = "On",
        [2] = 1
    }
    
    workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    
    
    
    end
    while getgenv().autohaki do wait(0)
        hakiauto()
    end
    end)
    page2:Button(
        "Haki 1",
        function()
        for i = 1,5 do
    local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    _G.swim = true
    
    while _G.swim do
    wait(0) do
    local args = {
        [1] = "On",
        [2] = 1
    }
    game.Workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    end
    end
    end
    
       end
    )
    page2:Button(
        "Haki 2",
        function()
        for i = 1,5 do
    local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    _G.swim = true
    
    while _G.swim do
    wait(0) do
    local args = {
        [1] = "Off",
        [2] = 1
    }
    game.Workspace.UserData["User_"..Final].III:FireServer(unpack(args))
    end
    end
    end
    
       end
    )
    page3:Line()
    page3:Label("┇ RAYLEIGH/DARK ATLAS CHECKING ┇")
        page3:Line()
    page3:Button("Tp To Rayleigh",function()
    local emoi = game:GetService("Workspace").Merchants.QuestHakiMerchant.Clickable.Available.Value
    if emoi == true
    then 
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.QuestHakiMerchant.HumanoidRootPart.CFrame
        else
         game.StarterGui:SetCore("SendNotification", {
            Title = "Dum Hub",
            Text = "Rayleigh did not spawn.",
            Duration = 4
          })
    
        end
        end
    )
    page3:Button("Dark Atlas",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Altar.RecepticalEffect.CFrame * CFrame.new(0, 0, 0)
        end
    )

    page3:Line()
        page3:Label("┇ TP ISLAND ┇")
            page3:Line()
            page3:Button("Safe Zone",
    function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace")["SafeZoneOuterSpacePart"].CFrame * CFrame.new(0, 5, 0)
    end
 )
    page3:Button(
        "Cave Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-194.73799133301, 216.99996948242, -891.580078125)
        end
    )
    page3:Button(
        "Sand Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(14.228896141052, 224.99993896484, 83.281211853027)
        end
    )
    page3:Button(
        "Sam Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1285.3370361328, 216.99996948242, -1286.6235351562)
        end
    )
    page3:Button(
        "Club Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1570.5280761719, 253.99995422363, 2080.4025878906)
        end
    )
    page3:Button(
        "Evil Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5232.1577148438, 390, -7718.2651367188)
        end
    )
    page3:Button(
        "Merlin Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1669.6044921875, 216.99995422363, -327.11395263672)
        end
    )
    page3:Button(
        "Snow Mountain Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(6251.4306640625, 485.99990844727, -1612.5649414062)
        end
    )
    page3:Button(
        "Gunslingers Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1185.2060546875, 217.99995422363, 1433.3782958984)
        end
    )
    page3:Button(
        "Snow Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1863.0474853516, 221.99995422363, 3229.9750976562)
        end
    )
    page3:Button(
        "Orange House Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(731.67883300781, 240.99995422363, 1219.0432128906)
        end
    )
    page3:Button(
        "Dead Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2042.4484863281, 487.99990844727, -720.06433105469)
        end
    )
    page3:Button(
        "Desert Castle Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(980.16436767578, 223.99995422363, -3250.3930664062)
        end
    )
    page3:Button(
        "Marine Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3133.8627929688, 275.79977416992, -3653.8217773438)
        end
    )
    page3:Button(
        "Spiral Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5890.7607421875, 215.99995422363, -8.0128145217896)
        end
    )
    page3:Button(
        "Stone Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2645.5473632812, 252.56103515625, 1018.7150268555)
        end
    )
    page3:Button(
        "Race Track Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6370.9833984375, 258.60165405273, 3841.9099121094)
        end
    )
    page3:Button(
        "Pyramid Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(284.54959106445, 215.9998626709, 4954.384765625)
        end
    )
    page3:Button(
        "Red House Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1053.0499267578, 217, 3313.7302246094)
        end
    )
    page3:Button(
        "3 Houses Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1747.6221923828, 217.99995422363, 835.576171875)
        end
    )
    page3:Button(
        "Moon-shaped Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3159.7631835938, 216.99995422363, 1556.4099121094)
        end
    )
    page3:Button(
        "Pursuer Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4848.783203125, 569.99981689453, -7135.171875)
        end
    )
    page3:Button(
        "Vokun Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(4671.2763671875, 216.99998474121, 4893.3154296875)
        end
    )
    page3:Button(
        "Kaizu Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1526.0230712891, 364.99990844727, 10510.020507812)
        end
    )
    page3:Line()
    page3:Label(" ┇ USELESS ISLANDS LIKE YOU!!! ┇")
        page3:Line()
    page3:Button(
        "Bald Island 1",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(187.71101379395, 216, -2272.5571289062)
        end
    )
    page3:Button(
        "Bald Island 2",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2745.2546386719, 215.99995422363, -929.37091064453)
        end
    )
    page3:Button(
        "Tiny ass Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-4003.5473632812, 215.99996948242, -2191.1081542969)
        end
    )
    page3:Button(
        "Small Dead Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-35.314682006836, 228.99995422363, 2147.9790039062)
        end
    )
    page3:Button(
        "Heart Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2211.556640625, 216.99998474121, -1960.4727783203)
        end
    )
    page3:Button(
        "Small Sand Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1204.1204833984, 224, 651.87091064453)
        end
    )
    page3:Button(
        "Smaller Sand Island",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(755.40563964844, 215.99995422363, -1370.9702148438)
        end
    )
    page3:Line()
    page3:Label(" ┇ MERCHANT ┇ ")
        page3:Line()
    page3:Button(
        "Better Drink Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.BetterDrinkMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Drink Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.DrinkMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Sam Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.QuestMerchant.HumanoidRootPart.CFrame
        end
    )
        page3:Button(
        "Friend Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.FriendMerchant.HumanoidRootPart.CFrame
        end
    )
        page3:Button(
        "Heavy Weapons Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.HeavyWeaponsMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Krizma Seller Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.KrizmaMerch.HumanoidRootPart.CFrame
        end
    )
        page3:Button(
        "Flair Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.FlailMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Sword Seller Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.SwordMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Gun Seller Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.SniperMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Merlin Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.QuestFishMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Emotes Teacher Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.EmoteMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "Affinity Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.AffinityMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button(
        "CHEF Merchant",
        function()
           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.FishMerchant.HumanoidRootPart.CFrame
        end
    )
    page3:Button("Expertise Merchant", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Merchants.ExpertiseMerchant.Head.CFrame
    end)
    page4:Line()
    page4:Label("┇ FREE FAKE WEAPON ┇")
        page4:Line()
    page4:Button("Seastone Cestus (500 melee requirement)",function()
            local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    local A_1 = "Seastone Cestus"
    local Event = game:GetService("Workspace").UserData["User_"..Final].UpdateMelee
    Event:FireServer(A_1)
        
    end)
        page4:Button("Aqua Staff (500 melee requirement)",function()
            local Players = game:GetService("Players")
    local cache = {}
    function lol(name)
        if cache[name] then return cache[name] end
        local player = Players:FindFirstChild(name)
        if player then
            cache[name] = player.UserId
            return player.UserId
        end 
    
        local id
        pcall(function ()
            id = Players:lol(name)
        end)
        cache[name] = id
        return id
    end
    local ehh = game.Players.LocalPlayer.Name
    local Final = lol(ehh)
    local A_1 = "Aqua Staff"
    local Event = game:GetService("Workspace").UserData["User_"..Final].UpdateMelee
    Event:FireServer(A_1)
        
    end)
    page4:Line()
    page4:Label(" ┇ GUN ┇ ")
        page4:Line()
    page4:Button("SlingShot ( 1,000 beli )",function()
        local A_1 = "Slingshot"
        local A_2 = 1000
        local Event = game:GetService("Workspace").Merchants.SniperMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                end)
    page4:Button("Stars ( 5,000 beli )",function()
                    local A_1 = "Stars"
        local A_2 = 5000
        local Event = game:GetService("Workspace").Merchants.SniperMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
    end)
    page4:Button("Crossbow ( 7,500 beli )",function()
                    local A_1 = "Crossbow"
        local A_2 = 7500
        local Event = game:GetService("Workspace").Merchants.SniperMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                end
            )
            page4:Button("Flintlock ( 10,000 beli )",function()
                    local A_1 = "Flintlock"
        local A_2 = 10000
        local Event = game:GetService("Workspace").Merchants.SniperMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                end
            )
                        page4:Button("Cannon ( 400,000 beli )",function()
                    local A_1 = "Cannon Ball"
        local A_2 = 400000
        local Event = game:GetService("Workspace").Merchants.HeavyWeaponsMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                end
            )
            page4:Line()
            page4:Label(" ┇ SWORD ┇ ")
                page4:Line()
            page4:Button("Dagger Sword ( 1,000 beli)",function()
        local A_1 = "Dagger"
        local A_2 = 1000
        local Event = game:GetService("Workspace").Merchants.SwordMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                end
            )
            page4:Button("Wakizashi Sword ( 5,000 beli )",function()
                local A_1 = "Wakizashi"
                local A_2 = 5000
                local Event = game:GetService("Workspace").Merchants.SwordMerchant.Clickable.Retum
                Event:FireServer(A_1, A_2)
                        end
                    )
                    page4:Button("Tachi Sword ( 7,500 beli )",function()
                   local A_1 = "Tachi"
                    local A_2 = 75000
                    local Event = game:GetService("Workspace").Merchants.SwordMerchant.Clickable.Retum
                        Event:FireServer(A_1, A_2)
                                end
                            )
                            page4:Button("Katana Sword ( 10,000 beli )",function()
                   local A_1 = "Katana"
                    local A_2 = 10000
                    local Event = game:GetService("Workspace").Merchants.SwordMerchant.Clickable.Retum
                        Event:FireServer(A_1, A_2)
                                end
                            )
                            page4:Button("Flail Sword ( 50,000 beli)",function()
        
        local A_1 = "Flail"
        local A_2 = 50000
        local Event = game:GetService("Workspace").Merchants.FlailMerchant.Clickable.Retum
        Event:FireServer(A_1, A_2)
                            end
                        )
                        page4:Button("Krizma Sword ( 80,000 beli )",function()
        local A_1 = "Krizma"
        local A_2 = 80000
        local Event = game:GetService("Workspace").Merchants.KrizmaMerch.Clickable.Retum
        Event:FireServer(A_1, A_2)
                            end
                        )
    page5:Line()
    page5:Label(" ┇ KILL ALL PLAYER ┇")
    page5:Line()       
    page5:Toggle("Quake Kill All",false, function(qare)
    getgenv().vcm = qare
        while getgenv().vcm do wait()
    pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Quake)
local vp = x.VTCebvc
for i,v in pairs(game.Players:GetChildren()) do
if v.Name ~= game.Players.LocalPlayer.Name then
for i,c in pairs(game.Workspace:GetChildren()) do
if c:IsA("Model") and c.Name == v.Name then
game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(vp,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,c.HumanoidRootPart.CFrame,100,Vector3.new(-290.4129333496094, 266.8401794433594, -103.8988037109375))
end
end
end
end
end)
end
end)
	page5:Toggle("Light Kill All",false, function(lare)
getgenv().ltm = lare
while getgenv().ltm do wait()
pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Light)
local campb = x.VTCrv
for i,v in pairs(game.Players:GetChildren()) do
if v.Name ~= game.Players.LocalPlayer.Name then
for i,c in pairs(game.Workspace:GetChildren()) do
if c:IsA("Model") and c.Name == v.Name then
local args = {
    [1] = campb,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = c.HumanoidRootPart.CFrame,
    [5] = workspace.IslandCaver.Stones.Stone,
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))
end
end
end
end
end)
end
end)

page5:Line()
    page5:Label(" ┇ ABOUT PLAYER ┇")
        page5:Line()
    PlayerName = {}
        for i,v in pairs(game.Players:GetChildren()) do  
            table.insert(PlayerName ,v.Name)
        end
        PlayerName = {}
        for i,v in pairs(game.Players:GetChildren()) do
            table.insert(PlayerName ,v.Name)
        end
        SelectedKillPlayer = ""
        local Player = page5:Dropdown("Selected Player",PlayerName,function(plys) --true/false, replaces the current title "Dropdown" with the option that t
            SelectedKillPlayer = plys
            Choose2 = plys
            SelectedPly:Refresh("Selected Player : "..SelectedKillPlayer)
        end)
        page5:Button("Refresh Player", function()
            PlayerName = {}
            Player:Clear()
            for i,v in pairs(game.Players:GetChildren()) do  
                Player:Add(v.Name)
            end
        end)
                            distance = 4
        page5:Slider("Distance",  0, 100,4,function(bool)
            distance = bool
        end)
        page5:Toggle("Teleport Behind (Distance)",false,function(bool)
            KillPlayer = bool
        end)
        page5:Toggle("Bring Player",false,function(bool)
            _G.BringPlayer = bool
        end)
        page5:Toggle("Spectate Player",false,function(bool)
            Sp = bool
            local plr1 = game.Players.LocalPlayer.Character.Humanoid
            local plr2 = game.Players:FindFirstChild(SelectedKillPlayer)
            repeat wait(.1)
                game.Workspace.Camera.CameraSubject = plr2.Character.Humanoid
            until Sp == false 
            game.Workspace.Camera.CameraSubject = game.Players.LocalPlayer.Character.Humanoid
        end)

        page5:Button("Teleport Player", function()
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild(SelectedKillPlayer).Character.HumanoidRootPart.CFrame
        end)
            page5:Toggle("Esp All Players",false,function(ESP)
        
            ESPPlayer = ESP
            while ESPPlayer do wait()
                UpdatePlayerChams()
            end
        
        end)
            spawn(function()
            while wait() do
                if KillPlayer then
                    game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild(SelectedKillPlayer).Character.HumanoidRootPart.CFrame * CFrame.new(0,0,distance)
                    game.Players:FindFirstChild(SelectedKillPlayer).Character.HumanoidRootPart.Size = Vector3.new(60,60,60)
                    game:GetService'VirtualUser':CaptureController()
                    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                end
            end
        end)
        spawn(function()
            while wait() do
                if _G.BringPlayer then
                    pcall(function()
                        game.Players:FindFirstChild(SelectedKillPlayer).Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,0,-3)
                    end)
                end
            end
        end)
        function isnil(thing)
            return (thing == nil)
        end
        local function round(n)
            return math.floor(tonumber(n) + 0.5)
        end
        Number = math.random(1, 1000000)
        function UpdatePlayerChams()
            for i,v in pairs(game:GetService'Players':GetChildren()) do
                pcall(function()
                    if not isnil(v.Character) then
                        if ESPPlayer then
                            if not isnil(v.Character.Head) and not v.Character.Head:FindFirstChild('NameEsp'..Number) then
                                local bill = Instance.new('BillboardGui',v.Character.Head)
                                bill.Name = 'NameEsp'..Number
                                bill.ExtentsOffset = Vector3.new(0, 1, 0)
                                bill.Size = UDim2.new(1,200,1,30)
                                bill.Adornee = v.Character.Head
                                bill.AlwaysOnTop = true
                                local name = Instance.new('TextLabel',bill)
                                name.Font = "SourceSansBold"
                                name.FontSize = "Size14"
                                name.TextWrapped = true
                                name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
                                name.Size = UDim2.new(1,0,1,0)
                                name.TextYAlignment = 'Top'
                                name.BackgroundTransparency = 1
                                name.TextStrokeTransparency = 0.5
                                if v.Team == game.Players.LocalPlayer.Team then
                                    name.TextColor3 = Color3.new(0, 254, 252)
                                else
                                    name.TextColor3 = Color3.new(0, 254, 252)
                                end
                            else
                                v.Character.Head['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
                            end
                        else
                            if v.Character.Head:FindFirstChild('NameEsp'..Number) then
                                v.Character.Head:FindFirstChild('NameEsp'..Number):Destroy()
                            end
                        end
                    end
                end)
            end
        end
page5:Line()
    page5:Label(" ┇ CAMP PLAYER ┇")
    page5:Line()
    
    page5:Toggle("Quake Camp" , false, function(state)
if state then
_G.AutoQuake = true
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Quake)
local vp = x.VTCebvc
while _G.AutoQuake do
    wait()
    pcall(function()
    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
        if v.Name == Choose2 then
            game:GetService("Players").LocalPlayer.Character.Powers.Quake.RemoteEvent:FireServer(vp,"QuakePower4", "StopCharging",workspace.IslandCaver.Stones.Stone,v.HumanoidRootPart.CFrame,100,Vector3.new(-290.4129333496094, 266.8401794433594, -103.8988037109375))
        end
    end
    end)
    end
else
    _G.AutoQuake = false
end
end)
----------
page5:Toggle("Light Camp" ,false, function(campbylight)
getgenv().campto2 = campbylight
 while getgenv().campto2 do wait()
pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Light)
local lightcode = x.VTCrv
    for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
        if v.Name == Choose2 then
local args = {
    [1] = lightcode,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = v.HumanoidRootPart.CFrame,
    [5] = workspace.IslandCaver.Stones.Stone,
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))
        end
        end
end)
 end
end)
         page5:Toggle("DARK CAMP",false, function(bool)
            _G.Dark = bool
            end)
        spawn(function()
            while wait() do
                if _G.Dark then
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Dark)
local v = x.VTCjebaj
                local args = {
    [1] = v,
    [2] = "DarkPower4",
    [3] = "StartCharging",
    [4] = CFrame.new(-102.340569, 213, 215.227097, -0.982314944, -0.125758141, 0.138716429, -0, 0.74086374, 0.671655476, -0.187236086, 0.659777224, -0.727761507),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("OutterDune"):WaitForChild("Beach"),
    [7] = "Right"
}

game:GetService("Players").LocalPlayer.Character.Powers.Dark.RemoteEvent:FireServer(unpack(args))
local args = {
    [1] = v,
    [2] = "DarkPower4",
    [3] = "StopCharging",
    [4] = CFrame.new(719.440735, 238.200012, 1191.39868, -0.999717414, -0.0117071513, 0.0206902344, -0, 0.870334446, 0.492461145, -0.0237727407, 0.492321968, -0.870088458),
    [5] = workspace:WaitForChild("IslandGrassy"):WaitForChild("Base"):WaitForChild("Path"):WaitForChild("Union"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Dark.RemoteEvent:FireServer(unpack(args))
end
end
end)



page6:Line()
    page6:Label("┇ Spam Fruit Skill ┇")
    page6:Line()
    page6:Slider("Spam Cooldown",0,10,0,function(to)
            Spam1 = to
            end) 
            page6:Toggle("Spam Rumble Skill V",false,function(rum4)
        getgenv().spamrum = rum4
        while getgenv().spamrum do wait()
    pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Rumble)
local v = x.VTCzyhf
local args = {
    [1] = v,
    [2] = "RumblePower4",
    [3] = "Create"
}

game:GetService("Players").LocalPlayer.Character.Powers.Rumble.RemoteEvent:FireServer(unpack(args))
wait(Spam1)
end)
end
end)
page6:Toggle("Spam Light Skill X",false,function(lightkey)
        getgenv().lightsum = lightkey
        while getgenv().lightsum do wait()
    pcall(function()
local x = getsenv(game:GetService("Players").LocalPlayer.Character.Powers.Light)
local v = x.VTCrv
game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(v,"LightPower2", "StartCharging",CFrame.new(Vector3.new(-1037.58544921875, 215.7229461669922, -5000.449951171875), Vector3.new(-0.7139230966567993, -0.5779988169670105, 0.39526084065437317)),workspace.IslandCaver.Stones.Stone, 100)
local args = {
    [1] = v,
    [2] = "LightPower2",
    [3] = "StopCharging",
    [4] = CFrame.new(-1084.59033, -9763.44336, 501.375885, -0, 0.995015204, 0.0997241139, 0.0880244896, -0.099337019, 0.991152883, 0.996118307, 0.00877816416, -0.08758571),
    [5] = workspace:WaitForChild("IslandWindmill"):WaitForChild("Beach"):WaitForChild("Beach"),
    [6] = 100
}

game:GetService("Players").LocalPlayer.Character.Powers.Light.RemoteEvent:FireServer(unpack(args))
wait(Spam1)
end)
end
end)
page6:Line()
    page6:Label("┇ Auto Skill Devil Fruit 1 ┇")
    page6:Line()
        page6:Toggle("Auto Skill Z",false,function(Z)
            _G.SkillZ = Z
        end)
        page6:Toggle("Auto Skill X",false,function(X)
            _G.SkillX = X
            end)
            page6:Toggle("Auto Skill C",false,function(C)
            _G.SkillC = C
            end)
            page6:Toggle("Auto Skill V",false,function(V)
            _G.SkillV = V
            end)
            page6:Toggle("Auto Skill B",false,function(B)
            _G.SkillB = B
            end)
            page6:Toggle("Auto Skill N",false,function(N)
            _G.SkillN = N
            end)
    
    page6:Line()
    page6:Label("┇ Auto Skill Devil Fruit 2 ┇")
    page6:Line()
            page6:Toggle("Auto Skill F",false,function(F)
            _G.SkillF = F
            end)
            page6:Toggle("Auto Skill G",false,function(G)
            _G.SkillG = G
            end)
            page6:Toggle("Auto Skill H",false,function(H)
            _G.SkillH = H
            end)
            page6:Toggle("Auto Skill J",false,function(J)
            _G.SkillJ = J
            end)
            page6:Toggle("Auto Skill K",false,function(K)
            _G.SkillK = K
            end)
            page6:Toggle("Auto Skill L",false,function(L)
            _G.SkillL = L
            end)
    
        spawn(function()
            while wait(.1) do
                if _G.SkillZ then
                    pcall(function()
                        Skill("Z")
                    end)
                end
            end
        end)
            spawn(function()
            while wait(.1) do
                if _G.SkillX then
                    pcall(function()
                        Skill("X")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillC then
                    pcall(function()
                        Skill("C")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillV then
                    pcall(function()
                        Skill("V")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillB then
                    pcall(function()
                        Skill("B")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillN then
                    pcall(function()
                        Skill("N")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillF then
                    pcall(function()
                        Skill("F")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillG then
                    pcall(function()
                        Skill("G")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillH then
                    pcall(function()
                        Skill("H")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillJ then
                    pcall(function()
                        Skill("J")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillK then
                    pcall(function()
                        Skill("K")
                    end)
                end
            end
            end)
            spawn(function()
            while wait(.1) do
                if _G.SkillL then
                    pcall(function()
                        Skill("L")
                    end)
                end
            end
            end)
    page6:Line()
    page6:Label("ABILITY")
    page6:Line()
    page6:Textbox("WalkSpeed", "", true, function(number)
        getgenv().speedx = number
        end)
    page6:Toggle("Enable",false,function(bool)
        if bool == true then
        game.Players.LocalPlayer.Character.CharacterTrait.WS.Value = getgenv().speedx
        else
         game.Players.LocalPlayer.Character.CharacterTrait.WS.Value = 1
        end
    end)
    page6:Textbox("Jump Power", "", true, function(number)
        getgenv().jumpx = number
    end)
    page6:Toggle("Enable",false,function(bool)
        if bool == true then
            game.Players.LocalPlayer.Character.Humanoid.JumpPower = getgenv().jumpx
            else
                game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
        end
    end)
    page8:Line()
    page8:Label("DISCORD SERVER")
        page8:Line()
           page8:Button("Copy Link", function()
            Flux:Notification("Copied To Clipboard","OK")
                setclipboard("https://discord.gg/nSF2sFEjkv")
                toclipboard("https://discord.gg/nSF2sFEjkv")
           end)
    page8:Line()
        page8:Label("SERVER")
            page8:Line()
page8:Button("Low Graphic Mode", function()
workspace:FindFirstChildOfClass('Terrain').WaterWaveSize = 0
	workspace:FindFirstChildOfClass('Terrain').WaterWaveSpeed = 0
	workspace:FindFirstChildOfClass('Terrain').WaterReflectance = 0
	workspace:FindFirstChildOfClass('Terrain').WaterTransparency = 0
	game:GetService("Lighting").GlobalShadows = false
	game:GetService("Lighting").FogEnd = 9e9
	settings().Rendering.QualityLevel = 1
	for i,v in pairs(game:GetDescendants()) do
		if v:IsA("Part") or v:IsA("UnionOperation") or v:IsA("MeshPart") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then
			v.Material = "Plastic"
			v.Reflectance = 0
		elseif v:IsA("Decal") then
			v.Transparency = 1
		elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
			v.Lifetime = NumberRange.new(0)
		elseif v:IsA("Explosion") then
			v.BlastPressure = 1
			v.BlastRadius = 1
		end
	end
	for i,v in pairs(game:GetService("Lighting"):GetDescendants()) do
		if v:IsA("BlurEffect") or v:IsA("SunRaysEffect") or v:IsA("ColorCorrectionEffect") or v:IsA("BloomEffect") or v:IsA("DepthOfFieldEffect") then
			v.Enabled = false
		end
	end
	workspace.DescendantAdded:Connect(function(child)
		coroutine.wrap(function()
			if child:IsA('ForceField') then
				game:GetService('RunService').Heartbeat:Wait()
				child:Destroy()
			elseif child:IsA('Sparkles') then
				game:GetService('RunService').Heartbeat:Wait()
				child:Destroy()
			elseif child:IsA('Smoke') or child:IsA('Fire') then
				game:GetService('RunService').Heartbeat:Wait()
				child:Destroy()
			end
		end)()
	end)


end)
        page8:Button("Rejoin", function()
            local ts = game:GetService("TeleportService")
            local p = game:GetService("Players").LocalPlayer
            ts:Teleport(game.PlaceId, p)
        end)
        local function HttpGet(url)
            return game:GetService("HttpService"):JSONDecode(htgetf(url))
        end
        page8:Button("Server Hop", function()
            local PlaceID = game.PlaceId
            local AllIDs = {}
            local foundAnything = ""
            local actualHour = os.date("!*t").hour
            local Deleted = false
            function TPReturner()
                local Site;
                if foundAnything == "" then
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                else
                    Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                end
                local ID = ""
                if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                    foundAnything = Site.nextPageCursor
                end
                local num = 0;
                for i,v in pairs(Site.data) do
                    local Possible = true
                    ID = tostring(v.id)
                    if tonumber(v.maxPlayers) > tonumber(v.playing) then
                        for _,Existing in pairs(AllIDs) do
                            if num ~= 0 then
                                if ID == tostring(Existing) then
                                    Possible = false
                                end
                            else
                                if tonumber(actualHour) ~= tonumber(Existing) then
                                    local delFile = pcall(function()
                                        -- delfile("NotSameServers.json")
                                        AllIDs = {}
                                        table.insert(AllIDs, actualHour)
                                    end)
                                end
                            end
                            num = num + 1
                        end
                        if Possible == true then
                            table.insert(AllIDs, ID)
                            wait()
                            pcall(function()
                                -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                wait()
                                game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                            end)
                            wait(.1)
                        end
                    end
                end
            end
            function Teleport() 
                while wait() do
                    pcall(function()
                        TPReturner()
                        if foundAnything ~= "" then
                            TPReturner()
                        end
                    end)
                end
            end
            Teleport()
        end)
        page7:Line()
        page7:Label(" MOB BRING ")
                page7:Line()
        Distance = 0
        page7:Slider("Distance",0,-50,0,function(to)
            Distance1 = to
            end)
        page7:Toggle("Bring Bandit",false,function(mob)
            getgenv().bringmob1 = mob
            while getgenv().bringmob1 do wait()
    pcall(function()
                for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                    if string.find(v.Name, "Bandit")
                    
                      and v:FindFirstChild("HumanoidRootPart") then
                        v:FindFirstChild("HumanoidRootPart").Anchored = true
                        v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                     end
                end
    end)
            end
            end)
                page7:Toggle("Bring Thief",false,function(mob)
                    getgenv().bringmob2 = mob
                    while getgenv().bringmob2 do wait()
            pcall(function()
                        for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                            if string.find(v.Name, "Thief")
                            
                              and v:FindFirstChild("HumanoidRootPart") then
                                v:FindFirstChild("HumanoidRootPart").Anchored = true
                                v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                             end
                        end
            end)
        end
    end)
    page7:Toggle("Bring Boar",false,function(mob)
        getgenv().bringmob3 = mob
        while getgenv().bringmob3 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Boar")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Crab",false,function(mob)
        getgenv().bringmob4 = mob
        while getgenv().bringmob4 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Crab")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    
    page7:Toggle("Bring Demon",false,function(mob)
        getgenv().bringmob5 = mob
        while getgenv().bringmob5 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Cave Demon")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Bob",false,function(mob)
        getgenv().bringmob6 = mob
        while getgenv().bringmob6 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Bob")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Thug",false,function(mob)
        getgenv().bringmob7 = mob
        while getgenv().bringmob7 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Thug")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Gunslingers",false,function(mob)
        getgenv().bringmob8 = mob
        while getgenv().bringmob8 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Gunslinger")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Bruno",false,function(mob)
        getgenv().bringmob9 = mob
        while getgenv().bringmob9 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Bruno")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Bucky",false,function(mob)
        getgenv().bringmob0 = mob
        while getgenv().bringmob0 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Bucky")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Buster",false,function(mob)
        getgenv().bringmob01 = mob
        while getgenv().bringmob01 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Buster")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Gunner",false,function(mob)
        getgenv().bringmob02 = mob
        while getgenv().bringmob02 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Gunner ")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    page7:Toggle("Bring Vokun",false,function(mob)
        getgenv().bringmob03 = mob
        while getgenv().bringmob03 do wait()
    pcall(function()
            for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
                if string.find(v.Name, "Vokun")
                
                  and v:FindFirstChild("HumanoidRootPart") then
                    v:FindFirstChild("HumanoidRootPart").Anchored = true
                    v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
                 end
            end
    end)
    end
    end)
    
    page7:Toggle("Bring All Mob",false,function(mob)
        getgenv().bringmob04 = mob
        while getgenv().bringmob04 do wait()
    pcall(function()
        for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
            if string.find(v.Name, " Boar")
            
              and v:FindFirstChild("HumanoidRootPart") then
                v:FindFirstChild("HumanoidRootPart").Anchored = true
                v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
             end
        end
        
        for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
            if string.find(v.Name, "Angry ")
            
              and v:FindFirstChild("HumanoidRootPart") then
                v:FindFirstChild("HumanoidRootPart").Anchored = true
                v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
             end
        end
        
        for _,v in pairs(game.Workspace.Enemies:GetChildren()) do
            if string.find(v.Name, "Crab") or string.find(v.Name, "Bandit") or string.find(v.Name, "Thief") or string.find(v.Name, "Bruno") or string.find(v.Name, "Bucky") 
              or string.find(v.Name, " Vokun") or string.find(v.Name, "Freddy")  
             or string.find(v.Name, "Cave ") or string.find(v.Name, "Thug") or string.find(v.Name, "Gunslinger") or string.find(v.Name, "Gunner") or string.find(v.Name, "Buster")
              and v:FindFirstChild("HumanoidRootPart") then
                v:FindFirstChild("HumanoidRootPart").Anchored = true
                v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,Distance1)
             end
         end
    end)
    end
    end)
    end
    end
if _G.WhiteListed == false then 
game.Players.LocalPlayer:Kick("KICKED      IRENHUB Notify: Go Buy Script")
end
