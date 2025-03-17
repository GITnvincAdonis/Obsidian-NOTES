
> [!Danger] Setup Steps
> 

- Download lazygit on system
```
https://github.com/jesseduffield/lazygit?tab=readme-ov-file#ubuntu
```

### Create plugin file

- Create a plugin file at location '.config/nvim/plugins' for lazygit
- populate file with the following:
  
```
-- nvim v0.8.0
return {
    "kdheepak/lazygit.nvim",
    lazy = true,
    cmd = {
        "LazyGit",
        "LazyGitConfig",
        "LazyGitCurrentFile",
        "LazyGitFilter",
        "LazyGitFilterCurrentFile",
    },
    dependencies = {
        "nvim-lua/plenary.nvim",
    },
    keys = {
        { "<leader>gg", "<cmd>LazyGit<cr>", desc = "LazyGit" }
    }
}
```

### Add a mapping

- add mapping for lazygit to init.lua
  
```
vim.api.nvim_set_keymap('n', '<leader>gg', ':LazyGit<CR>', { noremap = true, silent = true })
```
