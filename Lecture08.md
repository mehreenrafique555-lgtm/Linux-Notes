# systemctl, Ports aur APT

---

## systemctl

### 1. systemctl kya hai

- **systemctl** system ka **manager** hai.
- Ye **sari services ko manage** karta hai.
- Is se hum service ko **start, stop aur restart** kar sakte hain.

### 2. Commands

| Command | Kaam |
|---|---|
| `systemctl status ssh` | Service **chal rahi hai ya nahi** ye dekhna |
| `sudo systemctl start ssh` | Service **start** karna |
| `sudo systemctl stop ssh` | Service **band** karna |
| `sudo systemctl restart ssh` | Service ko **dobara start** karna |

- *Misal:* ssh service ko start karne k liye `sudo systemctl start ssh`

---

## Ports

### 1. Port kya hota hai

- Port wo **raasta (gate)** hai jis se **data andar aata hai ya bahir jata hai**.
- *Misal:* **Charging pin** aur **handfree pin** bhi ports hain.
- Ports se **data copy, paste, chat aur audio/video** ka lena dena hota hai.
- Data **enter ya exit** karne k liye ports use hoti hain.
- Ek system me **64,000 se zyada ports** hoti hain (65,535).

### 2. Ports ki types

| Type | Matlab | Misal |
|---|---|---|
| **Hardware Port** | **Physical** port jo nazar aati hai | Handfree pin, charging pin |
| **Software Port** | Network par data ka **virtual** raasta | ssh, web ki ports |

### 3. Common software ports

| Service | Port |
|---|---|
| **ssh** | 22 |
| **http** (website) | 80 |
| **https** (secure website) | 443 |

---

## APT (Advanced Package Tool)

### 1. APT kya hai

- APT Linux ka **package manager** hai.
- Ye **software ki list aur unke versions ki info** rakhta hai.
- Software ko **dhoondta, download aur install** karta hai.
- Hum **APT ko command dete hain** aur APT **repository se baat** karta hai.

### 2. Repository

- **Repository** ek **online server** hai.
- Wahan **hazaron packaged software** rakhe hote hain.
- Hum command dete hain aur system **wahan se download** karke **install** kar deta hai.

### 3. Kaam kaise hota hai

```text
User Command  →  APT  →  Repository  →  Install
```

### 4. update vs upgrade

| Command | Kaam |
|---|---|
| `sudo apt update` | Software ki **list aur versions refresh** karta hai, yani dekhta hai ke **naya update** hai ya nahi |
| `sudo apt upgrade` | Software ko **naye version par** le jata hai |

- *Misal:* Pehle `sudo apt update`, phir `sudo apt upgrade`.

---

## Quick Revision

| Topic | Ek line me |
|---|---|
| **systemctl** | Services ko start, stop, restart karna |
| **status** | Service ki halat dekhna |
| **Port** | Data k andar aane ya jane ka raasta |
| **Hardware port** | Physical (charging, handfree pin) |
| **Software port** | Virtual (ssh 22, http 80, https 443) |
| **APT** | Linux ka package manager |
| **Repository** | Software ka online server |
| **update / upgrade** | List refresh / naya version |
