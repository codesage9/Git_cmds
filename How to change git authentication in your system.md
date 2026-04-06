# How to change git authentication in your system

## I created new git account and logged in, in my system with that 
but since i want to use my main account in the git to push in the main account repo
i was denied the permission since other account was not permitted to make any changes in repo

so here is how to change the authentication 

⭐⭐⭐⭐⭐
## 🔄 Option 1: Switch HTTPS credentials
If you cloned with HTTPS (https://github.com/...):

Clear old credentials

## - On Windows: open Credential Manager → Windows Credentials.

Find entries like git:https://github.com and delete them.

## 2. Push again

## Run:

### bash
    - git push origin main

Git will prompt you to log in. Enter the username/password (or personal access token) for the correct GitHub account (codesage9).


## 🔑 Option 2: Use SSH keys (recommended for multiple accounts)
Generate a new SSH key for the account you want:

### bash
    ssh-keygen -t ed25519 -C "your_email@example.com"
Save it as something like id_ed25519_codesage9.

Add the public key (id_ed25519_codesage9.pub) to GitHub → Settings → SSH and GPG keys.

Configure SSH (~/.ssh/config):

## Code
    Host github-codesage9
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_codesage9
Update your repo remote:

### bash
    git remote set-url origin git@github-codesage9:codesage9/Git_cmds.git
Now Git will use the correct key/account when pushing.