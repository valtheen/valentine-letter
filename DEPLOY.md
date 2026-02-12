# Share Valentine Letter via GitHub Pages

## 1. Buat repo baru di GitHub
- Buka https://github.com/new
- Repository name: `valentine-letter`
- Public, jangan centang README / .gitignore / license
- Create repository

## 2. Push dari laptop (sekali saja)
```bash
cd /Users/nauvalfatheen/Desktop/ValentineLetter
git remote add origin https://github.com/valtheen/valentine-letter.git
git branch -M main
git push -u origin main
```

## 3. Aktifkan GitHub Pages (penting — kalau 404, cek ini)
1. Buka **https://github.com/valtheen/valentine-letter**
2. Klik **Settings** (tab di atas)
3. Di sidebar kiri, klik **Pages**
4. Di "Build and deployment":
   - **Source:** pilih **Deploy from a branch**
   - **Branch:** pilih **main**, folder **/ (root)**
   - Klik **Save**
5. Tunggu 1–3 menit. Nanti muncul tulisan hijau: *"Your site is live at https://valtheen.github.io/valentine-letter/"*

**Kalau masih 404:** pastikan nama repo persis **valentine-letter** (huruf kecil, pakai strip). URL harus: `valtheen.github.io/valentine-letter/` (bukan ValentineLetter atau valentine_letter).

## 4. Terima jawaban kuis Lily ke email (opsional)
Agar jawaban dan pilihan Lily dari kuis terkirim ke **Fathinnauval@gmail.com**:

1. Buka **https://formspree.io** → Sign up / Login (gratis).
2. Klik **"New form"** → isi **Email** dengan **Fathinnauval@gmail.com** → Create.
3. Di halaman form, salin **Form ID** (bagian dari URL: `https://formspree.io/f/XXXXX` → Form ID = **XXXXX**).
4. Di project, buka **index.html**, cari baris:
   ```js
   var FORMSPREE_ID = 'YOUR_FORMSPREE_FORM_ID';
   ```
   Ganti `YOUR_FORMSPREE_FORM_ID` dengan Form ID yang kamu salin (contoh: `mzbqxyzab`).
5. Save, lalu push ke GitHub:
   ```bash
   git add index.html && git commit -m "Set Formspree ID for quiz email" && git push
   ```

Setelah Lily selesai menjawab 8 pertanyaan kuis, jawabannya otomatis terkirim ke **Fathinnauval@gmail.com** (subject: "💌 Jawaban Kuis Valentine - Lily").

**Cara cek respons / jawaban user (Lily):**
1. **Lewat email** — Setiap kali ada yang selesai kuis, Formspree kirim ke **Fathinnauval@gmail.com**. Cek inbox (dan folder Spam kalau belum dapat).
2. **Lewat dashboard Formspree** — Buka **https://formspree.io** → Login → klik form **valentine-letter** (atau form yang pakai ID `xnjbpnbe`). Di sana ada tab **"Submissions"**: semua jawaban kuis (tanggal, isi pesan, dll) muncul di situ. Bisa dibuka satu per satu untuk lihat detail.
3. **Notifikasi** — Di Formspree, pastikan notifikasi email untuk form ini **ON** (Settings form → Notifications) biar tiap submission tetap dikirim ke email kamu.

## 5. Link untuk dibagikan
- **https://valtheen.github.io/valentine-letter/**
- Kirim link ini ke Lily via WA; bisa dibuka di HP.
