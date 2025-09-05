---
creation date: <% tp.file.creation_date() %>
---
Install Kitty:
```
sudo apt update
sudo apt install kitty
```

Create a config file in ./config
```
cd ~/.config/kitty
```

Create a kitty.conf:
```
startup_session launch.conf
font_family FantasqueSansM Nerd Font Mono Bold
font_size 14.0
bold_font auto
italic_font auto
bold_italic_font auto

background_opacity 0.9
dynamic_background_opacity 1
confirm_os_window_close 0

# Animated cursor
cursor_trail 100
cursor_trail_decay 0.08 0.2
cursor_trail_start_threshold 2

# change to x11 or wayland or leave auto
linux_display_server auto

scrollback_lines 2000
wheel_scroll_min_lines 1

enable_audio_bell no

window_padding_width 4

selection_foreground none
selection_background none

foreground #dddddd
background #000000
cursor #dddddd

```

Create a launch.conf file to automatically open tmux on launch:
```
launch sh -c "tmux attach -t mysession || tmux new-session -s mysession /bin/zsh"
```


AI chat conversation to help install fonts:
```
https://duckduckgo.com/?q=DuckDuckGo+AI+Chat&ia=chat&duckai=1
```



Link to original: [[2025-05-19]]