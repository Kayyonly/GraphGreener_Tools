🌱 Graph-Greener
GitHub Contribution Graph Commit Generator dengan GUI
Dibuat oleh: KayyOnly
📋 Deskripsi
Graph-Greener adalah tools berbasis GUI (Tkinter) yang membantu kamu mengisi GitHub Contribution Graph dengan commit history palsu yang terdistribusi secara acak dalam 1 tahun terakhir. Tools ini menggunakan GIT_AUTHOR_DATE dan GIT_COMMITTER_DATE untuk memanipulasi timestamp commit, sehingga commit akan muncul di tanggal yang diinginkan di contribution graph.
⚠️ Peringatan: Penggunaan tools ini mungkin melanggar GitHub Terms of Service. Gunakan dengan risiko tanggung sendiri. Disarankan hanya untuk repository pribadi / testing.
✨ Fitur
🖥️ GUI Modern Dark Theme — Tampilan elegan ala GitHub dark mode
📅 Random Date Distribution — Commit tersebar acak dalam 365 hari terakhir
📁 Browse Folder — Pilih repository dengan file picker
📊 Progress Bar Real-time — Pantau proses pembuatan commit
📝 Activity Log — Lihat status setiap commit (success/fail)
🚀 Auto Push — Opsi push otomatis ke remote setelah selesai
⚡ Non-blocking UI — Proses berjalan di background thread
🛡️ Validasi — Cek otomatis apakah folder adalah repository Git yang valid
🖥️ Screenshot Konsep
plain
Copy
┌─────────────────────────────────────────────┐
│  🌱 Graph-Greener                           │
│  GitHub Contribution Graph Commit Generator  │
│  by KayyOnly                                │
├─────────────────────────────────────────────┤
│  Number of Commits: [20        ]            │
│  Repository Path:   [/path/to/repo] [Browse]│
│  Target Filename:   [data.txt   ]            │
│  Commit Message:    [graph-greener!]         │
│  [✓] Push to remote after committing        │
├─────────────────────────────────────────────┤
│  [🚀 Generate Commits] [🧹 Clear] [❌ Exit] │
│  [===================>    ] 15/20...         │
├─────────────────────────────────────────────┤
│  Activity Log:                              │
│  [1/20] ✅ 2025-08-14 09:23:17              │
│  [2/20] ✅ 2025-03-02 14:55:42              │
│  ...                                        │
├─────────────────────────────────────────────┤
│            Made with 💚 by KayyOnly         │
└─────────────────────────────────────────────┘
🛠️ Persyaratan
Python 3.7+
Git terinstall dan tersedia di PATH
Repository Git lokal yang sudah diinisialisasi (git init)
Remote repository sudah di-setup (untuk fitur push)
📦 Instalasi
1. Clone atau Download
bash
Copy
git clone https://github.com/username/graph-greener.git
cd graph-greener
Atau download file graph_greener_gui.py langsung.
2. Jalankan
bash
Copy
python graph_greener_gui.py
Tidak perlu install dependencies tambahan karena hanya menggunakan:
tkinter (built-in Python)
subprocess, os, random, datetime (standard library)
🚀 Cara Penggunaan
Persiapan Repository
Buat repository baru di GitHub (private recommended)
Clone ke lokal:
bash
Copy
git clone https://github.com/username/your-repo.git
cd your-repo
Buat file kosong (opsional):
bash
Copy
touch data.txt
git add data.txt
git commit -m "init"
git push origin main
Menggunakan GUI
Jalankan aplikasi:
bash
Copy
python graph_greener_gui.py
Isi form:
Number of Commits: Jumlah commit yang ingin dibuat (default: 20)
Repository Path: Klik Browse untuk memilih folder repository Git kamu
Target Filename: File yang akan dimodifikasi setiap commit (default: data.txt)
Commit Message: Pesan commit (default: graph-greener!)
Push to remote: Centang jika ingin auto-push ke GitHub
Klik "🚀 Generate Commits"
Tunggu proses selesai — Progress bar dan log akan menampilkan status
Cek GitHub — Buka profil GitHub kamu, contribution graph akan update dalam beberapa menit
⚙️ Konfigurasi Lanjutan
Mengubah Default Value
Edit bagian berikut di kode jika ingin mengubah default:
Python
Copy
self.commits_var = tk.IntVar(value=20)        # Default commits
self.filename_var = tk.StringVar(value="data.txt")  # Default file
self.message_var = tk.StringVar(value="graph-greener!")  # Default message
Custom Date Range
Saat ini tools menggunakan distribusi acak dalam 365 hari terakhir. Untuk mengubah range, edit method random_date_in_last_year():
Python
Copy
def random_date_custom(self):
    start = datetime(2025, 1, 1)   # Tanggal mulai
    end = datetime(2025, 12, 31)   # Tanggal akhir
    delta = end - start
    return start + timedelta(seconds=random.randint(0, int(delta.total_seconds())))
🐞 Troubleshooting
Table
Masalah	Solusi
Directory is not a git repository	Pastikan folder memiliki subfolder .git. Jalankan git init jika belum.
Push failed	Cek remote URL dengan git remote -v. Pastikan autentikasi Git sudah setup (SSH key atau Personal Access Token).
Permission denied	Pastikan kamu punya write access ke repository.
GUI tidak muncul	Pastikan Python diinstall dengan Tcl/Tk support. Di Linux: sudo apt-get install python3-tk
Commit tidak muncul di graph	GitHub butuh waktu beberapa menit. Pastikan email Git (git config user.email) cocok dengan email akun GitHub.
📁 Struktur File
plain
Copy
graph-greener/
├── graph_greener_gui.py    # File utama (GUI)
├── README.md               # Dokumentasi ini
└── .gitignore              # (Opsional) Ignore data.txt
⚠️ Disclaimer
Tools ini dibuat untuk educational purposes dan personal testing.
GitHub dapat mendeteksi aktivitas yang tidak wajar. Penggunaan berlebihan atau untuk tujuan menipu (misal: melamar kerja dengan contribution graph palsu) dapat berakibat:
Akun ditandai atau dibatasi
Repository dihapus
Suspensi akun
Author (KayyOnly) tidak bertanggung jawab atas penyalahgunaan tools ini.
📝 Changelog
v1.0.0
✅ GUI Tkinter dengan dark theme
✅ Random commit date dalam 1 tahun terakhir
✅ Auto push ke remote
✅ Progress bar & activity log
✅ Validasi repository Git
👤 Author
KayyOnly
"Green your graph, but keep it real. 💚"
📜 Lisensi
MIT License — Bebas digunakan dan dimodifikasi dengan risiko sendiri.
<p align="center">
  <sub>Made with 💚 by KayyOnly</sub>
</p>
