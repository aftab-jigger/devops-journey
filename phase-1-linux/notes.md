# Phase 1: Linux & Command Line

## Linux kya hai aur kyun zaroori hai
- Linux ek free, open-source operating system hai
- Zyada tar servers, cloud machines, aur Docker containers Linux pe chalte hain
- DevOps mein terminal/command line use hoti hai kyunke servers pe GUI nahi hoti,
  aur commands ko automate/script kiya ja sakta hai

## Terminal basics
- Mac ka Terminal app Unix-based hai, Linux commands yahan bhi chalti hain
- Command prompt current location aur user dikhata hai

## Navigation
- Har folder ke andar jaane ke liye `cd <name>`, bahar/upar jaane ke liye `cd ..`
- `cd ~` hamesha seedha home directory le jata hai, chahe kahin bhi ho
- Prompt hamesha current location dikhata hai

## Files aur Folders Manage Karna
- `mkdir` naya folder banata hai, `touch` naya empty file banata hai
- `cat` file ka content dikhata hai
- `>` overwrite karta hai (purana content mit jata hai), `>>` end mein add karta hai (append)
- `rm` file delete karta hai

## File Permissions
- Har file ke 3 permission types: read (r), write (w), execute (x)
- 3 categories: owner, group, others — `ls -l` se dikhti hain (jaise `-rw-r--r--`)
- Bina execute (`x`) permission ke koi script run nahi ho sakti ("permission denied" error)
- `chmod +x file` se execute permission milti hai
- Numeric tareeqa: r=4, w=2, x=1 — jaise `chmod 755` = owner full access, group/others read+execute
- Scripts/automation ke liye ye bohat zaroori hai real DevOps kaam mein

## Process Management
- Har chalta hua program ek **process** hai, jiska unique **PID** (Process ID) hota hai
- `ps` sirf current session ki processes dikhata hai, `ps aux` **sab** system processes
- `top` live view deta hai (CPU/memory usage), `q` se exit hota hai
- `command &` se koi command background mein chalti hai
- `kill <PID>` se us PID wali process band ho jati hai
- `ps aux | grep <name>` se kisi specific process ko naam se dhoond sakte hain
- Server pe hangi/crashed processes dhoond ke restart karne ke liye ye commands zaroori hain

## Package Managers
- Software install karne ka command-line tareeqa, servers pe GUI nahi hoti isliye zaroori hai
- Mac → `brew` (Homebrew), Ubuntu/Debian → `apt`, RedHat/CentOS → `yum`/`dnf`
- Concept sab jagah same: search, install, uninstall, list
- `brew install <name>` se install, `brew uninstall <name>` se remove
- Cloud servers (AWS Ubuntu, etc.) pe yehi kaam `apt` se hoga

## Users & Groups
- Linux multi-user system hai, har user ka apna UID aur groups hote hain
- `id` se UID, primary group, aur sab groups dikhte hain; `groups` sirf groups
- **root** sabse powerful user hota hai — direct root se kaam karna risky hai (security best practice nahi)
- `sudo <command>` se koi normal user temporarily root powers le sakta hai ek command ke liye
- Real servers pe: har team member ka apna normal user hota hai, zaroorat pe `sudo` use karte hain, direct root login nahi karte

## SSH (Secure Shell)
- Remote server ko terminal se control karne ka secure tareeqa
- Key pair: **private key** (secret, apne paas rakhte hain) + **public key** (server/GitHub ko dete hain)
- `ssh-keygen -t ed25519 -C "label"` se naya key pair banta hai
- AWS server access, deployment pipelines, aur GitHub SSH push — sab isi concept pe based hain
- Passwords ke bajaye keys zyada secure hoti hain login ke liye

## Cron Jobs (Scheduled Tasks)
- Cron ek scheduler hai jo fixed time pe automatically command/script chalata hai
- `crontab -e` se edit karte hain, `crontab -l` se list dekhte hain, `crontab -r` se sab remove
- Format: `minute hour date month weekday command` — `*` ka matlab "har" (every)
- Real use: automated backups, log cleanup, scheduled reports
- Editor `vim` ho to: `i` = insert mode, `Esc` = normal mode, `:wq` = save+quit, `dd` = line delete
