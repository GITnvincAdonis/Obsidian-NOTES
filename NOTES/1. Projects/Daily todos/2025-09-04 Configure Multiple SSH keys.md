---
creation date: <% tp.file.creation_date() %>
---

> [!NOTE] Aliases is the key to this
> 

After generating SSH keys and placing them in ~/.ssh/ directory, and `~/.ssh/config` file is required to point specific accounts to the private keys

```
nvim ~/.ssh/config
```

## For Cloning

And enter the following:
```
Host gitlab-work
    HostName gitlab.com
    User git
    IdentityFile ~/.ssh/intellect_storm_key_rsa

Host gitlab-personal  
    HostName gitlab.com
    User git
    IdentityFile ~/.ssh/id_rsa

```

this is just an example of how to structure. The only this that needs to change is the alias and identity file, assuming gitlab is the platform for source control.
When cloning any repo, instead of using the domain gitlab.com, use the alias.

#### #multiple_generated_keys

without alias:


> [!Bug] Will fail
> 
```
git@gitlab.com:intellectstorm/clients/shoponline/shoponline-rails.git
```


> [!Success] Using Alias
> 
```
# the repo only accepts mere requests from authorized users.
# The ssh under the alias is assigned to an authorized gitlab user

git@gitlab-work:intellectstorm/clients/shoponline/shoponline-rails.git
```


## For Servers:

for for sshing into a server:
`ssh -i <path_to_private_key> user@server.example.com`

```
Host myshortname realname.example.com
    HostName realname.example.com
    IdentityFile ~/.ssh/realname_rsa # private key for realname
    User remoteusername

Host myother realname2.example.org
    HostName realname2.example.org
    IdentityFile ~/.ssh/realname2_rsa  # different private key for realname2
    User remoteusername
```

The format then becomes:
`ssh <myshortname | myother>`

See [stackoverflow thread](https://stackoverflow.com/questions/2419566/how-to-configure-multiple-ssh-private-keys-for-different-servers-efficiently)





Link to original: [[2025-09-04]]