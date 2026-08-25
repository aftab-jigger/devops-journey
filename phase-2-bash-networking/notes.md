# Phase 2: Bash Scripting & Networking

## Bash Script Kya Hoti Hai
- Ek text file jisme multiple commands likhi hoti hain, ek saath run karne ke liye
- `#!/bin/bash` se shuru hoti hai (shebang line)
- `chmod +x` se executable banti hai, `./script.sh` se chalti hai
- DevOps mein deployment automation (build, test, deploy) isi se hoti hai

## Variables & User Input
- Variable: `name="value"` — `=` ke aas paas space nahi hoti
- Value use karne ke liye `$` lagate hain: `$name`
- `read variable` se user se input le sakte hain, script ko interactive banata hai
- Isse scripts dynamic ban jati hain — hardcoded values ki jagah user/environment se value le sakte hain

## If-Else Conditions
- Script ko decision-making capability deta hai: "agar X true hai to Y karo, warna Z"
- Syntax: `if [ condition ] then ... else ... fi` — `[ ]` ke andar spaces zaroori hain
- Comparison operators words mein: `-gt` (>), `-lt` (<), `-eq` (==), `-ge` (>=), `-le` (<=)
- Real DevOps use: disk space alerts, file existence check, health checks, deployment validations

## Loops
- Ek kaam ko repeat karne ke liye, bina command baar baar likhe
- Syntax: `for i in list do ... done` — `i` temporary variable hai jo har iteration mein next value leta hai
- Files pe loop: `for file in path/*.ext` — matching sab files ko process karta hai
- Real DevOps use: multiple servers restart karna, sab log files check karna, bulk file processing
