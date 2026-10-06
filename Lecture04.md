# ls Options, find aur grep

---

## ls ki Options

### 1. ls -a

- Is location par **hidden aur unhidden sab files aur folders** dikhata hai.
- *Misal:* `ls -a`

### 2. ls -lh

- File ka **size check** karne k liye, wo bhi **human readable** form (KB, MB, GB) me.
- *Misal:* `ls -lh`

---

## find aur grep Me Farq

- **find** ko aise samjho jaise **library me book dhoondna** (book ka naam se).
- **grep** ko aise samjho jaise **book ke andar koi word dhoondna**.

| | find | grep |
|---|---|---|
| **Kya dhoondta hai** | File ya folder | File ke andar ka content |
| **Kis cheez se** | Name, type, size | Word ya line |
| **Misal** | `find . -name notes.txt` | `grep "hello" notes.txt` |

---

## grep Command

### 1. grep

- File ke **andar koi word** dhoondne k liye.
- Format: `grep "word" filename`
- *Misal:* `grep "hello" notes.txt`

### 2. grep -i

- **Small aur capital letters ko ignore** karta hai.
- Yani `Hello`, `hello` aur `HELLO` sab mil jate hain.
- *Misal:* `grep -i "hello" notes.txt`

### 3. grep -n

- Word kis **line number** par hai ye bhi batata hai.
- *Misal:* `grep -n "hello" notes.txt`

### 4. grep -n -i

- **Line number** batata hai aur saath me **chote bare letters ko ignore** karta hai.
- *Misal:* `grep -n -i "hello" notes.txt`

### 5. grep -r

- **Poore folder ke andar** word dhoondta hai.
- Result me **file ka naam** bhi batata hai.
- *Misal:* `grep -r "hello" .`

### 6. grep -v

- Jin lines me word **hai, wo lines hata deta hai** aur **baqi sab lines show** karta hai.
- *Misal:* `grep -v "hello" notes.txt`

### 7. grep -c

- **Kitni lines me** word use hua hai ye **count** batata hai.
- *Misal:* `grep -c "hello" notes.txt`

---

## find Command

### 1. find

- File ko dhoondne k liye. Ye **name, type aur size** se dhoondh sakta hai.
- `.` ka matlab hai **isi folder se dhoondo**.

### 2. find . -name

- File ko **name se** dhoondta hai.
- *Misal:* `find . -name notes.txt`

### 3. find . -iname

- Name se dhoondta hai aur **small capital ko ignore** karta hai.
- *Misal:* `find . -iname notes.txt`

### 4. find . -name "*.txt"

- **Sari files** dhoondta hai jin ke **end me .txt** ho.
- `*` ka matlab hai "kuch bhi".
- *Misal:* `find . -name "*.txt"`

### 5. find . -type f

- Sirf **files** dhoondne k liye (**f = file**).
- *Misal:* `find . -type f`

### 6. find . -type d

- Sirf **folders** dhoondne k liye (**d = directory**).
- *Misal:* `find . -type d`

### 7. find . -type f -size -1M

- **1 MB se choti files** dhoondne k liye.
- *Misal:* `find . -type f -size -1M`

---

## Quick Revision

| Command | Kaam |
|---|---|
| `ls -a` | Hidden files bhi dikhao |
| `ls -lh` | Size readable form me |
| `grep "word" file` | File me word dhoondo |
| `grep -i` | Small capital ignore |
| `grep -n` | Line number batao |
| `grep -r` | Poore folder me dhoondo |
| `grep -v` | Word wali lines hata do |
| `grep -c` | Kitni lines me word hai |
| `find . -name` | Name se file dhoondo |
| `find . -iname` | Name se, small capital ignore |
| `find . -type f` | Sirf files |
| `find . -type d` | Sirf folders |
| `find . -size -1M` | 1 MB se choti files |
