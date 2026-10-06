# Communication, Data, Metadata & Logs

---

## Communication

### 1. Internal Communication

- Jab **ek hi system ya network ke andar** cheezein aapas me baat karti hain.
- Isme data **bahir internet par nahi jata**, andar hi andar rehta hai.
- Is me **hardware parts** (CPU, RAM, hard disk) aur **programs** (processes) ek dusre se data share karte hain.
- Ek hi office ya ghar ke network me **computers aur printer** ka aapas me connect hona bhi internal communication hai.
- Is me **risk kam** hota hai kyunke bahir ke log directly involve nahi hote.
- *Misal:* Aap ne apne laptop se **ghar ke WiFi par laga hua printer** use kiya.

### 2. External Communication

- Jab **hamara system bahir ki duniya (internet)** se baat karta hai.
- Isme data **doosre networks, servers aur websites** tak jata hai.
- Is me **risk zyada** hota hai, kyunke **hackers** isi raste se attack karte hain.
- Isi liye **firewall, password aur encryption** zaroori hote hain.
- *Misal:* Aap ne **Google kholi, WhatsApp message bheja ya email send ki**.

### 3. Dono me farq

| | Internal | External |
|---|---|---|
| **Kahan hoti hai** | Same system / network ke andar | System se bahir internet par |
| **Risk** | Kam | Zyada |
| **Misal** | Laptop se printer | Laptop se website |

---

## Data aur Metadata

### 1. Data kya hota hai

- **Data** wo **raw information** hoti hai jo hum store ya use karte hain.
- Ye **text, numbers, images, video, audio** kuch bhi ho sakta hai.
- Computer me **sab kuch data hi hota hai** (files, photos, messages).
- *Misal:* Ek **photo**, ek **PDF file** ya aap ka **naam aur phone number**.

### 2. Metadata kya hota hai

- **Metadata** ka matlab hai **"data ke baare me data"**.
- Ye batata hai ke **asli data ke saath kya details judi hain**.
- Is me hota hai: file **kab bani**, **kis ne banayi**, **size** kitna hai, **kis device** par bani aur **location** kya thi.
- Asli content kholne ke bagair bhi **metadata se bohat si info** mil jati hai.
- *Misal:* Ek **photo** data hai. Us photo ki **date, camera ka model aur GPS location** metadata hai.

### 3. Dono me farq

| | Data | Metadata |
|---|---|---|
| **Matlab** | Asli information | Us information ki details |
| **Misal** | Photo | Photo kab aur kahan li gayi |

### 4. Linux me metadata

- `file file1.jpg` se **file ki type** pata chalti hai.
- `ls -lh` se **file ka size** pata chalta hai.
- Image ka **detailed metadata** (device, location) `exiftool file1.jpg` se milta hai.

---

## Logs

### 1. Logs kya hote hain

- **Logs** system ka **record** hote hain, jin me **har activity likhi** jati hai.
- Ye sari info system me **store hoti rehti hai**.
- Logs me **kab, kya aur kis ne** kiya ye sab hota hai.
- *Misal:* Laptop **2:30 pm** par on hua, **1st attempt fail**, phir **2nd aur 3rd attempt** hua. Ye sab logs me save ho gaya.

### 2. Logs kyun zaroori hain

- **Error ya problem** dhoondne k liye.
- **Security check** k liye ke koi **unknown banda login karne ki koshish** to nahi kar raha.
- **Hacking attempt** pakadne k liye. Bar bar fail login logs me nazar aa jata hai.

### 3. Linux me logs dekhna

- `tail -f filename` se logs **live monitor** kar sakte hain.
- `less filename` se **page by page** parh sakte hain.
- `grep "failed" filename` se logs me **sirf failed attempts** dhoondh sakte hain.
- *Misal:* `grep "failed" auth.log`

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **Internal Communication** | System ke andar ki baat cheet |
| **External Communication** | System aur internet ke beech baat cheet |
| **Data** | Asli information |
| **Metadata** | Data ke baare me details |
| **Logs** | System ki activity ka record |
