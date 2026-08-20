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
