# (´∀｀) Linux Beginner Cheat Sheet — by Dango

Welcome to the **Linux Cheat Sheet** of *Dangonomics*!  
A simple, colorful reference for beginners to learn the essential commands.  
Use it when you forget, explore when you’re curious, and enjoy the Linux journey (｀・ω・´)ゞ

---

## 1. Navigation & Files

| Command | Description | Example |
|----------|--------------|----------|
| `pwd` | Show current directory | `pwd` |
| `ls` | List files | `ls -la` |
| `cd` | Change directory | `cd Documents` |
| `cd ..` | Go up one folder | `cd ..` |
| `mkdir` | Create folder | `mkdir new_folder` |
| `rmdir` | Remove empty folder | `rmdir old_folder` |
| `rm -r` | Delete folder and contents | `rm -r my_folder` |
| `touch` | Create new empty file | `touch notes.txt` |
| `cp` | Copy file or directory | `cp file.txt backup.txt` |
| `mv` | Move or rename | `mv file.txt ~/Documents/` |
| `cat` | Display file content | `cat notes.txt` |
| `less` | View long files page by page | `less /etc/passwd` |
| `head` | Show first lines | `head -n 10 file.txt` |
| `tail` | Show last lines | `tail -f log.txt` |

---

## 2. File Permissions & Ownership

| Command | Description | Example |
|----------|--------------|----------|
| `ls -l` | Show permissions | `ls -l` |
| `chmod` | Change permissions | `chmod 755 script.sh` |
| `chown` | Change owner | `sudo chown alex:alex file.txt` |
| `chgrp` | Change group | `sudo chgrp users file.txt` |

Permission values:  
`r` = read, `w` = write, `x` = execute  
Example: `chmod u+x file.sh` → give execute rights to user.

---

## 3. System Info

| Command | Description | Example |
|----------|--------------|----------|
| `uname -a` | Show system information | `uname -a` |
| `hostname` | Display hostname | `hostname` |
| `uptime` | Show system uptime | `uptime` |
| `df -h` | Disk usage (human-readable) | `df -h` |
| `du -sh folder` | Size of a folder | `du -sh Downloads` |
| `free -h` | Memory usage | `free -h` |
| `top` | View active processes | `top` |
| `htop` | Interactive process viewer | `htop` |

---

## 4. Package Management (Fedora)

| Command | Description | Example |
|----------|--------------|----------|
| `sudo dnf update` | Update all packages | `sudo dnf update -y` |
| `sudo dnf install` | Install a package | `sudo dnf install git` |
| `sudo dnf remove` | Remove a package | `sudo dnf remove nano` |
| `dnf search` | Search a package | `dnf search python` |
| `dnf info` | Get package info | `dnf info neovim` |

---

## 5. Networking Basics

| Command | Description | Example |
|----------|--------------|----------|
| `ping` | Check connectivity | `ping google.com` |
| `ip a` | Show IP addresses | `ip a` |
| `ifconfig` | Network configuration (old) | `ifconfig` |
| `curl` | Fetch a URL | `curl https://example.com` |
| `wget` | Download a file | `wget https://example.com/file.zip` |
| `ssh` | Connect to remote server | `ssh user@host` |
| `scp` | Copy over SSH | `scp file.txt user@host:/home/user/` |

---

## 6. Process Management

| Command | Description | Example |
|----------|--------------|----------|
| `ps aux` | List all processes | `ps aux` |
| `kill PID` | Kill a process | `kill 1234` |
| `killall name` | Kill processes by name | `killall firefox` |
| `jobs` | Show background jobs | `jobs` |
| `fg` | Bring job to foreground | `fg` |
| `bg` | Send job to background | `bg` |

---

## 7. Searching & Filtering

| Command | Description | Example |
|----------|--------------|----------|
| `grep` | Search text in files | `grep "main" *.c` |
| `find` | Locate files | `find /home -name "*.txt"` |
| `locate` | Search with index | `locate bashrc` |
| `which` | Find path of command | `which python3` |
| `history` | Show recent commands | `history` |

Combine with pipes:
```bash
ls -la | grep "config"
ps aux | grep firefox
```

---

## 8. Archives & Compression

| Command | Description | Example |
|----------|--------------|----------|
| `tar -cvf` | Create archive | `tar -cvf backup.tar folder/` |
| `tar -xvf` | Extract archive | `tar -xvf backup.tar` |
| `gzip` | Compress file | `gzip file.txt` |
| `gunzip` | Decompress | `gunzip file.txt.gz` |
| `zip` | Create .zip archive | `zip -r backup.zip folder/` |
| `unzip` | Extract .zip file | `unzip backup.zip` |

---

## 9. Users & Groups

| Command | Description | Example |
|----------|--------------|----------|
| `whoami` | Show current user | `whoami` |
| `id` | Display user info | `id alex` |
| `sudo adduser` | Create new user | `sudo adduser student` |
| `sudo passwd` | Change password | `sudo passwd student` |
| `groups` | Show group memberships | `groups alex` |

---

## 10. Text Editing

| Editor | Description | Example |
|---------|--------------|----------|
| `nano file` | Simple terminal editor | `nano notes.txt` |
| `vim file` | Powerful modal editor | `vim config.ini` |
| `cat > file` | Create file via shell | `cat > hello.txt` |

To exit `nano`: `Ctrl + X`, then `Y`, then `Enter`  
To exit `vim`: press `Esc` then type `:wq`

---

## 11. Miscellaneous Commands

| Command | Description | Example |
|----------|--------------|----------|
| `date` | Show current date/time | `date` |
| `cal` | Display calendar | `cal` |
| `echo` | Print text | `echo "Hello World"` |
| `man` | Open manual | `man ls` |
| `clear` | Clear terminal | `clear` |
| `exit` | Close shell session | `exit` |

---

## 12. Bonus Tips

- Use `TAB` for auto-completion  
- Use `↑` and `↓` to navigate command history  
- Combine commands:  
  ```bash
  cd ~/Downloads && ls -la
  ```
- Redirect output:  
  ```bash
  ls > files.txt
  cat file.txt >> all.txt
  ```

---

## (´∀｀) Closing Words

Linux can be intimidating at first, but every command you learn gives you a bit more power and control.  
Practice, experiment, break things, fix them, and soon it’ll feel like second nature.  

(｀・ω・´)ゞ
