# Linux Commands Cheatsheet

| Command | Description |
|---|---|
| `pwd` | Current directory ka path dikhata hai (Print Working Directory) |
| `ls` | Current folder ke andar files aur folders list karta hai |
| `whoami` | Logged-in user ka naam dikhata hai |
| `cd <folder-name>` | Us folder ke andar jata hai (Change Directory) |
| `cd ..` | Ek folder upar/peeche jata hai (parent directory) |
| `cd ~` | Seedha home directory pe wapas le jata hai |
| `mkdir <name>` | Naya folder/directory banata hai |
| `touch <file>` | Naya empty file banata hai |
| `cat <file>` | File ka content screen pe dikhata hai |
| `echo "text" > file` | File mein text likhta hai, purana content overwrite kar deta hai |
| `echo "text" >> file` | File ke end mein text add karta hai, purana content safe rehta hai |
| `rm <file>` | File ko delete karta hai (Remove) |
| `ls -l` | Detailed listing dikhata hai jisme permissions, owner, size shamil hote hain |
| `chmod +x <file>` | File ko executable banata hai (run kar sakte ho) |
| `chmod 755 <file>` | Numeric tareeqa: owner=rwx(7), group=r-x(5), others=r-x(5) |
| `ps` | Current terminal session ke processes dikhata hai |
| `ps aux` | System ke **sab** running processes dikhata hai |
| `top` | Live real-time processes ka view (CPU/memory ke sath), `q` se exit |
| `command &` | Command ko background mein chalata hai |
| `kill <PID>` | Diye gaye PID wali process ko band/terminate karta hai |
| `brew search <name>` | Homebrew pe kisi software ko search karta hai (Mac) |
| `brew install <name>` | Software install karta hai |
| `brew uninstall <name>` | Installed software ko remove karta hai |
| `brew list` | Sab brew se installed software list karta hai |
| `id` | User ka UID, primary group, aur sab groups dikhata hai |
| `groups` | Sirf us user ki groups list karta hai |
| `sudo <command>` | Command ko temporarily root/admin powers ke sath chalata hai |
| `ssh-keygen -t ed25519 -C "label"` | Naya SSH key pair (private + public) generate karta hai |
| `cat ~/.ssh/id_ed25519.pub` | Public key ka content dikhata hai (ye server/GitHub ko diya jata hai) |
| `crontab -l` | Current user ke scheduled cron jobs list karta hai |
| `crontab -e` | Cron jobs edit karne ke liye editor kholta hai |
| `crontab -r` | User ke sab cron jobs remove kar deta hai |
