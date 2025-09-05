---
creation date: <% tp.file.creation_date() %>
---

Commands to Install;
```
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | grep -Po '"tag_name": "v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/latest/download/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit /usr/local/bin
rm lazygit.tar.gz lazygit
```

Make Lazygit folders:
```
mkdir -p ~/.config/lazygit
touch ~/.config/lazygit/config.yml
```


Link to original: [[2025-09-05 Setup Laptop With Work Environment]]