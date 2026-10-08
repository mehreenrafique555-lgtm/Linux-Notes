# sudo aur chmod (Permissions)

---

## sudo Command

### 1. sudo kya hai

- `sudo` ka matlab hai **root se request karna** ke ye command **execute** kar do.
- Normal user ke paas power kam hoti hai, isi liye **sudo** lagate hain.

### 2. sudo kahan use hota hai

| Kaam | Misal |
|---|---|
| **Installation** (software install) | `sudo apt install packagename` |
| **Version upgrade** | `sudo apt upgrade` |
| **System fix** | `sudo` ke saath fix command |

- Ye teeno kaam **root user** hi kar sakta hai.

### 3. sudo -i

- `sudo -i` se hum **root user me login** ho jate hain.
- Is ke baad har command **root ki power** se chalti hai, har bar `sudo` nahi likhna parta.
- Wapas normal user me aane k liye `exit` likho.

### 4. Ctrl + C

- Chalti hui command ko **rokne (cancel)** k liye.
- Screen **saaf** karne k liye `clear` ya `Ctrl + L` use hota hai.

---

## chmod Command

### 1. Numbers se permission

- `chmod` file ki **permission badalta** hai.
- Number ke **teen digits** hote hain: **Owner, Group, Other**.
- Har digit **r (4) + w (2) + x (1)** ka total hota hai.

| Number | Matlab |
|---|---|
| `000` | **Koi permission nahi** (file locked) |
| `777` | **Sab ko permission** (r + w + x) |
| `661` | Owner = 6 (rw), Group = 6 (rw), Other = 1 (sirf execute) |

- *Misal:* `chmod 000 run.ssh` ke baad file **locked** ho jati hai, koi use nahi kar sakta.

### 2. Letters se permission

- Letters ka matlab:
  - `u` = **owner** (user)
  - `g` = **group**
  - `o` = **other**
  - `a` = **all** (teeno)
- `+` se permission **dete** hain aur `-` se permission **wapis lete** hain.
- Permission ki letters: `r` (read), `w` (write), `x` (execute).

| Command | Kaam |
|---|---|
| `chmod a+rwx hello.txt` | **Teeno ko ek sath** r, w, x permission do |
| `chmod a-rwx hello.txt` | **Teeno se permission wapis** le lo |
| `chmod u+x hello.txt` | Sirf owner ko execute do |
| `chmod g-w hello.txt` | Group se write hata do |

### 3. Permission check karna

- `ls -l` se dekhte hain **kis ke paas kaunsi permission** hai.

---

## Practice Steps

```bash
mkdir vault
cd vault
touch hello.txt
ls -l
chmod 661 hello.txt
ls -l
chmod a+rwx hello.txt
ls -l
chmod a-rwx hello.txt
ls -l
cd ..
```

- `cd ..` se **folder se bahir** aate hain.

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **sudo** | Root se request karke command chalana |
| **sudo -i** | Root user me login |
| **000** | Koi permission nahi |
| **777** | Sab ko permission |
| **u / g / o / a** | Owner / Group / Other / All |
| **+ / -** | Permission dena / wapis lena |
| **ls -l** | Permission check karna |
