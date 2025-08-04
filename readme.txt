🚀 Prompt Generate Backend

Backend untuk AI Prompt Generator berbasis FastAPI yang mendukung upload gambar dan menghasilkan prompt otomatis dalam Bahasa Indonesia dan Inggris.


---

🔧 Teknologi yang Digunakan

FastAPI

Uvicorn

Pillow



---

📁 Struktur Folder

.
├── main.py             # Entry point FastAPI
├── requirements.txt    # Dependency Python
└── .render.yaml        # Konfigurasi auto-deploy ke Render


---

📦 Instalasi Lokal

# 1. Clone repositori
https://github.com/Taba0368/prompt-generate-backend.git

# 2. Masuk ke folder
cd prompt-generate-backend

# 3. Buat virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Jalankan server lokal
uvicorn main:app --reload

Akses dokumentasi API di:

http://127.0.0.1:8000/docs


---

🌐 Deploy Otomatis ke Render

✅ Langkah:

1. Pastikan file .render.yaml sudah ada di root repo


2. Login ke https://render.com


3. Klik New > Web Service


4. Hubungkan ke repo GitHub ini


5. Render akan otomatis membaca konfigurasi dan memulai deploy



🌍 Contoh URL setelah deploy:

https://prompt-generate-backend.onrender.com


---

📤 Endpoint Utama

POST /generate-prompt

Menghasilkan prompt dari gambar dan deskripsi pengguna

Parameter:

image: file gambar (JPG/PNG)

language: id, en, su, jv, bt

conversation: (opsional) teks tambahan

details: (opsional) deskripsi lanjutan


Contoh cURL:

curl -X POST https://prompt-generate-backend.onrender.com/generate-prompt \
  -F image=@/path/to/image.jpg \
  -F language=id \
  -F conversation="Suasana musim gugur" \
  -F details="Gaya sinematik, cahaya lembut"

Response JSON:

{
  "prompt_id": "Deskripsi dalam Bahasa Indonesia",
  "prompt_en": "Description in English"
}


---

🙋‍♂ Kontribusi

Pull request dan saran sangat diterima. Jangan lupa 🌟 repo ini jika bermanfaat!


---

📩 Kontak

Buat oleh: @tabakarunia3