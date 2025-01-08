local player = game.Players.LocalPlayer
local playerGuis = player.PlayerGui

-- elements
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UiStroke1 = Instance.new("UIStroke")
local ScrollingFrame = Instance.new("ScrollingFrame")
local UIListLayout = Instance.new("UIListLayout")
local Template = Instance.new("Frame")
local ImageLabel = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local UIStroke2 = Instance.new("UIStroke")
local Btn = Instance.new("TextButton")
local UpdateBtn = Instance.new("TextButton")

-- gui display
local parentDisplay = game.Workspace:GetChildren()

local images = {
	
	["Folder"] = "rbxassetid://134334860697754",
	["Part"] = "rbxassetid://132789312457391",
	["Model"] = "rbxassetid://138150444410658",
	["MeshPart"] = "rbxassetid://133335931844855",
	["ModuleScript"] = "rbxassetid://127069814934274",
	["Script"] = "rbxassetid://110870106211419",
	["LocalScript"] = "rbxassetid://98603956044137",
	["Terrain"] = "rbxassetid://111465305837551",
	["ParticleEmitter"] = "rbxassetid://75061415502013",
	["SpawnLocation"] = "rbxassetid://108303211351018",
	["Camera"] = "rbxassetid://99930768307465",

	
}

local function sla()
	
	for i, item in pairs(parentDisplay) do

		local aa = Template:Clone()
		aa.TextLabel.Text = item.Name
		aa.ImageLabel.Image = images[item.ClassName] or "rbxassetid://102217065937388"

		aa.Visible = true
		aa.Parent = ScrollingFrame

	end
	
end

local function cavalo()
	
	for i, item in pairs(playerGuis:GetChildren()) do
		
		if item.Name == "CustomWorkspace" and item:IsA("ScreenGui") then
			
			item:Destroy()
			
		end
		
	end

	-- screenGui
	ScreenGui.Name = "CustomWorkspace"
	ScreenGui.DisplayOrder = 999999999
	ScreenGui.Parent = playerGuis
	
	-- frame
	Frame.Name = "Frame"
	Frame.AnchorPoint = Vector2.new(0.5, 0.5)
	Frame.Position = UDim2.new(0.875, 0, 0.5, 0)
	Frame.Size = UDim2.new(0.2, 0, 0.9, 0)
	Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Frame.Parent = ScreenGui

	-- textButton
	Btn.Name = "Btn"
	Btn.Position = UDim2.new(0.01, 0, 0.25, 0)
	Btn.Size = UDim2.new(0.055, 0, 0.1, 0)
	Btn.BackgroundColor3 = Color3.fromRGB(125, 125, 125)
	Btn.Text = "Close"
	Btn.TextColor3 = Color3.fromRGB(255, 255, 255)
	Btn.Font = Enum.Font.FredokaOne
	Btn.TextWrapped = true
	Btn.TextScaled = true
	Btn.Parent = ScreenGui

	-- uiStroke1
	UiStroke1.Thickness = 5
	UiStroke1.Color = Color3.fromRGB(0, 0, 0)
	UiStroke1.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
	UiStroke1.LineJoinMode = Enum.LineJoinMode.Miter
	UiStroke1.Parent = Frame
	
	-- scrollingFrame
	ScrollingFrame.AnchorPoint = Vector2.new(0.5, 0.5)
	ScrollingFrame.BackgroundColor3 = Color3.fromRGB(175, 175, 175)
	ScrollingFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
	ScrollingFrame.Size = UDim2.new(0.94, 0, 0.98, 0)
	ScrollingFrame.AutomaticCanvasSize = Enum.AutomaticSize.XY
	ScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
	ScrollingFrame.ScrollBarThickness = 0
	ScrollingFrame.Parent = Frame
	
	-- updateBtn
	UpdateBtn.Name = "UpdateBtn"
	UpdateBtn.Position = UDim2.new(-0.525, 0, 0, 0)
	UpdateBtn.Size = UDim2.new(0.5, 0, 0.075, 0)
	UpdateBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
	UpdateBtn.Font = Enum.Font.FredokaOne
	UpdateBtn.TextScaled = true
	UpdateBtn.Text = "Update"
	UpdateBtn.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
	UpdateBtn.Parent = Frame
	
	-- uiListLayout
	UIListLayout.Padding = UDim.new(0, 10)
	UIListLayout.FillDirection = Enum.FillDirection.Vertical
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
	UIListLayout.Parent = ScrollingFrame
	
	-- template
	Template.Name = "Template"
	Template.BackgroundColor3 = Color3.fromRGB(150, 150, 150)
	Template.Size = UDim2.new(1, 0, 0.075, 0)
	Template.Visible = false
	Template.Parent = ScrollingFrame
	
	-- imageLabel
	ImageLabel.Name = "ImageLabel"
	ImageLabel.BackgroundTransparency = 1
	ImageLabel.Size = UDim2.new(0.2, 0, 1, 0)
	ImageLabel.Parent = Template
	
	-- textLabel
	TextLabel.BackgroundTransparency = 1
	TextLabel.Position = UDim2.new(0.225, 0, 0, 0)
	TextLabel.Size = UDim2.new(0.775, 0, 1, 0)
	TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.Font = Enum.Font.FredokaOne
	TextLabel.Text = ""
	TextLabel.TextScaled = true
	TextLabel.TextWrapped = true
	TextLabel.Parent = Template
	
	-- uiStroke2
	UiStroke1.Thickness = 5
	UiStroke1.Color = Color3.fromRGB(0, 0, 0)
	UiStroke1.ApplyStrokeMode = Enum.ApplyStrokeMode.Contextual
	UiStroke1.LineJoinMode = Enum.LineJoinMode.Miter
	UiStroke1.Parent = TextLabel
	
	sla()
	
	Btn.MouseButton1Click:Connect(function()
		
		Frame.Visible = not Frame.Visible
		
		if Frame.Visible == true then
			
			Btn.Text = "Close"
			
		else
			
			Btn.Text = "Open"
			
		end
		
	end)
	
	UpdateBtn.MouseButton1Click:Connect(function()
		
		for i, previous in pairs(ScrollingFrame:GetChildren()) do
			
			if previous ~= Template and previous ~= UIListLayout then
				
				previous:Destroy()
				
			end
			
		end
		
		sla()
		
	end)
	
end

cavalo()
