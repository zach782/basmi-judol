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

1. Buat Google Cloud Project
   [Buat di sini](https://console.cloud.google.com/)
   
2. Aktifkan YouTube Data API v3  
   [Aktifkan API di sini](https://console.cloud.google.com/apis/library/youtube.googleapis.com)
   <img width="1440" height="900" alt="Tangkapan Layar 2025-08-11 pukul 12 16 51" src="https://github.com/user-attachments/assets/3e441968-a3b8-44c5-bbce-fc85be0bb5f5" />
   
3. **Buat Credentials (OAuth Client ID)**  
   - Masuk ke halaman [Google Cloud Credentials](https://console.cloud.google.com/apis/credentials)
   - Klik tombol **"Create Credentials"** → pilih **"OAuth client ID"**

   Jika diminta untuk mengatur **OAuth Consent Screen**, lakukan hal berikut:
   - **User Type**: Pilih `External`
   - Isi kolom:
     - **App Name**
     - **User Support Email**
     - **Developer Contact Information**
   - Simpan dan lanjutkan (kolom lainnya bisa dikosongkan untuk keperluan testing)

   Setelah selesai setup consent screen:
   - Kembali ke halaman **Credentials**
   - Klik **Create Credentials** → **OAuth client ID**
   - **Application Type**: Pilih `Desktop App`
   - Beri nama, misalnya: `Basmi Judol`
   - Klik **Create**, lalu **Download JSON**
   <img width="1440" height="900" alt="Tangkapan Layar 2025-08-11 pukul 12 25 43" src="https://github.com/user-attachments/assets/a2318c52-f9a3-47e1-b82f-5b689830e668" />
   
4.  📁 Simpan file di direktori project
   Pastikan file client_secret.json ada di folder project yang sama dengan script Python kamu (misalnya main.py).
   <img width="1440" height="900" alt="Tangkapan Layar 2025-08-11 pukul 12 30 35" src="https://github.com/user-attachments/assets/301df1a6-db96-45d5-ab9e-6e701ff5f92a" />

5.  Referensikan Blok kode diatas ke nama file JSON yang kamu download dari Google Cloud setelah membuat OAuth Client ID.
   <img width="2688" height="454" alt="client" src="https://github.com/user-attachments/assets/b76dbd7b-2077-4384-a62c-d01823995468" />
   
6. Tambahkan akun Google kamu sebagai Test User di OAuth consent screen (jika project belum dipublish)
   <img width="1440" height="900" alt="Tangkapan Layar 2025-08-11 pukul 12 48 08" src="https://github.com/user-attachments/assets/b8acdc95-607b-4df5-a404-4ce6a4e7b084" />

7. Masukkan ID video YouTube yang ingin kamu moderasi di dalam file basmi_judol.ipynb, pada variabel VIDEO_ID.
   Contoh URL: https://www.youtube.com/watch?v=lGnUBl3pCF8
   → lGnUBl3pCF8 adalah ID videonya.
   <img width="1084" height="400" alt="idyt" src="https://github.com/user-attachments/assets/502e16ae-14fc-481f-9b89-f23be93453b9" />


---

## Instalasi

```bash
git clone https://github.com/zach782/basmi-komentar-judol-youtube.git
cd basmi-komentar-judol-youtube
python3 -m venv env
source env/bin/activate  # Mac/Linux
.\env\Scripts\activate   # Windows
pip install -r requirements.txt
