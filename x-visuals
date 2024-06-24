-- Define global variables for settings
local bloomEnabled = true
local bloomIntensity = 0.5

-- Function to toggle bloom effect
function toggleBloom()
    if bloomEnabled then
        -- Disable bloom
        set("sim/private/controls/bloom/enable", 0)
        bloomEnabled = false
    else
        -- Enable bloom
        set("sim/private/controls/bloom/enable", 1)
        bloomEnabled = true
    end
end

-- Function to adjust bloom intensity
function setBloomIntensity(value)
    set("sim/private/controls/bloom/intensity", value)
    bloomIntensity = value
end

-- Create UI elements
create_command("Custom/ToggleBloom", "Toggle Bloom Effect", "toggleBloom()", "")
create_command("Custom/SetBloomIntensity", "Set Bloom Intensity", "setBloomIntensity(%f)", bloomIntensity, 0.1)

-- Register UI controls
add_macro("Bloom Settings", "toggleBloom()", "toggleBloom()")
add_slider("Bloom Intensity", "setBloomIntensity", 0.1, 2.0, 0.1, "Bloom Intensity")

-- Initial setup
if bloomEnabled then
    set("sim/private/controls/bloom/enable", 1)
else
    set("sim/private/controls/bloom/enable", 0)
end
set("sim/private/controls/bloom/intensity", bloomIntensity)
