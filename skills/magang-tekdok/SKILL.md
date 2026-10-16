---
name: magang-tekdok
description: Membuat proyek, mengisi naskah, atau kompilasi PDF proposal/laporan magang Teknologi Kedokteran ITS.
---

# Magang Teknologi Kedokteran ITS

Template ada di `template/` relatif terhadap lokasi SKILL.md.

## Mulai proyek

Jika proyek belum ada, minta konfirmasi lalu salin `<direktori-skill>/template/.` ke direktori kosong tujuan. Selesai saat `proposal_magang.tex`, `laporan_magang.tex`, `bab/`, dan `pustaka/variables.tex` siap.

## Isi naskah

Petakan berkas: metadata di `pustaka/variables.tex`, bab di `bab/`, pustaka di `pustaka/pustaka.bib`, dan CV di `lainnya/lampiran-cv.tex`. Sunting hanya naskah relevan.

Gunakan `/scientific-writing` saat menyusun bab, mengelola sitasi, dan memastikan klaim bebas fabrikasi. Gunakan data pengguna; jangan mengarang isi. Selesai saat bagian target terisi dan placeholder tersisa dilaporkan.

## Periksa hasil

Jalankan `latexmk -pdf -halt-on-error proposal_magang.tex` atau `laporan_magang.tex` dari direktori proyek (bangun keduanya jika berkas bersama berubah). Periksa visual PDF hasil kompilasi. Laporkan status build, lokasi PDF, dan data yang belum lengkap.
