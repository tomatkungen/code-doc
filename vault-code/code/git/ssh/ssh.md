```shell
# Generate ssh key press enter or name the file
# ssh-keygen -t ed25519 -C <email>
$ ssh-keygen -t ed25519 -C "my@hotmail.com"

# create id_my, id_my.pub 
```

```shell
# Add ssh to ssh-agent
$ eval "$(ssh-agent -s)" # agent pid <number>

# alternative if it not working 
# exec ssh-agent bash
# exec ssh-agent zsh

# Open ssh config
$ open ~/.ssh/config

# if not exist
$ mkdir .ssh
$ touch ~/.ssh/config

# open config and paste and use private key file
# If you chose not to add a passphrase to your key, you should omit
# the `UseKeychain` line.
Host github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_my

# Add private key to ssh-agent 
$ ssh-add ~/.ssh/id_rsa

# alternative
$ ssh-add --apple-use-keychain ~/.ssh/id_rsa
```

```shell
# add public ssh key to github

1. Copy the SSH public key to your clipboard.
2. In the upper-right corner of any page on GitHub, click your profile photo, then click **Settings**
3. In the "Access" section of the sidebar, click  **SSH and GPG keys**.
4. Click **New SSH key** or **Add SSH key**.
5. In the "Title" field, add a descriptive label for the new key. For example, if youre using a personal laptop, you might call this key "Personal laptop".    
6. Select the type of key, either authentication or signing. For more information about commit signing, see "[About commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)."
7. In the "Key" field, paste your public key.   
8. Click **Add SSH key**.
```

```shell
# how to test ssh auth and type yes to verify fingerprint
$ ssh -T git@github.com
```

```shell
# Goto repository and push code if clone by https add ssh orgin instead
# git remote set-url origin git@github.com:username/your-repository.git
$ git remote set-url origin git@github.com:tomatkungen/code-doc.git
```