# Phase 3: Git Deep Dive & Python Basics

## Branching
- Branch = code ka alag "timeline", bina main/master ko chhue changes karne ke liye
- `git branch` se list, `git checkout -b <name>` se nayi branch bana ke switch
- Real teams: har feature/bugfix apni branch pe, phir main mein merge
- Isse main branch hamesha stable rehta hai

## Pull Requests (PR)
- Jab branch ka kaam complete ho, PR banate hain: "ye code main mein merge kar do" ki request
- Team review karti hai, comments de sakti hai, CI tests chal sakte hain, phir merge hota hai
- Isse galtiyan directly main branch mein nahi jatin

## Merge Conflicts
- Jab do branches ek hi file ki ek hi line ko alag tarah change karein, Git khud decide nahi kar pata
- `git pull origin main` conflict trigger karta hai agar dusri branch mein overlapping changes hain
- File mein `<<<<<<< HEAD`, `=======`, `>>>>>>> main` markers dikhte hain — dono versions
- Manually decide karo kya rakhna hai, markers hata do, phir `git add`, `git commit`, `git push`
- Ye normal hai jab team members same file pe kaam karte hain — dar ki baat nahi

## Python Basics
- `.py` extension, `print("text")` se output (Bash ke echo, JS ke console.log jaisa)
- `python3 script.py` se run karte hain (Bash ke `./script.sh` se alag, chmod +x zaroori nahi)
- DevOps mein use: automation scripts, cloud SDKs (AWS/Docker/K8s), infrastructure scripts
- Logic JS jaisa hi hai, sirf syntax alag hai

## Variables & Data Types
- Koi keyword nahi chahiye (let/const/var nahi): `name = "Aftab"`
- Semicolon zaroori nahi
- Data types: str (string), int (number), float (decimal), bool (True/False — capital letter)
- `print("label:", variable)` se comma se multiple cheezein ek saath print hoti hain

## If-Else in Python
- Curly braces `{}` nahi, **indentation (4 spaces)** se code blocks define hote hain — mandatory hai
- Syntax: `if condition:` phir agli line indent, `else:` phir indent
- Comparison operators JS jaise: `==`, `!=`, `>`, `<`, `>=`, `<=`
- `input("prompt")` se user input (hamesha string aata hai), `int()` se number mein convert

## Loops in Python
- Syntax: `for i in range(a, b):` — a se (b-1) tak chalta hai, **end number exclude hota hai** (important gotcha)
- `import os` se modules import karte hain (JS ke require/import jaisa concept)
- `os.listdir(".")` se current folder ki files list hoti hain (Bash ke `for file in *.ext` jaisa)
