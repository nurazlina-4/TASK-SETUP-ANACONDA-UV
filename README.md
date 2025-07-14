# Membangun Dunia Mini untuk Data Science: Panduan Set-Up Environment dengan Anaconda, Conda, dan UV 
---
##### Bayangin environment tuh kek kamar kosong, kamu bisa menata perabotan (packages) sesuka hati tanpa ngeberantakin seisi rumah (sistem utama)!
---
#### Kenapa kita butuh Virtual Environment?
##### Kek rumah susun yang punya banyak kamar, tiap proyek tuh punya ruang terpisah dengan ruang lain dan punya perabotan (packages) yang berbeda.
##### Virtual Environment memungkinkan kita untuk:
##### 1. Mengisolasi Proyek. Artinya tiap proyek punya dependensi dan versi paket yang spesifik tanpa mempengaruhi proyek lain.
##### 2. Mencegah konflik versi. Kita jadi terhindar dari masalah yang muncul ketika dua proyek perlu versi paket yang beda-beda.
##### 3. Reproduksibilitas: Ini tuh buat mastiin kalo kode dapat dijalanin dengan dependensi yang konsisten di berbagai sistem.
##### Dependensi tuh sederhananya adalah ketergantungan antara satu komponen dengan komponen lain biar berfungsi dengan baik.
##### Sampai sini, semoga sudah bisa dipahami ya, teman-teman.
---
### Nah, lanjut kita bahas tentang Anaconda, Conda, dan UV, apa ituuu?
##### Apa kamu sudah mulai membayangkan satu kawasan di Brazil yang terkenal itu? Hutan Amazon!!
##### Hutan Amazon emang habitat alami si anaconda, di mana mereka dapat ditemukan di perairan dangkal dan hutan yang lembap. Tapi, itu sejenis ular yaa.. 
##### Sedangkan yang mau kita omongin ini sejenis aplikasi (software), tapi lebih tepatnya "distribusi Python" (Python distribution). 
##### karena isinya nggak cuma aplikasi tunggal melainkan kumpulan tools dan library siap pakai untuk data science dan pemrograman Python. 
##### Bisa kita panggil sebagai "Paket Komplit"
#### Anaconda
##### Distribusi Python/R: Versi Python + ratusan library data science (Pandas, Matplotlib, Scikit-learn, dll.) yang sudah di-preinstall.
##### Package Manager: Punya conda untuk menginstall/mengupdate library tanpa pusing soal kompatibilitas.
##### Environment Manager: Bikin "kandang terpisah" (virtual environment) untuk tiap proyek agar library nggak tabrakan.
---
##### Conda 
##### Conda adalah manajer paket dan lingkungan yang disertakan dalam Anaconda. 
##### Analoginya kek kita mau bikin kue terus beli box kue lengkap (Python + library) + resep jitu (conda) biar adonannya nggak gagal.
---
##### UV
##### Kamu mau berpikir ini sejenis radiasi elektromagnetik dari matahari dan kamu harus pakai tabir surya. Nggak dong ya.
##### UV adalah alat manajemen paket dan lingkungan virtual Python yang super cepat dan modern.
##### Penerus pip dan virtualenv: Menggantikan pip dengan kecepatan 10-100x lebih cepat dalam instalasi paket.
##### Manajer Lingkungan Virtual: Bisa buat/mengelola virtual environment (seperti conda tapi lebih ringan).
##### Kompatibel dengan pip dan requirements.txt: Bisa pakai file dependensi yang sudah ada.
---
### Bagian 1: Instalasi Anaconda
---
#### 1. Download Installer Anaconda Apa
##### Buka https://www.anaconda.com/products/distribution - Pilih versi sesuai OS Anda (Windows/macOS/Linux) - Klik tombol Download
---
![image](https://github.com/nurazlina-4/TASK-SETUP-ANACONDA-UV/blob/main/anaconda%20awal.PNG)

##### Do's: Gulir ke bawah ya
##### Don’t: Jangan download di sumber yang abal-abal
---
#### 2. Jalankan Installer Anaconda Apa
##### Langkah-langkah: - Buka file installer yang sudah didownload - Ikuti wizard instalasi - Pilih opsi "Add Anaconda to PATH" (opsional)
---
![image](https://github.com/nurazlina-4/TASK-SETUP-ANACONDA-UV/blob/main/anaconda%20instal.PNG)
---
#### 3. Verifikasi Anaconda Terinstall dan Dapat Diakses Apa? 
##### Langkah-langkah:
##### 1. Buka terminal atau command prompt.
##### 2. Ketik perintah:
   ##### conda --version
##### 3. Jika muncul versi conda, instalasi sudah sukses.
##### Do's:
##### - Gunakan terminal baru
##### Don’t:
##### - Kalau ada yang error, cek lagi, apa masalahnya dan selesaikan 
##### 4. Konfigurasi Variabel Lingkungan PATH Conda dan Anaconda Apa? 
##### Langkah-langkah:
##### 1. Pada Windows, tambahkan direktori Anaconda dan Scripts ke PATH Environment Variable.
##### 2. Pada macOS/Linux, biasanya otomatis terpasang. Jika tidak, edit .bashrc atau .zshrc untuk menambah PATH
##### 3. Tekan Windows + R, ketik sysdm.cpl, tekan Enter.
##### 4. Pergi ke tab "Advanced", klik "Environment Variables".
##### 5. Pilih "Path" di "System variables", klik "Edit".
##### 6. Tambahkan (ganti NAMA_ANDA):
##### 7. Klik Ok
---
##### Bagian 2: Membuat UV Environment
##### 1. Buat Environment Baru
##### Langkah-langkah:
##### 1.	Pastikan lingkungan Conda tidak aktif (jalankan conda deactivate jika perlu).
##### 2.	Ketik: pip install uv
---
![image](https://github.com/nurazlina-4/TASK-SETUP-ANACONDA-UV/blob/main/kedua.PNG)
---
##### 3.	Output seperti Successfully installed uv-0.7.12 menunjukkan keberhasilan. Kalau udah seperti punyaku juga nunjukin bahwa itu udah suskses sebelumnya yaa. Jangan panik.
---
##### 4.	Catatan tentang folder ghost_intellixuv: Folder ghost_intellixuv akan dibuat di langkah berikutnya  menggunakan uv init. Perintah ini otomatis membuat folder jika belum ada, karena UV dirancang untuk menginisialisasi direktori proyek baru secara langsung. Anda tidak perlu membuat folder ini secara manual sebelum menjalankan uv init. Untuk memverifikasi folder setelah inisialisasi, ketik dir di CMD untuk melihat daftar direktori.
##### 2. Menginisialisasi Proyek UV
##### Langkah-langkah:
##### 1. Pastikan environment UV sudah aktif
##### 2. Ketik: uv init ghost_intellixuv
           ##### Cd ghost intellixuv
##### 3. Output menunjukkan proyek diinisialisasi di C:\Users\NAMA_ANDA\ghost_intellix\ghost_intellixuv.
##### Do's:
##### - pastikan nama folder yang tertulis sama
##### Don'ts:
##### - Jangan mengubah struktur folder setelah proyek berjalan
Install Paket yang Dibutuhkan
Langkah-langkah:
1.	Ketik: uv add pandas
---
![imag](https://github.com/nurazlina-4/TASK-SETUP-ANACONDA-UV/blob/main/ketiga.PNG)
Do's:
- Install hanya paket yang diperlukan
Don'ts:
- Jangan campur UV dan pip.
5. Menonaktifkan Lingkungan UV
Langkah-langkah:
1.	Ketik: .venv\Scripts\deactivate
2.	Prompt kembali ke C:\Users\NAMA_ANDA\ghost_intellix\ghost_intellixuv>.
Do's:
- Selalu deactivate ketika berpindah konteks.
---
![image](https://github.com/nurazlina-4/TASK-SETUP-ANACONDA-UV/blob/main/keempat.PNG)
Don'ts:
- Jangan tinggal aktif tanpa alasan.
Kesimpulan
•	Anaconda = "Paket komplit" untuk data science.
•	Conda = "Manajer serba bisa" untuk proyek kompleks.
•	UV = "Pemburu kecepatan" untuk efisiensi.
Dengan mengikuti panduan ini kamu sudah: 
Progress Anda Sudah Sempurna!
✅ Anaconda Terinstall → Python + Conda + library siap pakai.
✅ UV Environment Berjalan → Manajemen paket super cepat.


