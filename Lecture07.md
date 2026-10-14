# Program, Process aur Service

---

## Program vs Process

### 1. Program

- Ek **file** jo **SSD (storage)** me pari hoti hai.
- Ye sirf **save** hoti hai, chal nahi rahi hoti.
- *Misal:* Computer me install **Chrome** ki file.

### 2. Process

- Wohi file jab **actively run** ho rahi hoti hai, to wo **process** ban jati hai.
- Process **CPU** me running form me hoti hai.
- *Misal:* Chrome ko **double click** karke kholna.

### 3. Dono me farq

| | Program | Process |
|---|---|---|
| **Kahan hota hai** | Disk (ROM, SSD) me | CPU me, running |
| **Halat** | Sirf save hai | Chal raha hai |
| **Misal** | Chrome ki file | Khula hua Chrome |

---

## Process ID

### 1. PID aur PPID

- **PID (Process ID):** har process ka **apna unique number**.
- **PPID (Parent Process ID):** us process ka number jis ne **is process ko start kiya**.
- *Misal:* Chrome ke andar chalne wali **WhatsApp app** ek alag process hoti hai.

---

## Processes Dekhna

### 1. ps aux

- **Chalti hui sari processes** ki list dikhata hai.
- *Misal:* `ps aux`

### 2. Pipe ( | )

- **Do commands ko ek command me** jodne k liye.
- Pehli command ka result **doosri command ko mil jata hai**.

### 3. ps aux | grep

- Chalti processes me se **sirf wo processes** dhoondta hai jo kisi word se match karein.
- *Misal:* `ps aux | grep ssh` yani **ssh k liye jo programs run ho rahe hain unhe dhoondo**.

### 4. htop

- Processes ko **colorful aur achi form** me dikhata hai.
- `ps aux` ke muqable me **zyada easy** hota hai parhna.
- *Misal:* `htop`

---

## Foreground aur Background Process

| | Foreground | Background |
|---|---|---|
| **Kahan** | **Screen par samne** chalta hai | **Peeche** chalta hai |
| **Nazar aata hai** | Haan | Nahi, nazar nahi aata |

---

## Process Kill Karna

### 1. kill

- Process ko **ID se band** karne k liye.
- *Misal:* `kill 5272`

### 2. kill -9

- Agar process **normal kill se band na ho** to usay **zabardasti (forcefully)** band karwate hain.
- *Misal:* `kill -9 5272`

### 3. killall -9

- Process ko **uske name se** forcefully band karta hai, ID ki zaroorat nahi.
- *Misal:* `killall -9 firefox`

---

## Service

### 1. Service kya hoti hai

- Aisi process jo **background me chalti rehti hai**, **hamari attention k bagair**.
- Ye **always running** form me hoti hai.
- *Misal:* WiFi, Bluetooth aur ssh jaise kaam peeche chalte rehte hain.

### 2. Program se Service tak

```text
Program  →  Process  →  Service
(file)      (running)    (hamesha running)
```

### 3. systemd

- **systemd** poore system ko **manage** karta hai.
- Ye services ko **start, stop aur monitor** karta hai.

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **Program** | SSD me pari hui file |
| **Process** | Chalta hua program (CPU me) |
| **PID / PPID** | Process ka number / uske parent ka number |
| **ps aux** | Chalti processes ki list |
| **\|** | Do commands ko jorna |
| **htop** | Colorful process viewer |
| **kill -9** | Zabardasti band karna |
| **Service** | Background me hamesha chalne wali process |
| **systemd** | Poore system ko manage karta hai |
