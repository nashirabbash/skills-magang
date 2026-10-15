---
name: magang-tekdok
description: Membuat proyek proposal atau laporan magang Teknologi Kedokteran ITS, mengisi naskahnya, atau memeriksa hasil PDF dari template LaTeX.
---

# Magang Teknologi Kedokteran ITS

Gunakan direktori kerja pengguna untuk proyek. Template tersedia di `template/` relatif terhadap lokasi SKILL.md yang terpasang; jangan menganggap direktori kerja saat ini sebagai lokasi skill.

## Mulai proyek

Periksa direktori tujuan. Jika proyek magang sudah ada, lanjutkan proyek tersebut. Jika belum, tunjukkan lokasi tujuan dan minta persetujuan sebelum menyalin isi `<direktori-skill>/template/.` ke direktori kosong. Jika tujuan berisi berkas lain, minta direktori kosong baru agar berkas pengguna tetap aman. Selesai saat `proposal_magang.tex`, `laporan_magang.tex`, `bab/`, dan `pustaka/variables.tex` tersedia di tujuan.

## Isi naskah

Tentukan dokumen dan bagian yang diminta pengguna, lalu baca sumber terkait. Identitas, pembimbing, instansi, dan periode magang ada di `pustaka/variables.tex`; bab di `bab/`; pustaka di `pustaka/pustaka.bib`. Proposal dan laporan memakai bab berbeda; sunting hanya naskah yang relevan. Biodata laporan mengambil isi dari `lainnya/lampiran-cv.tex`, sama seperti CV proposal. Gunakan data dan sumber pengguna; minta rincian yang belum tersedia, bukan mengarang kegiatan, hasil, atau referensi. Selesai saat seluruh bagian yang diminta terisi dan placeholder yang belum dapat dipastikan dinyatakan kepada pengguna.

## Periksa hasil

Dari direktori proyek, jalankan `latexmk -pdf -halt-on-error proposal_magang.tex` untuk proposal atau `latexmk -pdf -halt-on-error laporan_magang.tex` untuk laporan. Jika perubahan menyentuh sumber bersama, bangun keduanya. Periksa halaman PDF yang berubah secara visual, termasuk daftar isi bila judul atau urutan halaman berubah. Laporkan hasil build, lokasi PDF, dan bagian yang masih memerlukan data pengguna. Build berhasil tidak membuktikan kebenaran isi atau kesesuaian aturan institusi terbaru; periksa pedoman resmi dan arahan pembimbing sebelum pengumpulan.
