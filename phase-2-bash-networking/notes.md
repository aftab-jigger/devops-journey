# Phase 2: Bash Scripting & Networking

## Bash Script Kya Hoti Hai
- Ek text file jisme multiple commands likhi hoti hain, ek saath run karne ke liye
- `#!/bin/bash` se shuru hoti hai (shebang line)
- `chmod +x` se executable banti hai, `./script.sh` se chalti hai
- DevOps mein deployment automation (build, test, deploy) isi se hoti hai
- `#!/bin/bash` (shebang) — pehli line, batati hai script kis interpreter se chalni chahiye
- Agar shebang na ho to default shell use hota hai — kaam chal sakta hai lekin guarantee nahi
- Linux pe `sh` aksar ek alag, simpler shell (dash) hota hai jo bash-specific syntax (arrays, etc.) support nahi karta
- Mac pe `sh` asal mein bash hi hai, isliye ye farq Mac pe test nahi hota — sirf Linux/servers pe dikhega
- Isi liye hamesha shebang likhna professional practice hai, especially CI/CD aur cross-system scripts ke liye

## Variables & User Input
- Variable: `name="value"` — `=` ke aas paas space nahi hoti
- Value use karne ke liye `$` lagate hain: `$name`
- `read variable` se user se input le sakte hain, script ko interactive banata hai
- Isse scripts dynamic ban jati hain

## If-Else Conditions
- Syntax: `if [ condition ] then ... else ... fi` — `[ ]` ke andar spaces zaroori hain
- Comparison operators words mein: `-gt` (>), `-lt` (<), `-eq` (==), `-ge` (>=), `-le` (<=)
- Real DevOps use: disk space alerts, file existence check, health checks

## Loops
- Syntax: `for i in list do ... done`
- Files pe loop: `for file in path/*.ext`
- Real DevOps use: multiple servers restart karna, log files check karna

## Functions
- Define: `function_name() { ... }` — `function` keyword optional hai
- Arguments: `$1`, `$2`, waghera se access hote hain
- Jitni baar call karo, utni baar chalta hai

## Networking Basics
- **IP Address** — har device ka unique address
- **Port** — device ke andar specific service ka number (22=SSH, 80=HTTP, 443=HTTPS, 3000=Node, 5432=PostgreSQL)
- **DNS** — domain naam ko IP mein convert karta hai
- `ifconfig` / `ipconfig getifaddr en0` se apna local IP
- `ping <host>` se reachability check
- `lsof -i -P | grep LISTEN` se active/listening services dekh sakte hain
- Private IP sirf local network ke andar valid; public IP + open ports chahiye bahar se access ke liye
