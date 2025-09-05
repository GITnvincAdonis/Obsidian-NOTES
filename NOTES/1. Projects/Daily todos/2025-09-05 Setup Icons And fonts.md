---
creation date: <% tp.file.creation_date() %>
---

> [!NOTE] Nerd Fonts are what allow icons to be showed in LAZYVIM
> 

### Step 1.

Download any nerd font. Examples include:

- GeistMonoNerdFont
- FeraNerdFont
  
See [registry](https://www.nerdfonts.com/font-downloads)

### Step 2.

Create local shared font director:
```
mkdir ~/.local/share/fonts
```

### Step 3.

Move downloaded fonts into shared director:
```

mv Downloads/<Font folder>/*<extension, either .ttf or .otf> ~/.local/share/fonts
```

### Step 4.

Configure NVIM Lua to use nerd fonts.

CD into config nvim file
```
nvim ~/.config/nvim/init.lua
```

Edit file to use one of the nerd fonts:
```
require("config.lazy")
vim.g.codeium_render = false
vim.opt.guifont = "<Font name Humanized>:h14"
vim.g.have_nerd_font = true

```

### Step 5. 

Save file and reload NVIM

Link to original: [[2025-09-05 Setup Laptop With Work Environment]]