local CollectionService = game:GetService("CollectionService")
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local G2L = {}

-- Key correta
local CORRECT_KEY = "PUTAS DE 4"

-- ScreenGui principal
G2L["ScreenGui_1"] = Instance.new("ScreenGui", LocalPlayer:WaitForChild("PlayerGui"))
G2L["ScreenGui_1"].ZIndexBehavior = Enum.ZIndexBehavior.Sibling
CollectionService:AddTag(G2L["ScreenGui_1"], "main")
G2L["ScreenGui_1"].Enabled = true -- deixa visível para digitar a key

-- Frame principal
G2L["Frame_2"] = Instance.new("Frame", G2L["ScreenGui_1"])
G2L["Frame_2"].BorderSizePixel = 0
G2L["Frame_2"].BackgroundColor3 = Color3.fromRGB(0,0,0)
G2L["Frame_2"].Size = UDim2.new(0.32297,0,0.45989,0)
G2L["Frame_2"].Position = UDim2.new(0.32468,0,0.24527,0)

-- Título
G2L["Titulo_3"] = Instance.new("TextLabel", G2L["Frame_2"])
G2L["Titulo_3"].TextWrapped = true
G2L["Titulo_3"].TextScaled = true
G2L["Titulo_3"].BackgroundTransparency = 1
G2L["Titulo_3"].TextColor3 = Color3.fromRGB(255,255,255)
G2L["Titulo_3"].Text = "Sistema de key (Nome do seu script)"
G2L["Titulo_3"].Position = UDim2.new(-0.04762,0,0.1,0)
G2L["Titulo_3"].Size = UDim2.new(1.07407,0,0.325,0)
G2L["Titulo_3"].FontFace = Font.new([[rbxasset://fonts/families/FredokaOne.json]])

-- UICorner
Instance.new("UICorner", G2L["Frame_2"])

-- UIStroke
local stroke = Instance.new("UIStroke", G2L["Frame_2"])
stroke.Thickness = 2
stroke.Color = Color3.fromRGB(10,200,255)

-- UIAspectRatio
local aspect = Instance.new("UIAspectRatioConstraint", G2L["Frame_2"])
aspect.AspectRatio = 1.575

-- Texto: Key no Discord
G2L["TextLabel_7"] = Instance.new("TextLabel", G2L["Frame_2"])
G2L["TextLabel_7"].TextWrapped = true
G2L["TextLabel_7"].TextScaled = true
G2L["TextLabel_7"].BackgroundTransparency = 1
G2L["TextLabel_7"].TextColor3 = Color3.fromRGB(255,252,252)
G2L["TextLabel_7"].Text = "Key no nosso discord"
G2L["TextLabel_7"].Position = UDim2.new(0.08466,0,0.63333,0)
G2L["TextLabel_7"].Size = UDim2.new(0.79365,0,0.09167,0)
G2L["TextLabel_7"].FontFace = Font.new([[rbxasset://fonts/families/FredokaOne.json]])

-- Botão copiar link Discord
G2L["ColocarLinkDaKeyDiscord_8"] = Instance.new("TextButton", G2L["Frame_2"])
G2L["ColocarLinkDaKeyDiscord_8"].TextWrapped = true
G2L["ColocarLinkDaKeyDiscord_8"].TextScaled = true
G2L["ColocarLinkDaKeyDiscord_8"].TextColor3 = Color3.fromRGB(255,255,255)
G2L["ColocarLinkDaKeyDiscord_8"].BackgroundColor3 = Color3.fromRGB(40,106,255)
G2L["ColocarLinkDaKeyDiscord_8"].Text = "Copiar Link da key (Discord) https://discord.gg/62Mu6CkQ🔗"
G2L["ColocarLinkDaKeyDiscord_8"].Position = UDim2.new(0.12169,0,0.75833,0)
G2L["ColocarLinkDaKeyDiscord_8"].Size = UDim2.new(0.60847,0,0.175,0)
Instance.new("UICorner", G2L["ColocarLinkDaKeyDiscord_8"])

-- Botão enviar key
G2L["ClicarParaEnviarKey_a"] = Instance.new("TextButton", G2L["Frame_2"])
G2L["ClicarParaEnviarKey_a"].TextWrapped = true
G2L["ClicarParaEnviarKey_a"].TextSize = 20
G2L["ClicarParaEnviarKey_a"].BackgroundColor3 = Color3.fromRGB(81,81,81)
G2L["ClicarParaEnviarKey_a"].Text = "▶️"
G2L["ClicarParaEnviarKey_a"].Position = UDim2.new(0.77249,0,0.75833,0)
G2L["ClicarParaEnviarKey_a"].Size = UDim2.new(0.16402,0,0.16667,0)
Instance.new("UICorner", G2L["ClicarParaEnviarKey_a"])

-- Caixa de digitar a key
G2L["PutKey_c"] = Instance.new("TextBox", G2L["Frame_2"])
G2L["PutKey_c"].CursorPosition = -1
G2L["PutKey_c"].TextWrapped = true
G2L["PutKey_c"].TextScaled = true
G2L["PutKey_c"].BackgroundColor3 = Color3.fromRGB(255,255,255)
G2L["PutKey_c"].Size = UDim2.new(0.73016,0,0.16667,0)
G2L["PutKey_c"].Position = UDim2.new(0.12698,0,0.45,0)
Instance.new("UICorner", G2L["PutKey_c"])

-- BOTÕES
local keyBox = G2L["PutKey_c"]
local sendButton = G2L["ClicarParaEnviarKey_a"]
local discordButton = G2L["ColocarLinkDaKeyDiscord_8"]
local screenGui = G2L["ScreenGui_1"]

-- Clicar para enviar key
sendButton.MouseButton1Click:Connect(function()
    local playerKey = keyBox.Text
    if playerKey == CORRECT_KEY then

-- colar gui e sistemas aqui!!
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")

local screenGui = Instance.new("ScreenGui")
screenGui.Name = "AshFreeGui"
screenGui.ResetOnSpawn = false
screenGui.Parent = playerGui

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 200, 0, 120)
frame.Position = UDim2.new(0, 20, 0.5, -60)
frame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
frame.BorderSizePixel = 3
frame.Parent = screenGui

local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 30)
title.BackgroundTransparency = 1
title.Text = "Desenvolvedor JJ"
title.TextColor3 = Color3.new(1,1,1)
title.Font = Enum.Font.SourceSansBold
title.TextSize = 23
title.Parent = frame 


local pullBtn = Instance.new("TextButton")
pullBtn.Size = UDim2.new(1, -20, 0, 40)
pullBtn.Position = UDim2.new(0, 10, 0, 40)
pullBtn.Text = "Gerar armas(10)"
pullBtn.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
pullBtn.TextColor3 = Color3.new(1,1,1)
pullBtn.Font = Enum.Font.SourceSansBold
pullBtn.TextSize = 22
pullBtn.Parent = frame
pullBtn.Text = "Gerar armas(10)"

local toggleBtn = Instance.new("TextButton")
toggleBtn.Size = UDim2.new(0, 100, 0, 30)
toggleBtn.Position = UDim2.new(0, 10, 1, 10)
toggleBtn.Text = "Ocultar"
toggleBtn.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
toggleBtn.TextColor3 = Color3.new(1,1,1)
toggleBtn.Font = Enum.Font.SourceSans
toggleBtn.TextSize = 15
toggleBtn.Parent = frame

-- Armas já puxadas (pra evitar duplicatas)
local armasPuxadas = {}

pullBtn.MouseButton1Click:Connect(function()
    local puxadas = 0
    local fontes = {
        game:GetService("Workspace"),
        game:GetService("ReplicatedStorage"),
        game:GetService("StarterPack"),
        game:GetService("StarterGear")
    }

    for _, fonte in ipairs(fontes) do
        for _, obj in ipairs(fonte:GetDescendants()) do
            if obj:IsA("Tool") and not armasPuxadas[obj.Name] then
                local temScript = false
                for _, filho in ipairs(obj:GetDescendants()) do
                    if filho:IsA("Script") or filho:IsA("LocalScript") then
                        temScript = true
                        break
                    end
                end

                if temScript then
                    pcall(function()
                        obj.Parent = player.Backpack
                        armasPuxadas[obj.Name] = true
                        puxadas += 1
                    end)
                end

                if puxadas >= 10 then
                    break
                end
            end
        end
        if puxadas >= 10 then
            break
        end
    end

    game.StarterGui:SetCore("SendNotification", {
        Title = "JJ",
        Text = "Foram puxadas " .. puxadas .. " novas armas.",
        Duration = 4,
    })
end)

local menuVisible = true
toggleBtn.MouseButton1Click:Connect(function()
    menuVisible = not menuVisible
    frame.Visible = menuVisible
    toggleBtn.Text = menuVisible and "Esconder Menu" or "Mostrar Menu"
end)
-- Colar o script sempre acima disso 🔼
        
        print("Key correta! Abrindo seu Hub...")
        screenGui:Destroy() -- destrói a tela da key, opcional
    else
        keyBox.BackgroundColor3 = Color3.fromRGB(255,0,0)
        print("Key incorreta ❌")
    end
end)

-- Botão copiar link Discord
discordButton.MouseButton1Click:Connect(function()
    setclipboard("https://discord.gg/nSVkmuq65")
    print("Link copiado para o clipboard 🔗")
end)

return G2L["ScreenGui_1"], require

