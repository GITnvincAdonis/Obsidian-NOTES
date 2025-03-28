---
creation date: <% tp.file.creation_date() %>
---

> [!NOTE] Steps for Removing Branches
> #### 1. List all branches in verbose mode
> #### 2. Get all with the term "gone"
> #### 3. Prune remote refs
> #### 4. Delete branches


Command list:
```
git branch --merged | grep -v "\*" | grep -v "main" | xargs git branch -d
git branch -vv | grep "gone" | awk '{print $1}' | xargs -r git branch -D
```
Link to original: [[2025-03-27]]