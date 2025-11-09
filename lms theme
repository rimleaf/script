local themes = workspace.Themes
local supportedThemes = {
	-- last man standing - standart
	["rbxassetid://71057332615441"] = "A GRAVE SOUL (NOW, RUN)",
	["rbxassetid://115884097233860"] = "CREATION OF HATRED",
	["rbxassetid://80564889711353"] = "PLEAD",
	
	-- last man standing - skins
	["rbxassetid://134062685653533"] = "Through Patches of Violet",
	["rbxassetid://137266220091579"] = "Vanity Slasher",
	["rbxassetid://90022574613230"] = "CLOSE TO ME",
	["rbxassetid://130101085745481"] = "BURNOUT",
	["rbxassetid://127298326178102"] = "COMPASS",
	["rbxassetid://122146196733152"] = "SMILE",

	-- skin chase themes
	-- soon! :3

	-- non skin related stuff
	["rbxassetid://113613352374472"] = "DAMNATION (Lobby Theme)"
}

if themes and not _G.Connection then
	print("[OST REPLACE | Info] To change a theme, add an .mp3 file to your workspace with the exact same name as the original track.")
print("[OST REPLACE | Example] For instance, to replace \"A GRAVE SOUL (NOW, RUN)\", just add an .mp3 file titled exactly the same.")

	print("[OST REPLACE | Status] Running! To stop the script, run it again.")
	_G.Connection = themes.ChildAdded:Connect(function(child)
		if child.SoundId ~= nil then
			local name = supportedThemes[child.SoundId]
			if name then
				local fileMP3 = isfile(name ..".mp3", "exists")
				print("[OST REPLACE | SUPPORTED] CURRENTLY PLAYING: ".. name)

				if fileMP3 then
					print("[OST REPLACE | REPLACED] Replacing with custom song..")
					child.SoundId = getcustomasset(name ..".mp3", false)
				end
			end
		end
	end)
else
	print("[OST REPLACE | Status] Stopped!")
	_G.Connection:Disconnect()
	_G.Connection = nil
end
