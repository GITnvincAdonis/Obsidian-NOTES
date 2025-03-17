
> [!Question] Why?
> Pushing any information to a repository from a local branch requires authentication. Setting up an SSH keys allows GITHUB or GITLAB to trust your system, foregoing continuous password and user checks.  SSH keys simply allow for faster interactions with GIT hosting applications 


> [!Danger] Steps for setting up
> 

- Generate a key in the terminal of any type e.g. rsa https://docs.gitlab.com/user/ssh/
- Retrieve ssh key from saved location https://docs.gitlab.com/user/ssh/#add-an-ssh-key-to-your-gitlab-account
- In GITLAB or whatever git application, navigate to the SSH keys tab in setting. FOR GITLAB: https://gitlab.com/-/user_settings/ssh_keys
