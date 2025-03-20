---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Apparent Issues

1. Issue with container stopping
2. Missing ENV files

> [!Bug] Issues with using ZSH shortcuts
> Path to docker commands not instantiated
> Needed to [[2025-03-18 Setup Plugins in ~.zshrc file]]
 

> [!Success] Fixes
> 

1. Create Env file in repo adding missing credentials:
   
```
cd Documents/code/postgres-pgadmin/  
```

```
nvim .env
```

The credentials to add to the file:
```
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
PGADMIN_DEFAULT_EMAIL=
PGADMIN_DEFAULT_PASSWORD=
PGADMIN_LISTEN_PORT=5050
```
#### refer to sample .env from postgres Docker repository
https://gitlab.com/intellectstorm/teams/backend/postgres-pgadmin

Link to original: [[2025-03-18]]