<div align="center">

# atlanta reimagined

[![preview](https://media.discordapp.net/attachments/1497579415947706491/1549888494267015229/image.png?ex=6aac55a4&is=6aab0424&hm=bd87588c01cb93554d787a5d6dfaf7c1f6542cf44aaa9f921d4ed9a924d13077&=&format=webp&quality=lossless&width=1024&height=549)](#preview)

**clean · fast · mobile-friendly roblox ui library**

</div>

## Quick Start

```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/cursed-blip/atlanta-reimagined/refs/heads/main/library.lua"))()

local window = library:window({ name = "my script" })
local tab = window:tab({ name = "Combat" })
local section = tab:column():section({ name = "aim" })

section:toggle({
    name = "enabled",
    flag = "aim_enabled",
    callback = function(state) end,
})

section:slider({ name = "smoothness", min = 0, max = 100, default = 40, flag = "smooth" })
section:dropdown({ name = "target", items = { "head", "torso" }, default = "head", flag = "target" })
section:button({ name = "run", callback = function() end })
```

chain pickers and binds onto any toggle:

```lua
section:toggle({ name = "chams", flag = "chams" })
    :colorpicker({ flag = "chams_color", color = Color3.fromHex("#6078BE") })
    :keybind({ flag = "chams_bind" })
```

## API

```
library
├── window
│   └── tab
│       └── column
│           ├── section
│           │   ├── toggle        slider
│           │   ├── dropdown      list
│           │   ├── button        textbox
│           │   ├── label         divider
│           │   └── paragraph
│           └── multi_section → sections
├── toggle → colorpicker · keybind
├── watermark · notification · indicator · playerlist
└── configs: get_config / load_config
```

## Theming

```lua
library:update_theme("accent", Color3.fromHex("#e04848"))
```

`accent` · `outline` · `inline` · `text` · `glow` — one call recolors the whole ui.

---

<div align="center">

*reworked, retuned, reimagined.*

</div>
