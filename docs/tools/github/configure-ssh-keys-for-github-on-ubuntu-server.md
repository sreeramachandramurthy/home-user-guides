# Configure SSH Keys for GitHub on Ubuntu Server

## Overview

A step by step guide to configure SSH keys for GitHub on Ubuntu server. This completely removes the need for entering usernames, passwords or Personal Access Tokens (PAT's) during `git` operations such as `clone` or `pull` or `push`.

## Steps

### Generate a new SSH Key Pair

* Create a highly secure ED25519 SSH key in the Ubuntu server

```bash
ssh-keygen -t ed25519 -C "Ubuntu Server - GitHub"
```

* Press `Enter` to accept the default file location (`/home/<username>/.ssh/id_ed25519`) or enter the new file location such as `/home/<username>/.ssh/github.com`.
* Press `Enter` twice to leave the passphrase empty. This is recommended for automated server environments, so that it never prompts for a password.

### Add Key to SSH Agent

* Start the SSH Agent

```bash
eval "$(ssh-agent -s)"
```

* Add the Key

```bash
ssh-add ~/.ssh/github.com
```

### Copy Public SSH Key

Open the public version of the key (the file ending in .pub) and copy everything inside it.

```bash
cat ~/.ssh/github.com.pub
```

### Add Public Key to GitHub

1. Log in to GitHub.
2. Click the profile picture in the upper-right corner and select Settings.
3. In the left sidebar, click SSH and GPG keys.
4. Click the green New SSH key button.
5. Give key a descriptive Title (e.g., "Personal Laptop").
6. Leave the Key type as Authentication Key.
7. Paste your copied key into the Key field.
8. Click Add SSH key

### Switch GitHub Repository from HTTPS to SSH

If the server repository was previously set up using HTTPS (asking for tokens), change it's remote target configuration to use SSH.

* Navigate to the repository folder on the server

```bash
cd /workspace/path/to/repo
```

* Update remote URL

```bash
git remote set-url origin git@github.com:<github-username>/repository.git
```

### Test Your Connection

* Test the setup

```bash
ssh -T git@github.com
```

If successful, you will see a warning message followed by:

> Hi username! You've successfully authenticated, but GitHub does not provide shell access.

## References

1. <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent>
2. <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account>
