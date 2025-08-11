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

   
   
5. Buat OAuth Client ID dengan tipe **Desktop App**  
   Download file `client_secret.json`

6. Tambahkan akun Google kamu sebagai Test User di OAuth consent screen (jika project belum dipublish)

---

## Instalasi

```bash
git clone https://github.com/username/basmi-judol.git
cd basmi-judol
python3 -m venv env
source env/bin/activate  # Mac/Linux
.\env\Scripts\activate   # Windows
pip install -r requirements.txt
