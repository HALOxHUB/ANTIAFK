--hi
local anti = Instance.new("ScreenGui")
local Gradient = Instance.new("Frame")
local UIGradient = Instance.new("UIGradient")
local UICorner = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")

anti.Name = "anti"
anti.Parent = game.CoreGui

Gradient.Name = "Gradient"
Gradient.Parent = anti
Gradient.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Gradient.BackgroundTransparency = 0.500
Gradient.BorderColor3 = Color3.fromRGB(27, 42, 53)
Gradient.BorderSizePixel = 0
Gradient.Position = UDim2.new(0.445330292, 0, -0.0084951371, 0)
Gradient.Size = UDim2.new(0, 144, 0, 36)

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(203, 215, 253)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(225, 226, 227))}
UIGradient.Parent = Gradient

UICorner.CornerRadius = UDim.new(0, 7)
UICorner.Parent = Gradient

TextLabel.Parent = Gradient
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0, 0, 0.249999985, 0)
TextLabel.Size = UDim2.new(0, 144, 0, 23)
TextLabel.Font = Enum.Font.PatrickHand
TextLabel.Text = "HALOxHUB ANTI AFK ON!"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 22.000
TextLabel.TextStrokeTransparency = 0.000

local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
   vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
   wait(1)
   vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
