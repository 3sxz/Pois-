--- Script ESP simples
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local RunService = game:GetService("RunService")

-- Função para criar um ESP para um jogador
local function createESP(player)
    if player == LocalPlayer then return end -- Ignorar o próprio jogador
    player.CharacterAdded:Connect(function(character)
        local highlight = Instance.new("Highlight")
        highlight.Parent = character
        highlight.Adornee = character
        highlight.FillColor = Color3.fromRGB(255, 0, 0) -- Cor do ESP (vermelho)
        highlight.FillTransparency = 0.5
        highlight.OutlineTransparency = 0
    end)

    -- Caso o jogador já tenha um personagem ao entrar
    if player.Character then
        local highlight = Instance.new("Highlight")
        highlight.Parent = player.Character
        highlight.Adornee = player.Character
        highlight.FillColor = Color3.fromRGB(255, 0, 0) -- Cor do ESP (vermelho)
        highlight.FillTransparency = 0.5
        highlight.OutlineTransparency = 0
    end
end

-- Adicionar ESP para todos os jogadores no jogo
for _, player in ipairs(Players:GetPlayers()) do
    createESP(player)
end

-- Adicionar ESP para novos jogadores que entrarem no jogo
Players.PlayerAdded:Connect(function(player)
    createESP(player)
end)
