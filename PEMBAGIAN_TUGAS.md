# Pembagian Tugas Tim CareerUp

**Kelompok 1** | UAS Software Development Fundamentals
**Deadline:** Kamis, 29 Oktober 2026, 12:00 WIB (target selesai internal: **Rabu, 28 Oktober malam**)

## Anggota

| Nama | GitHub | Peran utama |
|---|---|---|
| Abdullah Azzam Firdaus (ketua) | @username-azzam | Dokumen inti, kode, test, koordinasi |
| Azkiya Raihana | @username-azkiya | Use case diagram + 1 sequence diagram |
| Sahfria Elisabeth Yaleget | @username-Sahfria | 1 sequence diagram + bantu test case |

> Ganti `@username-...` dengan username GitHub asli sebelum dikumpulkan.

## Ringkasan Pembagian Deliverable

| Deliverable | Penanggung jawab | Reviewer |
|---|---|---|
| D1. Topik & Masalah | Azzam (selesai, tinggal commit) | Azkiya |
| D2. Modul | Azkiya | Sahfria |
| D3. Use Case Diagram | Azkiya | Azzam |
| D4. Sequence Diagram 1: Peserta menyelesaikan kuis | Azkiya | Sahfria |
| D4. Sequence Diagram 2: Mentor menilai tugas | Sahfria | Azkiya |
| D4. Sequence Diagram 3: Peserta mengklaim sertifikat | Azzam | Sahfria |
| D6. Test Case (skenario klaim sertifikat) |  Sahfria (isi 5 edge case) | Azkiya |
| D7. Fungsi `is_eligible_for_certificate` + unit test | Azzam | Sahfria |
| README.md + Activity Log | Semua (README: Azzam, log: masing-masing) | - |

