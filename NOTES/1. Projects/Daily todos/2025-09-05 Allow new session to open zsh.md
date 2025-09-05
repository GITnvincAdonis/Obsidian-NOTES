---
creation date: <% tp.file.creation_date() %>
---
TMUX config is sym-linked to the dotfile configuration [[2025-03-17 DOTFILE configuration]]
A tag is missing to set the default terminal for TMUX sessions and buffers:

```
set -g default-shell /bin/zsh

```

Add the above to the locally stored `tmux.conf` file

Directory:

```
~/.tmux.conf
```


Do not forget to reload configuration:

```
source-file ~/.tmux.conf
```


Link to original: [[2025-09-05 Setup Laptop With Work Environment]]