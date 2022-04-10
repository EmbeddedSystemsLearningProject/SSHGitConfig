# SSHGitConfig

How to set ssh with github to avoid password usage:

First execute the next commands on your terminal and use the e-mail linked to your GitHub account

```sh
ssh-keygen -t ed25519 -C user@email.com
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

Get the public key with the next command

```sh
cat ~/.ssh/id_ed25519.pub
```

Copy the stdout (output) of the last command and paste it on your GitHub account configuration, in "SSH and GPG" keys option
![capture](images/sshGitHubConfig.png)
