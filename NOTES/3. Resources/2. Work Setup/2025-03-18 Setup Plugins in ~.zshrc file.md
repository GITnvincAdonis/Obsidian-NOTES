---
creation date: <% tp.file.creation_date() %>
---

> [!Question] Why?
> 

the config file for zsh doesn't automatically allow for shorthand commands. For each class of commands, its corresponding plugin needs to be added to the config file. It can be exited using the following command:

```
nvim ~/.zshrc
```


> [!Important] Add a plugin
> plugins=(....)
> This specific line, withing the parenthesis to be exact, is where all plugins are managed.
> A plugin such as rails, needs to be added within this parenthesis, allowing zsh to access all of its commands.
> The update zshrc file will have:
> ```
> plugins=(rails git mise) 
> ```



Link to original: [[2025-03-18 Fix Postgres Error for postgres container]]