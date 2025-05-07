## Roblox Pixel Shader – Custom Raytraced Screen Effect

A lightweight **real-time screen shader** for Roblox that mimics **basic raytraced lighting, reflections, and shadows** using 2D UI frames and `Raycast` math. No plugins, no modules – just one neat LocalScript.

![Demo]() 

---

##  Features

-  Simulated **raycasting per pixel**
-  Directional sun lighting with soft shadows

- **Reflective surfaces** (metal/glass style)
-  Adjustable **resolution scaling**
- Runs in a single **LocalScript** with UI Frames

---

## How to Use

1. Create a **LocalScript** inside:
2. Paste in the full script from `senti_pixel_shader.lua`
3. Hit **Play** in Roblox Studio and watch the shader draw!
## REMEMBER TO CREATE A BLANK SCREENGUI IN STARTERGUI   ![image](https://github.com/user-attachments/assets/56d53595-20b8-4115-86a1-722c03682cd3)

---

##  How It Works

Each frame:

- A 2D **grid of UI frames** covers the screen (e.g. 40x30 resolution)
- Each frame casts a `Ray` from the **Camera's position**
- If the ray hits something, we:
- Get surface **normal** and color
- Check **shadow occlusion** toward the sun
- Apply **ambient lighting** and simple **reflection logic**
- The pixel color is set via `.BackgroundColor3`

It's like building a raytraced render engine with colored squares!

---

##  Settings

You can tweak these inside the script:

```lua
local pixelSize = 8           -- Size of each square
local resolutionX = 160       -- Horizontal pixels
local resolutionY = 90        -- Vertical pixels
local renderDistance = 500    -- Max raycast distance
