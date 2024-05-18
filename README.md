print("running")
local ArrayField = loadstring(game:HttpGet("https://raw.githubusercontent.com/Hosvile/Refinement/main/MC%3AArrayfield%20Library"))()
local Window = ArrayField:CreateWindow({
   Name = "Kapi V1",
   LoadingTitle = "Kapi have released in 14/05/24",
   LoadingSubtitle = "by kaper715",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "ArrayField"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Kapi",
      Subtitle = "Key System",
      Note = "The Key System of kapi its very fast",
      FileName = "Key", -- It is recommended to use something unique as other scripts using ArrayField may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = true, -- If this is true, set Key below to the RAW site you would like ArrayField to get the key from
      Actions = {
            [1] = {
                Text = 'Click here to copy key system',
                OnPress = function()      setclipboard("https://sites.google.com/view/keysystemkapi/início") --This Will Copy The Link Of The Key
                    print('Pressed')
                end,
                }
            },
      Key = {"https://pastebin.com/raw/TrEs6GD6"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local Tab = Window:CreateTab("Hitbox", 4483362458) -- Title, Image

local Button = Tab:CreateButton({
   Name = "Start Hitbox",
   Interact = 'Click',
   Callback = function()          _G.Size = 5
              _G.Fov = 70
_G.CanCollide = false

while wait(0.1) do
    local Players = game:GetService("Players")
    local all = Players:GetPlayers()
    local Lp = Players.LocalPlayer
    
    for _, player in ipairs(all) do
       if Lp ~= player and player.Character then
          local ht  = player.Character:FindFirstChild("HumanoidRootPart")
          if ht then
            local hum = player.Character:FindFirstChild("Humanoid")
            if hum then
            if hum.Health == 0 then
             ht.Size = Vector3.new(0, 0, 0)
            else
                print("Aimbot Op")
             hum.WalkSpeed = _G.Speed
             ht.Size = Vector3.new(_G.Size, _G.Size, _G.Size)
             ht.Transparency = _G.Transparency
			 ht.CanCollide = _G.CanCollide
             game.Workspace.Camera.FieldOfView = _G.Fov
          end
         end
       end
    end
    end
    end

   -- The function that takes place when the button is pressed
   end,
})

local Section = Tab:CreateSection("Settings",false) -- The 2nd argument is to tell if its only a Title and doesnt contain element

local Button = Tab:CreateButton({
   Name = "Normal Hitbox",
   Interact = 'Click', 
   Callback = function()              _G.Size = 10
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Big Hitbox",
   Interact = 'Click',
   Callback = function()       _G.Size = 20
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Kitsune and T-rex Hitbox",
   Interact = 'Click',
   Callback = function()       _G.Size = 40
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Buddha HitBox",
   Interact = 'Click',
   Callback = function()        _G.Size = 60
   -- The function that takes place when the button is pressed
   end,
})

local Section = Tab:CreateSection("Transparent",false) -- The 2nd argument is to tell if its only a Title and doesnt contain element

local Button = Tab:CreateButton({
   Name = "Transparent 0%",
   Interact = 'Click',
   Callback = function()           _G.Transparency = 0
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Transparent 0.25%",
   Interact = 'Click',
   Callback = function()            _G.Transparency = 0.25
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Transparent 0.5%",
   Interact = 'Click',
   Callback = function()            _G.Transparency = 0.5
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Tranparent 0.75",
   Interact = 'Click',
   Callback = function()                  _G.Transparency = 0.75
   -- The function that takes place when the button is pressed
   end,
})

local Button = Tab:CreateButton({
   Name = "Transparent 1%",
   Interact = 'Click',
   Callback = function()          _G.Transparency = 1
   -- The function that takes place when the button is pressed
   end,
})
