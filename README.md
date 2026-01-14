
# 🌴 SaWiTOS — Nugra21  Terminal OS 

SaWiTOS adalah **Fake Linux Terminal OS berbasis Python (CLI)**  
yang meniru pengalaman menggunakan Linux Terminal dengan **command custom**,  
**mode user & mode pejabat (administrator)**, serta **data yang tersimpan permanen**.

> ⚠️ Catatan:  
> SaWiTOS **BUKAN sistem operasi asli**, melainkan **simulasi terminal Linux**  
> untuk pembelajaran, showcase, dan fun project.

---

## 📌 Informasi Umum

| Item | Detail |
|----|------|
| Nama OS | **SaWiTOS** |
| Versi | v1.0 |
| Tipe | Fake Linux / CLI Simulator |
| Bahasa | Python |
| Creator | **Nugra21** |
| Mode | User & Pejabat (Admin) |
| Data | Persistent (JSON) |

---

## ✨ Fitur Utama

- 🎨 Terminal berwarna (tidak monokrom)
- 🖥️ Tampilan mirip Linux terminal
- 👤 Multi-user system
- 🔐 Mode User & Mode Pejabat
- 🔑 sudo / su
- 💾 Data tidak hilang saat keluar
- 📊 Informasi sistem lengkap
- 📂 Manajemen file & folder (fake)
- 🧠 Command custom & Linux-like
- 🧹 clear, exit, reboot
- 🔄 Modular (multi file)

---

## 📁 Struktur Project

```

sawitos/
│
├─ main.py                # Entry point
├─ core/
│   ├─ terminal.py        # UI, prompt, banner
│   ├─ commands.py        # Semua command
│   ├─ system.py          # Info OS
│   └─ auth.py            # User & mode pejabat
│
├─ data/
│   ├─ system.json        # Data sistem
│   └─ users.json         # Data user
│
├─ requirements.txt
├─ README.md
└─ LICENSE

````

---

## ⚙️ Instalasi & Menjalankan SaWiTOS

### 1️⃣ Clone Repository
```bash
git clone https://github.com/nugra21/sawitos.git
cd sawitos
````

### 2️⃣ Install Dependency

```bash
pip install -r requirements.txt
```

### 3️⃣ Jalankan OS

```bash
python main.py
```

---

## 🖥️ Tampilan Prompt

| Mode    | Prompt                           |
| ------- | -------------------------------- |
| User    | `Nugra21@SaWiTOS:/home $`        |
| Pejabat | `Nugra21@SaWiTOS:/root #PEJABAT` |

---

## 👤 Sistem User & Mode

### 🔓 Mode User

* Akses terbatas
* Tidak bisa mengubah sistem
* Default saat login

### 🔐 Mode Pejabat (Administrator)

* Akses penuh
* Bisa kelola user & sistem
* Mirip `root` di Linux

Masuk mode pejabat:

```bash
sudo su
```

Keluar mode pejabat:

```bash
exit
```

---


## 📜 Daftar Command SaWiTOS (Custom)

SaWiTOS menggunakan **command berbahasa Indonesia** dengan tema **perkebunan / sawit** 🌴
Semua command di bawah adalah **COMMAND RESMI SaWiTOS**.

---

## 📂 Command Navigasi & Direktori

| Command          | Fungsi                                |
| ---------------- | ------------------------------------- |
| `LIHAT`          | Menampilkan isi direktori saat ini    |
| `MASUK <folder>` | Masuk ke direktori                    |
| `MUNDUR`         | Kembali ke direktori sebelumnya       |
| `POSISI`         | Menampilkan path direktori aktif      |
| `BUKA <folder>`  | Membuat folder baru                   |
| `BAKAR <folder>` | Menghapus folder (**MODE PEJABAT**)   |
| `KEBUN`          | Menampilkan struktur direktori (tree) |

---

## 📄 Command File

| Command               | Fungsi              |
| --------------------- | ------------------- |
| `TANAM <file>`        | Membuat file kosong |
| `PANEN <file>`        | Membaca isi file    |
| `RAWAT <file>`        | Edit isi file       |
| `TEBANG <file>`       | Menghapus file      |
| `CANGKOK <src> <dst>` | Copy file           |
| `PINDAH <src> <dst>`  | Memindahkan file    |
| `GANTI <lama> <baru>` | Rename file         |

---

## 🧹 Command Terminal

| Command     | Fungsi                      |
| ----------- | --------------------------- |
| `BERSIHKAN` | Membersihkan layar terminal |
| `CLS`       | Alias dari `BERSIHKAN`      |
| `WAKTU`     | Menampilkan waktu & tanggal |

---

## 👤 Command User & Akses

| Command     | Fungsi                                 |
| ----------- | -------------------------------------- |
| `SIAPA`     | Menampilkan user aktif                 |
| `SU <user>` | Ganti user                             |
| `SUDO`      | Masuk **MODE PEJABAT (Administrator)** |

📌 **MODE PEJABAT** diperlukan untuk:

* Menghapus folder (`BAKAR`)
* Operasi sistem tertentu

---

## 🖥️ Command Sistem

| Command      | Fungsi                     |
| ------------ | -------------------------- |
| `INFO_SAWIT` | Informasi sistem SaWiTOS   |
| `NEOFETCH`   | Informasi sistem ala Linux |
| `BANTUAN`    | Menampilkan semua command  |
| `SAWIT`      | Easter egg rahasia 🌴      |

---

## 🚪 Command Keluar

| Command  | Fungsi                    |
| -------- | ------------------------- |
| `EXIT`   | Keluar dari SaWiTOS       |
| `PULANG` | Alias keluar dari SaWiTOS |

---

## 🧪 Contoh Penggunaan

```bash
LIHAT
MASUK dokumen
TANAM catatan.txt
RAWAT catatan.txt
PANEN catatan.txt
SUDO
BAKAR dokumen
PULANG
```

---

## 🔐 Catatan Penting

* Command **tidak case-sensitive**
  (`lihat`, `LIHAT`, `Lihat` → sama)
* Data **tersimpan permanen** (JSON)
* Mode **PEJABAT ≈ root Linux**

---

## 🌴 Filosofi Command SaWiTOS

| Konsep | Arti               |
| ------ | ------------------ |
| TANAM  | Buat file          |
| PANEN  | Baca file          |
| RAWAT  | Edit file          |
| TEBANG | Hapus file         |
| BAKAR  | Hapus folder       |
| KEBUN  | Struktur direktori |

---
## 💾 Penyimpanan Data

Semua data disimpan di file JSON:

| File          | Fungsi    |
| ------------- | --------- |
| `system.json` | Info OS   |
| `users.json`  | Data user |

✔️ Data tidak hilang
✔️ Bisa diedit manual
✔️ Bisa dikembangkan

---

## 🎨 Customisasi

* Edit **warna & UI** → `core/terminal.py`
* Tambah command → `core/commands.py`
* Tambah info OS → `data/system.json`

---

## 🚀 Rencana Upgrade

* 🔐 Login screen
* 🧠 Fake process manager
* 🌐 Network command
* 🎮 Mini game terminal
* 🐧 Bash script emulator

---

## 📜 Lisensi

MIT License
Bebas digunakan, dimodifikasi, dan dibagikan.

---

## 👑 Author

**Nugra21**
SaWiTOS Fake Linux Terminal OS
Made with ☕ & 🌴

> “Bukan Linux sungguhan, tapi rasanya Linux 😎”
