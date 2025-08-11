# basmi-judol
Basmi Judol — Script Python untuk otomatis mendeteksi dan menghapus komentar spam judi, slot, dan togel di video YouTube menggunakan YouTube Data API v3. Dengan fitur autentikasi OAuth 2.0, kamu bisa membersihkan kolom komentar dari kata kunci spam secara efisien dan otomatis.

---

## Fitur

- Deteksi otomatis komentar spam berdasarkan kata kunci
- Hapus komentar spam secara otomatis menggunakan YouTube Data API
- Autentikasi OAuth 2.0 untuk akses channel YouTube
- Daftar kata kunci spam yang dapat disesuaikan

---

## Persiapan

1. Buat Google Cloud Project dan aktifkan YouTube Data API v3  
   [Aktifkan API di sini](https://console.cloud.google.com/apis/library/youtube.googleapis.com)
   <img width="1440" height="900" alt="Tangkapan Layar 2025-08-11 pukul 11 52 54" src="https://github.com/user-attachments/assets/85d69639-e59a-4fd5-bf79-90e8f117ce3b" />


3. Buat OAuth Client ID dengan tipe **Desktop App**  
   Download file `client_secret.json`

4. Tambahkan akun Google kamu sebagai Test User di OAuth consent screen (jika project belum dipublish)

---

## Instalasi

```bash
git clone https://github.com/username/basmi-judol.git
cd basmi-judol
python3 -m venv env
source env/bin/activate  # Mac/Linux
.\env\Scripts\activate   # Windows
pip install -r requirements.txt
