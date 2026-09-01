# Phase 3: Git Deep Dive & Python Basics Cheatsheet

| Command / Syntax | Description |
|---|---|
| `git branch` | Current branches list karta hai, `*` current branch dikhata hai |
| `git checkout -b <name>` | Nayi branch banata hai aur usmein switch kar deta hai |
| `git push origin <branch>` | Specific branch ko GitHub pe push karta hai |
| `git config --global user.name/email` | Git identity (naam/email) set karta hai |
| `git config pull.rebase false` | Pull karte waqt merge strategy use karne ko set karta hai |
| `git pull origin <branch>` | Remote branch ke changes local mein le aata hai |
| `git branch -d <branch>` | Merge ho chuki branch ko delete karta hai (safe delete) |
| `python3 --version` | Installed Python version check karta hai |
| `print("text")` | Screen pe text print karta hai (Bash ke echo jaisa) |
| `python3 <script>.py` | Python script ko run karta hai |
| `variable = value` | Variable banata hai (koi let/const/var keyword nahi chahiye) |
| `print("a:", var)` | Comma se multiple cheezein ek saath print karta hai |
| `if condition:` | Colon ke sath, block agli line pe indent hota hai (curly braces nahi) |
| `input("prompt")` | User se input leta hai (hamesha string return karta hai) |
| `int(value)` | Value ko integer (number) mein convert karta hai |
| `for i in range(a, b):` | Loop, a se (b-1) tak — end number exclude hota hai |
| `import <module>` | Extra functionality add karta hai (jaise JS ka import/require) |
| `os.listdir(".")` | Current folder ki files/folders list karta hai |
| `def function_name(param):` | Function define karta hai, colon + indentation ke sath |
| `return value` | Function se value wapas bhejta hai |
| `os.path.expanduser("~/path")` | `~` ko poore absolute path mein convert karta hai |
| `os.path.join(a, b)` | Do paths ko safely combine karta hai |
| `os.path.isfile(path)` | Check karta hai ye file hai ya folder |
| `os.path.getsize(path)` | File ka size (bytes mein) deta hai |
