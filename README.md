# Template magang Teknologi Kedokteran ITS

Template LaTeX untuk proposal dan laporan akhir magang, disertai [skill AI](skills/magang-tekdok/SKILL.md) yang membantu membuat proyek, mengisi naskah, dan memeriksa PDF. Berkas sumber ada di [`skills/magang-tekdok/template/`](skills/magang-tekdok/template/). Dokumen ini contoh kerja; sesuaikan dengan pedoman prodi dan arahan pembimbing sebelum dikumpulkan.

## Pratinjau

![Sampul proposal magang dengan data contoh](skills/magang-tekdok/template/sampul/preview-proposal.png)

Pratinjau sampul `proposal_magang.tex` memakai judul dan identitas contoh; isi PDF pengguna mengikuti data proyek masing-masing.

## Mulai cepat

Perlu distribusi TeX dengan `latexmk`, `pdflatex`, `biber`, `biblatex-apa`, dan `txfonts`. Dari root repositori ini, salin template ke direktori proyek yang **kosong**:

```bash
mkdir -p ~/magang-tekdok
cp -a skills/magang-tekdok/template/. ~/magang-tekdok/
cd ~/magang-tekdok
latexmk -pdf -halt-on-error proposal_magang.tex
latexmk -pdf -halt-on-error laporan_magang.tex
```

Hasilnya `proposal_magang.pdf` dan `laporan_magang.pdf` di direktori proyek. Di Overleaf, unggah isi `template/` dan pilih `proposal_magang.tex` atau `laporan_magang.tex` sebagai berkas utama.

## Isi template

- `proposal_magang.tex`: proposal; `laporan_magang.tex`: laporan akhir.
- `pustaka/variables.tex`: nama, NRP, judul, pembimbing, instansi, dan periode magang. Ganti nilai contoh sebelum digunakan.
- `bab/`: naskah; proposal dan laporan memakai bab yang berbeda. Baca pemanggilan `\input` pada berkas utama sebelum menyunting.
- `pustaka/pustaka.bib`: sumber referensi. Kedua dokumen menampilkan satu **contoh daftar pustaka APA** melalui `\nocite{rajpurkar2022ai}` di berkas utama; hapus perintah itu setelah memasukkan sitasi sendiri.
- `lainnya/lampiran-cv.tex`: isi CV proposal sekaligus biodata penulis laporan.

Untuk memperbarui PDF setelah mengubah isi, jalankan kembali perintah `latexmk` untuk dokumen yang berubah. Perubahan pada sumber bersama, seperti `pustaka/variables.tex`, perlu build **keduanya**. Periksa halaman hasil PDF dan daftar isi setelah perubahan tata letak.

## Menggunakan skill AI

[`magang-tekdok`](skills/magang-tekdok/SKILL.md) berisi alur untuk agen yang mendukung skill: minta agen membuat proyek magang di direktori kerja kosong, lalu berikan data dan sumber untuk bagian yang ingin ditulis. Agen harus meminta izin sebelum menyalin template. Contoh permintaan:

> /magang-tekdok Buat proyek magang di folder ini.
>
> /magang-tekdok Bantu isi Bab 1 proposal berdasarkan data dan sumber yang saya berikan.
>
> /magang-tekdok Periksa PDF laporan magang saya.

Tinjau sendiri fakta, sitasi, dan persyaratan institusi; build berhasil hanya membuktikan dokumen dapat dikompilasi.

## Contributors

- [@Aisarsyb](https://github.com/Aisarsyb)
