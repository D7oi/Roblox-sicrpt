local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "D7oi hub ",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "استنى ثواني و ينفتح",
   LoadingSubtitle = "by D7oi",
   Theme = "Ocean", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"507"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local Tab = Window:CreateTab("خواص قوية", nil) -- Title, Image

local Button = Tab:CreateButton({
   Name = "تعرف من القاتل",
   Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/Ihaveash0rtnamefordiscord/Releases/main/MurderMystery2HighlightESP"))(' Watermelon ?')
   end,
})


local Button = Tab:CreateButton({
   Name = "سكربت ايم بوت",
   Callback = function() 
 loadstring(game:HttpGet("https://raw.githubusercontent.com/ttwizz/Open-Aimbot/refs/heads/master/source.lua"))()

        end,
})

local Button = Tab:CreateButton({
   Name = "ما تموت",
   Callback = function()
  --[[ WARNING: Heads up! This script has not been verified by ScriptBlox. Use at your own risk! ]] loadstring(game:HttpGet("https://freenote.biz/raw/Fhpx5r5A8M"))()
   end,
})

local Tab = Window:CreateTab("خواص جانبية", nil) -- Title, Image

local Slider =Tab:CreateSlider({
   Name = " سرعة",
   Range = {0, 300},
   Increment = 1,
   Suffix = "سرعة",
   CurrentValue = 16,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end, })

local Button = Tab:CreateButton({
   Name = "نطه خارقة",
   Callback = function()
   player=game.Players.LocalPlayer.Character
player.Humanoid.JumpPower = 300
print("Jump Power changed")
   end,
})

local Button = Tab:CreateButton({
   Name = "عشان تلغي الخواص الي في القائمة ذي اضغط ",
   Callback = function()
   
        end,
})