**Catatan penting:** spec D4 mewajibkan **setiap anggota memegang 1 seq`uence diagram**, jadi 3 diagram dibagi ke 3 orang, bukan semuanya ke satu orang.

## Detail Tugas per Orang

### Azzam
1. Bikin repo, README kerangka, dan folder (`docs/`, `diagrams/`, `src/`, `tests/`).
2. Commit D1 (`docs/D1.md`).
3. Tulis D2 (modul + tabel ketergantungan modul).
4. Gambar sequence diagram 3 (klaim sertifikat, ada alur `alt`: syarat belum terpenuhi).
5. Tulis kerangka D6 dan 5 test case common.
6. Kode D7 + minimal 8 unit test + screenshot test lulus.
7. Review PR Azkiya dan Sahfria, ajarin cara resolve conflict.
8. Rapikan README (link semua deliverable, cara run test, bagian penggunaan AI).

### Azkiya (tugas ringan, fokus belajar Git)
1. Clone repo, buat branch `d3-azkiya`.
2. Tulis use case diagram dari kode PlantUML yang disediakan Azzam, lalu sesuaikan dengan kata-kata sendiri.
3. Export gambar (`.png`) dan simpan source (`.puml`).
4. Buka Pull Request D3.
5. Gambar sequence diagram 1 (peserta menyelesaikan kuis, `alt`: nilai kurang lalu ulang).
6. Review PR D1 dan D2 dengan komentar singkat.
7. Isi activity log sendiri setiap selesai kerja.

### Sahfria (tugas ringan, fokus belajar Git)
1. Clone repo, buat branch `d4-Sahfria`.
2. Gambar sequence diagram 2 (mentor menilai tugas, `alt`: tugas belum dikumpulkan).
3. Tulis alasan kenapa skenarionya penting (1-2 kalimat).
4. Tulis 5 edge case di D6 (lihat daftar ide di bawah), plus 3-5 kalimat penjelasan cara memilihnya.
5. Review PR D3 dan D7 dengan komentar singkat.
6. Isi activity log sendiri.

## Rencana Commit (min. 3 commit bermakna per orang)

| Orang | Commit 1 | Commit 2 | Commit 3 |
|---|---|---|---|
| Azzam | Setup repo + README kerangka | Tambah D1 dan D2 | Tambah kode D7 dan unit test |
| Azkiya | Tambah source use case diagram (`.puml`) | Tambah gambar D3 setelah review | Tambah sequence diagram 1 |
| Sahfria | Tambah sequence diagram 2 | Tambah 5 edge case di D6 | Revisi diagram setelah review |

Commit untuk activity log boleh ditambah, tapi **bukan pengganti** 3 commit di atas.

## Rencana Pull Request (min. 2, masing-masing di-review anggota lain)

| PR | Isi | Dibuat oleh | Reviewer |
|---|---|---|---|
| PR #1 | D3 Use Case Diagram | Azkiya | Azzam + Sahfria |
| PR #2 | Sequence Diagram 2 | Sahfria | Azzam + Azkiya |
| PR #3 (opsional) | D7 kode dan unit test | Azzam | Sahfria |

Aturan: **tidak ada yang merge PR miliknya sendiri sebelum direview** minimal 1 orang.

## Jadwal

| Tanggal | Target |
|---|---|
| Kamis 22 Okt | Repo dibuat, D1 di-commit, semua clone repo dan buat branch |
| Jumat 23 Okt | D2 selesai; Azkiya mulai D3; Sahfria mulai sequence diagram 2 |
| Sabtu 24 Okt | PR D3 dan PR sequence diagram 2 dibuka dan direview |
| Minggu 25 Okt | Sequence diagram 1 (Azkiya) dan 3 (Azzam); kerangka D6 |
| Senin 26 Okt | D6 lengkap (10 test case); D7 kode dan test selesai |
| Selasa 27 Okt | Perbaikan hasil review; README lengkap; screenshot test |
| Rabu 28 Okt | Cek akhir semua checklist, pastikan activity log cocok dengan commit |
| Kamis 29 Okt | Cadangan waktu. Submit link repo **sebelum 12:00 WIB** |

## Ide Edge Case untuk D6 (skenario klaim sertifikat)

Fungsi: `is_eligible_for_certificate(progress, avg_score)`, lulus jika progres 100% dan nilai rata-rata minimal 70.

- Nilai tepat 70 (batas bawah)
- Nilai 69,9 (sedikit di bawah batas)
- Progres 99% (hampir lengkap)
- Nilai negatif
- Nilai di atas 100
- Progres di atas 100%
- Input kosong atau `None`

## Aturan Tim

1. **Jangan commit langsung ke `main`.** Selalu pakai branch lalu Pull Request.
2. Nama branch: `d<nomor>-<nama>`, contoh `d3-azkiya`.
3. Pesan commit jelas, contoh: `Add use case diagram for CareerUp`. Jangan `update` atau `fix` saja.
4. Activity log (`ACTIVITY_LOG.md`) diisi **sendiri** dari akun GitHub masing-masing, **setiap selesai kerja**, dengan hash commit atau nomor PR sebagai bukti. Jangan menulis atas nama teman.
5. Tanggal di activity log harus sesuai tanggal kerja sebenarnya.
6. Semua anggota harus bisa menjelaskan **bagian mana pun** dari proyek jika ditanya dosen.
7. Jika memakai AI, catat di README alat apa dan untuk apa.

## Checklist Akhir

- [ ] D1 sampai D7 ada dan ter-link di README
- [ ] Diagram punya gambar (`.png`/`.svg`) **dan** file source
- [ ] Tiap anggota punya minimal 3 commit bermakna
- [ ] Minimal 2 PR yang direview anggota lain
- [ ] Setiap anggota memegang 1 sequence diagram
- [ ] Activity log lengkap dan cocok dengan riwayat commit
- [ ] README: nama app, anggota (nama + NIM + username GitHub), link deliverable, cara run test, bagian penggunaan AI
- [ ] Screenshot test lulus
- [ ] Repo publik (atau dosen sudah ditambahkan sebagai collaborator)
- [ ] Link repo disubmit sebelum Kamis 29 Okt, 12:00 WIB
