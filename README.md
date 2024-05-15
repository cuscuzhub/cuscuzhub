local player = game.Players.LocalPlayer
local rs = game:GetService("RunService")

local function farm()
    while true do
        local target = workspace:FindFirstChild("Enemy") -- Change this to the enemy's name
        if target then
            local character = player.Character
            local weapon = character:FindFirstChild("Weapon") -- Change this to your weapon's name
            if weapon then
                weapon:Activate()
                rs.RenderStepped:Wait()
            end
        end
        rs.RenderStepped:Wait()
    end
end

farm()

