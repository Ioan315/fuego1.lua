local Players = game:GetService("Players")

-- Funktion: fügt einem Charakter eine grüne Umrandung hinzu
local function addOutline(character)
    -- Prüfen ob schon ein Highlight existiert
    if character:FindFirstChild("PlayerOutline") then return end

    local highlight = Instance.new("Highlight")
    highlight.Name = "PlayerOutline"
    highlight.FillTransparency = 1 -- Körper durchsichtig lassen
    highlight.OutlineColor = Color3.fromRGB(0, 255, 0) -- Grün
    highlight.OutlineTransparency = 0 -- Sichtbar
    highlight.Parent = character
end

-- Wenn ein Spieler spawnt, Umrandung hinzufügen
Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function(character)
        addOutline(character)
    end)
end)

-- Falls Spieler schon im Spiel sind
for _, player in pairs(Players:GetPlayers()) do
    if player.Character then
        addOutline(player.Character)
    end
end
