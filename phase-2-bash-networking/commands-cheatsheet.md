# Phase 2: Bash Scripting & Networking Cheatsheet

| Command / Syntax | Description |
|---|---|
| `#!/bin/bash` | Script ki pehli line (shebang) — batata hai ye bash script hai |
| `nano <file>` | File ko edit mode mein kholta hai (Ctrl+O save, Ctrl+X exit) |
| `chmod +x <script>` | Script ko executable banata hai |
| `./<script>` | Script ko run karta hai |
| `variable="value"` | Variable banata hai (= ke aas paas space nahi hoti) |
| `$variable` | Variable ki value use/print karta hai |
| `read <variable>` | User se input leta hai aur variable mein store karta hai |
| `if [ condition ] then ... fi` | Condition check karke decision leta hai |
| `-gt` `-lt` `-eq` `-ge` `-le` | Comparison operators: greater/less/equal/greater-eq/less-eq than |
| `for i in ... do ... done` | Loop — kisi list/range pe repeat karta hai |
| `for file in path/*.ext` | Kisi folder ki matching files pe loop karta hai |
