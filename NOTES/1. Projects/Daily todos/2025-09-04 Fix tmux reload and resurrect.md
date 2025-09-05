---
creation date: <% tp.file.creation_date() %>
---

> [!Bug] The Dotfile does not provide explicit Bindings
> 

In the dotfile, paste the following:
```
# Explicit tmux-resurrect key bindings
bind-key C-s run-shell '~/.tmux/plugins/tmux-resurrect/scripts/save.sh'
bind-key C-r run-shell '~/.tmux/plugins/tmux-resurrect/scripts/restore.sh'
```


Also ensure that a tmux resurrection directory exists:

```
ls -la ~/.tmux/resurrect/
```

If empty, create:
```
mkdir -p ~/.tmux/resurrect
```


Attempt to save and restore now

Reference [claude chat](https://claude.ai/chat/e588aa80-7c1f-4979-8a14-8f18367e8db9) for help

Link to original: [[2025-09-04]]