# 🌱 Graph-Greener

**GitHub Contribution Graph Commit Generator dengan GUI**  
Dibuat oleh: **KayyOnly**

---

## 📋 Deskripsi

Graph-Greener adalah tools berbasis GUI (Tkinter) yang membantu kamu mengisi **GitHub Contribution Graph** dengan commit history palsu yang terdistribusi secara acak dalam 1 tahun terakhir. Tools ini menggunakan `GIT_AUTHOR_DATE` dan `GIT_COMMITTER_DATE` untuk memanipulasi timestamp commit, sehingga commit akan muncul di tanggal yang diinginkan di contribution graph.

> ⚠️ **Peringatan**: Penggunaan tools ini mungkin melanggar [GitHub Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service). Gunakan dengan risiko tanggung sendiri. Disarankan hanya untuk repository pribadi / testing.

---

## 🛠️ Persyaratan

- **Python 3.7+**
- **Git** terinstall dan tersedia di PATH
- Repository Git lokal yang sudah diinisialisasi (`git init`)
- Remote repository sudah di-setup (untuk fitur push)

## 🚀 Cara Penggunaan

### Persiapan Repository

1. Buat repository baru di GitHub (private recommended)
2. Clone ke lokal:
   ```bash
   git clone https://github.com/username/your-repo.git
   cd your-repo
   ```
3. Buat file kosong (opsional):
   ```bash
   touch data.txt
   git add data.txt
   git commit -m "init"
   git push origin main
   ```

### Menggunakan GUI

1. **Jalankan aplikasi**:
   ```bash
   python main.py
   ```

2. **Isi form**:
   - **Number of Commits**: Jumlah commit yang ingin dibuat (default: 20)
   - **Repository Path**: Klik **Browse** untuk memilih folder repository Git kamu
   - **Target Filename**: File yang akan dimodifikasi setiap commit (default: `data.txt`)
   - **Commit Message**: Pesan commit (default: `graph-greener!`)
   - **Push to remote**: Centang jika ingin auto-push ke GitHub

3. **Klik "🚀 Generate Commits"**

4. **Tunggu proses selesai** — Progress bar dan log akan menampilkan status

5. **Cek GitHub** — Buka profil GitHub kamu, contribution graph akan update dalam beberapa menit

---

## ⚠️ Disclaimer

> Tools ini dibuat untuk **educational purposes** dan **personal testing**.
> 
> GitHub dapat mendeteksi aktivitas yang tidak wajar. Penggunaan berlebihan atau untuk tujuan menipu (misal: melamar kerja dengan contribution graph palsu) dapat berakibat:
> - Akun ditandai atau dibatasi
> - Repository dihapus
> - Suspensi akun
> 
> **Author (KayyOnly) tidak bertanggung jawab atas penyalahgunaan tools ini.**

---

## 📝 Changelog

### v1.0.0
- ✅ GUI Tkinter dengan dark theme
- ✅ Random commit date dalam 1 tahun terakhir
- ✅ Auto push ke remote
- ✅ Progress bar & activity log
- ✅ Validasi repository Git

---

## 👤 Author

**KayyOnly**

> "Green your graph, but keep it real. 💚"

---

## 📜 Lisensi

MIT License — Bebas digunakan dan dimodifikasi dengan risiko sendiri.

---

<p align="center">
  <sub>Made with 💚 by KayyOnly</sub>
</p>
