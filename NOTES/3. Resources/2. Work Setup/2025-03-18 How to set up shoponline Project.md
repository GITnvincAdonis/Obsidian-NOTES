---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Steps
> 

> [!Danger] Note
> Just be vigilant to restart server when issues arise. it tends to be the fix

### 1. Ensure all prerequisites are set up
Inclusive of rails, ruby, mise, postgres container, nvim and so and so forth [[2025-03-17 Setup Dev Environment]]

### 2. Clone repository from gitlab using [[SETTING UP SSH keys| SSH key]]
```
git clone git@gitlab.com:intellectstorm/clients/shoponline/shoponline-rails.git
```

### 3. Install all dependencies
```
mise i
bundle
```

### 4. Create .env file with correct credentials
```
POSTGRES_PASSWORD=password
GOOGLE_CLIENT_ID=907069055045-ve53c2jk7dn2bdofc2t5do509da44k19.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=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

```

Link to original: [[2025-03-18]]