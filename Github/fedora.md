# (´∀｀) Git & GitHub on Fedora — Full Beginner Guide

Welcome to the special GitHub class of **Dango** (´∀｀)♡  
This guide will help you set up Git, create your first repository, and push code to GitHub directly from Fedora Linux.

---
## Don't be scared!

If you are lost or new to Git and GitHub, don't worry! This guide is made for absolute beginners.  
Follow each step carefully, and you'll be pushing code in no time (｀・ω・´)ゞ

If you are confused about any command or step, feel free to look it up online or ask for help.
You can also check out my [Linux Beginner Cheat Sheet](../Linux/CheatSheet.md) for useful commands.

GOOD LUCK!

---

## 1. Prerequisites

Before starting, make sure your Fedora system is up to date and has the required tools installed.

```bash
sudo dnf upgrade --refresh -y
```

### Install Git
```bash
sudo dnf install git -y
```

### Install OpenSSH
(Used to connect securely to GitHub.)
```bash
sudo dnf install openssh-clients -y
```

---

## 2. Create a GitHub Account

1. Go to [https://github.com](https://github.com)
2. Click **Sign up**
3. Choose:
   - A **username**
   - Your **email address**
   - A **password**
4. Confirm your email and log in.

---

## 3. Create a New Repository

1. Click the **+** icon (top right) → **New repository**
2. Fill in:
   - **Repository name** (e.g., `my-first-repo`)
   - Description (optional)
   - Choose **Public** or **Private**
3. Click **Create repository**
4. Copy the SSH URL (it looks like `git@github.com:username/my-first-repo.git`)

---

## 4. Create and Add an SSH Key

### Generate a new SSH key

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

If your system does not support `ed25519`, use RSA:
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

Press **Enter** to accept the default path and optionally add a passphrase.
*I recommend not using a passphrase for simplicity, but it's more secure with one.*

### Copy the public key

```bash
cat ~/.ssh/id_ed25519.pub
```

### Add the key to GitHub

1. Go to **GitHub → Settings → SSH and GPG keys**
2. Click **New SSH key**
3. Paste the content of your public key
4. Save

### Test the connection

```bash
ssh -T git@github.com
```

Expected output:
> Hi username! You’ve successfully authenticated, but GitHub does not provide shell access.

---

## 5. Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

Check your settings:
```bash
git config --list
```

---

## 6. Clone Your Repository Locally

```bash
git clone git@github.com:username/my-first-repo.git
cd my-first-repo
```

### 7 Create a sample file

```bash
echo "# My First Repo" >> README.md
```

Add your files:
```bash
git add .
```

Commit them:
```bash
git commit -m "Initial commit"
```

---

## 8. Push Your Code to GitHub

```bash
git push
```

Now check your GitHub repository — your files should appear there.

---

## 9. Basic Git Commands Cheat Sheet

| Command | Description |
|----------|-------------|
| `git status` | Check changes in your working directory |
| `git add <file>` | Stage a file for commit |
| `git add .` | Stage all files |
| `git commit -m "message"` | Save changes locally |
| `git push` | Send changes to GitHub |
| `git pull` | Get latest changes from GitHub |
| `git clone <url>` | Copy an existing repository |
| `git log` | Show commit history |
| `git diff` | Show what changed before committing |

---

## 10. Troubleshooting

If you encounter issues, try to check on the net for solutions. It's important to learn how to troubleshoot Git problems ( and any problems in general ) by yourself. It's a really useful skill to have as a developer.

---

## 11. Done

You’ve successfully:
- Installed Git and SSH on Fedora  
- Created a GitHub account and repo  
- Generated and added SSH keys  
- Pushed and pulled files  

You’re ready to code and collaborate with GitHub.  
(｀・ω・´)ゞ
