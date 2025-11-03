# (´∀｀) Git & GitHub on Fedora — Full Beginner Guide

Welcome to the special GitHub class of **Dango** (´∀｀)♡  
This guide will help you set up Git, create your first repository, and push code to GitHub directly from Fedora Linux.

![Fedora GitHub Meme](https://i.imgur.com/fz7gh4I.png)

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

### Start the SSH agent and add your key

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

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
git config --global core.editor "nano"
```

Check your settings:
```bash
git config --list
```

---

## 6. Create a Local Project

```bash
mkdir my-first-repo
cd my-first-repo
echo "# My first repo" > README.md
```

Initialize the local Git repository:
```bash
git init
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

## 7. Link Local Repo to GitHub

Copy your SSH repo URL, then run:
```bash
git remote add origin git@github.com:username/my-first-repo.git
```

---

## 8. Push Your Code to GitHub

```bash
git branch -M main
git push -u origin main
```

Now check your GitHub repository — your files should appear there.

---

## 9. Basic Git Commands Recap

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

## 10. Test Your Setup

Try the full workflow:

```bash
cd ~
git clone git@github.com:username/my-first-repo.git
cd my-first-repo
echo "Hello GitHub!" >> test.txt
git add test.txt
git commit -m "Add test file"
git push
```

Then check your repo online — you should see the new file!

---

## 11. Troubleshooting

| Problem | Solution |
|----------|-----------|
| Permission denied (publickey) | Re-add your SSH key to GitHub or `ssh-add` again |
| Wrong branch name | Use `git branch -M main` before pushing |
| Forgot commit message | Run `git commit --amend` |
| Want to undo last commit | `git reset --soft HEAD~1` |

---

## 12. Done

You’ve successfully:
- Installed Git and SSH on Fedora  
- Created a GitHub account and repo  
- Generated and added SSH keys  
- Pushed and pulled files  

You’re ready to code and collaborate with GitHub.  
(｀・ω・´)ゞ Ganbatte!
