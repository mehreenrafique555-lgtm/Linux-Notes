# Users, sudo aur Permissions

---

## Root User aur Normal User

### 1. Farq

- **Root user** manager ki tarah hota hai, is ke paas **sab se zyada access aur power** hoti hai.
- **Normal user** employee ki tarah hota hai, is ki power **kam** hoti hai.

### 2. sudo

- Root ki power **use karne k liye** `sudo` lagate hain.
- Ye aise hai jaise manager se **request karna** ke "please ye kaam kar do".
- *Misal:* `sudo apt update`

### 3. whoami aur exit

- `whoami` batata hai ke aap **kaun se user** ho.
- `sudo whoami` ka result **root** aata hai.
- `sudo -i` se hum **root user me login** ho jate hain.
- `exit` se **root se wapas normal user** me aate hain.

---

## Permissions

### 1. Kis ko permission deni hai

- **Owner:** file ka malik (hum khud).
- **Group:** group ke members.
- **Other:** jo group se bahir hain.

### 2. Permission ki types

| Permission | Letter | Number | Kaam |
|---|---|---|---|
| **Read** | `r` | 4 | File parhna / folder ki list dekhna |
| **Write** | `w` | 2 | File me likhna / folder me file banana |
| **Execute** | `x` | 1 | File chalana / folder ko open karna |

- Numbers ko **jama (add)** karte hain: `rwx` = 4+2+1 = **7**, `r-x` = 4+0+1 = **5**.

### 3. Misal

- **Owner** → `rwx` = 7
- **Group** → `r-x` = 5
- **Other** → `r-x` = 5
- Yani permission number bana **755**.

---

## chmod Command

### 1. chmod

- File ki **permission badalne** k liye use hota hai.
- Format: `chmod number filename`

### 2. Misalein

| Command | Matlab | `ls -l` me |
|---|---|---|
| `chmod 750 content.txt` | Owner sab, group parh sake, other kuch nahi | `-rwxr-x---` |
| `chmod 774 content.txt` | Owner aur group sab, other sirf parh sake | `-rwxrwxr--` |
| `chmod 666 content.txt` | Sab parh aur likh sakte hain | `-rw-rw-rw-` |
| `chmod 770 secret.txt` | Owner aur group sab, other kuch nahi | `-rwxrwx---` |
| `chmod 000 content.txt` | **Sab ki permission band** | `----------` |

### 3. Permission check karna

- `ls -l` file ki **permission** dikhata hai.
- `ls -la` **hidden files** bhi dikhata hai, saath me **size aur owner** ki info.

---

## Practice Steps

```bash
mkdir ~/lab
cd lab
pwd
touch content.txt
ls
chmod 750 content.txt
ls -l
```

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **root** | Sab se zyada power wala user |
| **sudo** | Root ki power use karna |
| **whoami** | Kaun sa user hoon |
| **r / w / x** | 4 / 2 / 1 |
| **chmod** | Permission badalna |
| **ls -l** | Permission dekhna |
