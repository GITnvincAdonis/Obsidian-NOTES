---
creation date: <% tp.file.creation_date() %>
---
## Install

```
curl https://mise.run | sh
```

Hook mise into your shell (pick the right one for your shell):

```shell
echo 'eval "$(~/.local/bin/mise activate bash)"' >> ~/.bashrc
echo 'eval "$(~/.local/bin/mise activate zsh)"' >> ~/.zshrc
```

Dont Forget to reload ZSH config:

```
source ~/.zshrc
```

To ensure correct setup, run:

```
mise doctor
```


> [!NOTE] Resources
> - https://github.com/jdx/mise?tab=readme-ov-file#quickstart


Link to original: [[2025-03-17 Setup Dev Environment]]