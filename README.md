# Praktikum-Search-Algorithm_Informed_Search

## Penjelasan Singkat Proyek
Dalam proyek ini, kita mengimplementasikan tiga algoritma pencarian untuk menemukan jalur optimal dalam sebuah graf berbobot:
1. Greedy Best-First Search (GBFS)
2. A Tree Search*
3. A Graph Search*

Ketika algoritma ini digunakan untuk mencari jalur dari simpul awal ke simpul tujuan berdasarkan heuristik dan biaya tertentu.

## Algoritma 
1. Greedy Best-First Search (GBFS)
   Algoritma ini memilih simpul yang memiliki nilai heuristik terendah tanpa mempertimbangkan biaya jalur yang telah ditempuh.
   GBFS menggunakan fungsi evaluasi: f(n) = h(n), dimana h(n) adalah nilai heuristik yang memperkirakan jarak ke tujuan.
   Cara Kerja GBFS:
   - Mulai dari simpul awal dan pilih simpul dengan nilai heuristik terendah.
   - Lanjutkan ke simpul berikutnya dengan heuristik terkecil hingga mencapai tujuan.
   - Tidak mempertimbangkan biaya dari simpul sebelumnya (bisa menyebabkan solusi yang kurang optimal).

2. A Tree Search*
   Algorima pencarian yang mempertimbangkan baik biaya jalur sejauh ini (g(n)) maupun perkiraan biaya ke tujuan (h(n)).
   Fungsinya: f(n) = g(n) + h(n), dimana g(n) adalah biaya dari simpul awal ke simpul saat ini, dan h(n) adalah perkiraan biaya dari simpul saat ini ke tujuan.
   Cara Kerja:
   - Mulai dari simpul awal, pilih simpul dengan nilai f(n) terkecil.
   - Kembangkan simpul yang belum dikunjungi berdasarkan prioritas nilai f(n).
   - Gunakan struktur Priority Queue untuk selalu memproses simpul dengan nilai terendah terlebih dahulu.
   - Tidak menyimpan daftar simpul yang sudah dikunjungi (bisa menyebabkan eksplorasi berulang).

3. A Graph Search*
   Algoritma nya sama seperti A* Tree Search, tetapi dengan tambahan mekanisme untuk menyimpan simpul yang telah dikunjungi agar tidak dikunjungi kembali jika ditemukan biaya yang lebih tinggi.
   Cara Kerja:
   - Menggunakan fungsi evaluasi yang sama dengan A* Tree Search: f(n) = g(n) + h(n)
   - Simpul yang sudah dikunjungi disimpan dalam daftar explored.
   - Jika simpul yang sudah dikunjungi ditemukan dengan biaya lebih rendah, simpul tersebut diperbarui dalam frontier.
   - Menghindari eksplorasi berulang yang terjadi pada A* Tree Search.
