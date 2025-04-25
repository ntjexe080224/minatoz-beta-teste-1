local Rayfield = loadstring(game:HttpGet('https://[Log in to view URL]'))()

local Window = Rayfield:CreateWindow({
   Name = "minato hub",
   LoadingTitle = "minato hub V1",
   LoadingSubtitle = "by eo ntj",
   ConfigurationSaving = {
      Enabled = false,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Key Huub"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Key | Youtube @eominatoz",
      Subtitle = "Key System",
      Note = "Key In Discord Server",
      FileName = "Youtube:@eominatoz", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = true, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"https://[Log in to view URL]"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }

local MainTab = Window:CreateTab("Home", nil) -- Title, Image
local MainSection = MainTab:CreateSection("Main")

Rayfield:Notify({
   Title = "voce executou o script",
   Content = "bem vindo a o minato hub!",
   Duration = 5,
   Image = nil,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "entendido!",
         Callback = function()
         print("The user tapped entendido!")
      end
   },
            
local Button = MainTab:CreateButton({
   Name = "pulo infinito Toggle",
   Callback = function()
       --Toggles the infinite jump between on or off on every script run
_G.infinjump = not _G.infinjump

if _G.infinJumpStarted == nil then
	--Ensures this only runs once to save resources
	_G.infinJumpStarted = true
	
	--Notifies readiness
	game.StarterGui:SetCore("SendNotification", {Title="Youtube Hub"; Text="Infinite Jump Activated!"; Duration=5;})

	--The actual infinite jump
	local plr = game:GetService('Players').LocalPlayer
	local m = plr:GetMouse()
	m.KeyDown:connect(function(k)
		if _G.infinjump then
			if k:byte() == 32 then
			humanoid = game:GetService'Players'.LocalPlayer.Character:FindFirstChildOfClass('Humanoid')
			humanoid:ChangeState('Jumping')
			wait()
			humanoid:ChangeState('Seated')
			end
		end
	end)
end
   end,
})

local Slider = MainTab:CreateSlider({
   Name = "WalkSpeed Slider",
   Range = {1, 350},
   Increment = 1,
   Suffix = "Speed",
   CurrentValue = 16,
   Flag = "sliderws", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end,
})

local Slider = MainTab:CreateSlider({
   Name = "altura do pulo Slider",
   Range = {1, 350},
   Increment = 1,
   Suffix = "velocidade player",
   CurrentValue = 16,
   Flag = "sliderjp", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = (Value)
   end,
})
local otherTab = Window:CreateTab("Misc", Nil) -- Title, Image
local Section = otherTab:CreateSection("Misc")

local Button = otherTab:CreateButton({
   Name = "Dex Explorer",
   Callback = function()
   --Dark Dex
if game:GetService'CoreGui':FindFirstChild'Dex'then game:GetService'CoreGui'.Dex:Destroy()end;math.randomseed(tick())local a={}for b=48,57 do table.insert(a,string.char(b))end;for b=65,90 do table.insert(a,string.char(b))end;for b=97,122 do table.insert(a,string.char(b))end;function RandomCharacters(c)if c>0 then return RandomCharacters(c-1)..a[math.random(1,#a)]else return''end end;local d=game:GetObjects('rbxassetid://3567096419')[1]d.Name=RandomCharacters(math.random(5,20))d.Parent=game:GetService('CoreGui')local function e(f,g)local function h(i,j)local k={}local l={script=j}local m={}m._index=function(n,o)if l[o]==nil then return getfenv()[o]else return l[o]end end;m._newindex=function(n,o,p)if l[o]==nil then getfenv()[o]=p else l[o]=p end end;setmetatable(k,m)setfenv(i,k)return i end;local function q(j)if j.ClassName=='Script'or j.ClassName=='LocalScript'then spawn(function()h(loadstring(j.Source,'='..j:GetFullName()),j)()end)end;for b,r in pairs(j:GetChildren())do q(r)end end;q(f)end;e(d)
   end,
})

local Button = otherTab:CreateButton({
   Name = "FE Chat Bypass",
   Callback = function()
   loadstring(game:HttpGet("https://[Log in to view URL]"))()
   end,
})

local Button = otherTab:CreateButton({
   Name = "HitBox Expander",
   Callback = function()
   { "FFlagHandleAltEnterFullscreenManually": "False", "FLogNetwork": "7", "DFIntTaskSchedulerTargetFps": "1500", "FFlagFixGraphicsQuality": "True", "FFlagDebugGraphicsPreferD3D11": "True", "DFFlagTextureQualityOverrideEnabled": "True", "DFFlagDisableDPIScale": "True", "FIntRenderShadowIntensity": "0", "DFFlagDebugRenderForceTechnologyVoxel": "True", "FFlagDisablePostFx": "True", "FIntTerrainArraySliceSize": "0", "FIntDebugForceMSAASamples": "1", "FFlagTaskSchedulerLimitTargetFpsTo2402": "False", "FIntUGCValidationLeftArmThresholdBack": "23", "FIntUGCValidationLeftArmThresholdFront": "27", "FIntUGCValidationLeftArmThresholdSide": "40", "FIntUGCValidationLeftLegThresholdBack": "40", "FIntUGCValidationLeftLegThresholdFront": "40", "FIntUGCValidationLeftLegThresholdSide": "36", "FIntUGCValidationRightArmThresholdBack": "46", "FIntUGCValidationRightArmThresholdFront": "50", "FIntUGCValidationRightArmThresholdSide": "80", "FIntUGCValidationRightLegThresholdBack": "80", "FIntUGCValidationRightLegThresholdFront": "80", "FIntUGCValidationRightLegThresholdSide": "76", "FIntUGCValidationTorsoThresholdBack": "200", "FIntUGCValidationTorsoThresholdFront": "200", "FIntUGCValidationTorsoThresholdSide": "200"}
   end,
})

local Button = otherTab:CreateButton({
   Name = "F3X",
   Callback = function()
   loadstring(game:GetObjects("rbxassetid://6695644299")[1].Source)()
   end,
})
