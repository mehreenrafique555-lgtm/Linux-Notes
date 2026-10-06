# 🐧 Linux Commands – Easy Notes (Kali Linux)

Ye notes beginners k liye hain. Har command ka matlab aur example diya gaya hai.

---

## 📌 Basic Concepts

| Term | Matlab |
|------|--------|
| **CLI** | Command Line Interface – jahan hum commands likhte hain |
| **Kali Linux** | Security/hacking testing k liye use hone wala Linux OS |
| **Logs** | System har activity ka record rakhta hai (e.g. laptop kab on hua, login attempt fail hua ya pass) |
| **root** | Sab se upar ka point (`/`) – is se piche nahi ja sakte |
| **Home (`~`)** | User ka apna folder, e.g. `/home/david` |

> 💡 **Terminal colors:** 🔵 Blue = Folder, ⚪ White = Files

**Logs ki example:** Laptop 2:30 pm pe on kiya → 1st attempt fail → 2nd attempt → 3rd attempt. Ye sari info system logs me store hoti rehti hai.

---

## 📍 1. Navigation (Folders me ghoomna)

| Command | Kaam |
|---------|------|
| `pwd` | **P**rint **W**orking **D**irectory – abhi kis location pe ho ye batata hai |
| `ls` | List – folder me konsi files/folders hain |
| `ls -l` | Poori detailed list |
| `ls -a` | Hidden + unhidden sab files dikhata hai |
| `ls -lh` | File size human-readable form me (KB, MB) |
| `cd foldername` | Folder ke andar jana (forward) |
| `cd ..` | Ek step peeche jana |
| `cd ~` | Home pe jana |
| `cd /` | Root pe jana |
| `cd` | Seedha home pe |
| `clear` | Terminal screen saaf karna |

**Example:**
```bash
pwd              # /home/david
ls               # list dekho
cd Downloads     # Downloads folder me jao
cd ..            # wapas aao
```

---

## 📁 2. Files aur Folders banana

| Command | Kaam |
|---------|------|
| `mkdir foldername` | Naya folder banana |
| `touch filename` | Nayi khali file banana |
| `nano filename` | File me text likhna/edit karna |

**Example:**
```bash
mkdir first_new
cd first_new
touch index.html
touch index.js
touch index.css
```

**Nano me save kaise kare:**
`Ctrl + X` → `Y` → `Enter`

---

## 📖 3. File ka content parhna

| Command | Kaam |
|---------|------|
| `cat filename` | Poora content ek sath dikhata hai |
| `less filename` | Page by page dikhata hai |
| `head filename` | File ki shuru ki lines (header) |
| `head -n 25 filename` | Shuru ki 25 lines |
| `tail filename` | File ki aakhri lines (bottom) |
| `tail -f filename` | Live monitor – nayi lines real-time me dikhti hain |

**`less` ke shortcuts:**

| Key | Kaam |
|-----|------|
| `Space` | Next page |
| `b` | Back page |
| `G` | Seedha last page |
| `g` | Seedha first page |
| `/word` | Koi word search karna |
| `q` | Bahir aa jana (quit) |

**Example:**
```bash
cat index.js
less insta.html
head -n 25 insta.html
```

---

## ✍️ 4. echo – Text likhna

```bash
echo "Hello class" >> notes.txt    # file me add (append) hota hai
echo "New text" > notes.txt         # purana sab delete, sirf naya save
```

| Symbol | Matlab |
|--------|--------|
| `>>` | Purane content ke baad **add** karta hai |
| `>` | Purana content **delete** karke naya likhta hai ⚠️ |

---

## 📋 5. Copy aur Delete

| Command | Kaam |
|---------|------|
| `cp notes.txt backup.txt` | File ki copy banana |
| `rm index.css` | File delete karna |
| `rmdir foldername` | Folder delete karna |

**Folder delete karne ka tareeqa:**
1. Folder se bahir aao (`cd ..`)
2. `clear` karo
3. `ls` se check karo
4. `rmdir first_new`

> ⚠️ `rmdir` sirf **khali** folder delete karta hai. Agar folder me files hon to `rm -r foldername` use hota hai (careful rehna, wapas nahi aata!).

---

## 🔍 6. Search karna (find & grep)

| Command | Matlab | Example |
|---------|--------|---------|
| `find` | File/folder ko **name** se dhoondna 📚 (book dhoondna) | `find . -name index.html` |
| `grep` | File ke **andar ka content** dhoondna 📖 (book ke andar kuch dhoondna) | `grep "hello" notes.txt` |

---

## 🖼️ 7. File ki information

```bash
file file1.jpg
```
File ka type aur basic info batata hai. (Image ki detailed info jaise kis device pe bani, location waghera ke liye `exiftool file1.jpg` use hota hai.)

---

## ⚡ Quick Cheat Sheet

```text
pwd        → abhi kahan ho
ls         → list
ls -a      → hidden files bhi
ls -lh     → size ke sath
cd         → folder change
mkdir      → folder banao
touch      → file banao
nano       → file edit
cat        → content parho
less       → page by page
head/tail  → shuru/aakhir ki lines
echo       → text likho
cp         → copy
rm         → file delete
rmdir      → folder delete
find       → name se dhoondo
grep       → content me dhoondo
clear      → screen saaf
```

---

⭐ Agar notes helpful lage to repo ko star kar dena!
