# Week 1 – Hari 1: Setup Lingkungan Python untuk Data & AI

Tujuan hari ini:
- Menjalankan **Python 3.11** dalam **virtual environment (venv)**.
- Memasang **JupyterLab**, **NumPy**, **Pandas**, **Matplotlib**.
- Menjalankan notebook **`notebooks/00_check_env.ipynb`** untuk sanity‑check.

> Hasil akhir: kamu bisa membuka JupyterLab di `http://localhost:8888`, mengimpor NumPy/Pandas/Matplotlib tanpa error, dan melihat sebuah plot sederhana.


---

## 1) Buat Virtual Environment (venv)
Di folder proyek buat venv jika belum ada:
```bash
python -m venv .venv
```
Aktifkan:
- Linux/WSL/macOS
  ```bash
  source .venv/bin/activate
  ```
- Windows PowerShell
  ```powershell
  .\.venv\Scripts\Activate.ps1
  ```
Cek versi:
```bash
python -V
pip -V
```

---

## 2) Install Paket & Simpan `requirements.txt`
```bash
python -m pip install --upgrade pip
pip install jupyterlab numpy pandas matplotlib
pip freeze > requirements.txt
```

---

## 3) Jalankan JupyterLab
```bash
jupyter lab
```
Buka URL yang muncul (umumnya `http://localhost:8888`).

---

## 4) Jalankan Notebook Cek Lingkungan
1. Salin file **`00_check_env.ipynb`** ke folder `notebooks/`.
2. Buka notebook tersebut di JupyterLab.
3. Jalankan sel dari atas ke bawah.
4. Pastikan:
   - Versi Python/NumPy/Pandas/Matplotlib tercetak.
   - Operasi NumPy dan `groupby` Pandas berjalan.
   - Plot Matplotlib tampil.

> Jika semua OK, buat **screenshot** hasil plot dan simpan ke `reports/figures/` sebagai bukti.


---

## Troubleshooting Singkat
- **Windows: “running scripts is disabled on this system”** saat `Activate.ps1`  
  Buka PowerShell **as Administrator** dan jalankan:
  ```powershell
  Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
  ```
- **pyenv gagal install Python** (Linux/WSL): pastikan paket build di langkah 1A terpasang lengkap.
- **`jupyter` tidak dikenali**: pastikan venv aktif atau jalankan `python -m jupyter lab`.

---

