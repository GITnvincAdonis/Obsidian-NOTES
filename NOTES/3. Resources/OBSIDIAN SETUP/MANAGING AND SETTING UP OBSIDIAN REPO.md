
> [!Danger] Setup with GITHUB access token
> 


The repository for managing this vault uses credentials divergent from the rest of the system for git. The name and email are different. The push changes, the following are important

```
account name: GITnvincAdonis
password: --SEE BITWARDEN GITHUB NOTES-- (for now. Will expire 90 days from now)

command: git push (should setup lazygit in future to handle repo management)
```

Git has updated their authentication strategy, relying on access tokens. Above is the current effective token. 

Token access and generation is done on the developer token section of github

> [!NOTE] CLAUDE conversation with generating a token
> 
> https://claude.ai/chat/0e0a8a9c-197a-41e6-bf8e-7ab9d39d2192
> ### notes from duck.ai: 
> Personal Access Token (PAT):
> Generate a personal access token on GitHub:
> Go to your GitHub account settings. Navigate to "Developer settings" > "Personal access tokens".
> Click on "Generate new token". Select the scopes or permissions you'd like to grant this token.
> Generate the token and copy it (you won't be able to see it again).
> Use this token in place of your password when prompted during Git operations.
> 
> #### GITHUB URL:
> https://github.com/settings/tokens 





