---
title: "AI selesai 2 hari, kenapa Sprintnya masih 2 minggu?"
description: "Parkinson's Law di era Agentic Engineering: ketika AI membuat coding jauh lebih cepat, bottleneck berpindah dari menulis software ke mengambil keputusan."
ref: ai-two-days-two-week-sprint
authors: [ahmad]
image: /assets/images/ai-selesai-2-hari/cover.jpg
---

*Pertama kali terbit di [daus95.com](https://daus95.com/2026/09/14/ai-bisa-selesai-dalam-2-hari-kenapa-kita-masih-pakai-sprint-2-minggu/), 14 September 2026.*

Ada sebuah hukum sederhana yang sudah dikenal sejak lama:

> “Work expands to fill the time available for its completion.”

Pekerjaan cenderung berkembang mengikuti waktu yang kita sediakan untuk menyelesaikannya.

Prinsip ini dikenal sebagai Parkinson’s Law, diperkenalkan oleh C. Northcote Parkinson pada tahun 1955.

Contohnya sederhana.

Bayangkan kita meminta seseorang membuat sebuah laporan dan memberikan waktu dua minggu. Sangat mungkin laporan tersebut baru benar-benar selesai mendekati akhir minggu kedua.

Tetapi jika sejak awal kita mengatakan laporan itu harus selesai besok sore, sering kali ternyata pekerjaan yang sama memang bisa diselesaikan dalam satu hari.

Bukan berarti orang tersebut sengaja bermalas-malasan. Yang terjadi biasanya lebih halus.

Ketika tersedia banyak waktu, kita cenderung melakukan lebih banyak diskusi, mempertimbangkan lebih banyak alternatif, melakukan revisi lebih banyak, menunggu lebih lama untuk mengambil keputusan, dan menambahkan pekerjaan-pekerjaan yang sebelumnya tidak dianggap perlu.

Akhirnya pekerjaan berkembang mengikuti waktu yang tersedia.

## Lalu datanglah AI

Parkinson’s Law menjadi semakin menarik ketika kita memasuki era AI, khususnya Agentic Engineering.

Dalam software engineering tradisional, sebuah fitur mungkin diperkirakan membutuhkan dua minggu untuk dibuat.

Karena itu kita membuat sprint dua minggu.

Tim melakukan planning, kemudian developer mulai coding. Setelah itu ada code review, testing, bug fixing, deployment, dan berbagai aktivitas lainnya.

Dua minggu kemudian fitur tersebut selesai.

Sekarang bayangkan pekerjaan yang sama dilakukan dengan bantuan AI coding agent.

AI dapat membaca spesifikasi, mempelajari codebase, membuat perubahan pada banyak file, menjalankan test, menemukan error, memperbaikinya, kemudian menjalankan test kembali.

Pekerjaan coding yang sebelumnya membutuhkan beberapa hari mungkin sekarang dapat dilakukan dalam beberapa jam.

Pertanyaannya:

Apakah fitur tersebut sekarang akan selesai dalam beberapa jam?

Belum tentu.

Bisa saja prosesnya tetap seperti ini:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/alur.jpg' | relative_url }}" alt="Alur kerja: AI selesai coding dalam 4 jam, lalu menunggu review, menunggu QA, menunggu meeting, masuk sprint berikutnya, dan baru selesai dua minggu kemudian. Total waktu sekitar 2 minggu meskipun coding-nya hanya 4 jam." width="2172" height="724" loading="lazy"></figure>

AI membuat pekerjaan menjadi jauh lebih cepat, tetapi sistem kerja di sekelilingnya masih menggunakan asumsi lama.

Akibatnya, produktivitas engineering mungkin meningkat 10 kali lipat, tetapi kecepatan organisasi menghasilkan sesuatu tidak meningkat 10 kali lipat.

Inilah Parkinson’s Law dalam bentuk baru.

## Masalahnya bukan lagi kecepatan coding

Selama puluhan tahun, salah satu bottleneck terbesar software development adalah kemampuan manusia menulis software.

Karena itu kita banyak mengukur capacity.

- Berapa developer yang kita punya?
- Berapa hari mereka bekerja?
- Berapa story point yang bisa diselesaikan dalam satu sprint?

Secara sederhana modelnya seperti ini:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/old.jpg' | relative_url }}" alt="Model lama: People (tim dengan berbagai peran) menentukan Capacity (jumlah orang, jam kerja, skill dan tools, infra dan lingkungan), yang menentukan Time (misalnya 2 minggu atau 1 sprint), yang menghasilkan Output (software yang selesai dan siap digunakan)." width="2172" height="724" loading="lazy"></figure>

Agentic Engineering mulai mengubah hubungan tersebut.

Jika AI mampu membantu melakukan coding, testing, debugging, dokumentasi, dan berbagai pekerjaan engineering lainnya dengan jauh lebih cepat, maka jumlah waktu manusia tidak lagi berhubungan langsung dengan jumlah software yang dapat dihasilkan.

Pertanyaan yang lebih penting berubah dari:

> “Berapa banyak pekerjaan yang bisa kita selesaikan dalam dua minggu?”

menjadi:

> “Apa yang harus selesai dan apa indikator itu dianggap selesai?”

Perbedaannya terlihat kecil, tetapi sebenarnya sangat fundamental.

## Dari Time-Box menjadi Outcome

Dalam pendekatan tradisional, kita sering memulai dari waktu.

Misalnya:

Kita punya sprint dua minggu. Apa yang bisa kita selesaikan?

Agentic Engineering memungkinkan kita membalik cara berpikir tersebut.

Kita mulai dari outcome.

Misalnya:

User harus sudah bisa melakukan pembayaran menggunakan QRIS.

Kemudian kita mendefinisikan secara jelas apa arti selesai; hal apa yang wajib dipenuhi dan hal apa yang opsional untuk dipenuhi.

Misalnya:

**Mandatory** — harus tersedia agar fitur pembayaran QRIS dapat diterima:

- sistem dapat menghasilkan QR code dengan nominal transaksi yang benar;
- pembayaran yang berhasil mengubah status transaksi menjadi Paid;
- pembayaran gagal atau kedaluwarsa tidak boleh mengubah transaksi menjadi Paid;
- transaksi yang sama tidak boleh tercatat dua kali.

Sementara itu ada hal-hal yang memberikan nilai tambah, tetapi tidak harus tersedia agar fungsi utamanya dapat digunakan.

**Optional:**

- halaman pembayaran mempunyai countdown timer;
- sistem mengirim email konfirmasi pembayaran;
- dashboard admin mempunyai grafik transaksi QRIS;

AI kemudian membantu tim menghasilkan implementasi dengan sangat cepat.

Di sinilah justru peran manusia menjadi semakin penting.

Setelah melihat hasilnya, manusia harus membuat keputusan:

Apakah implementasi mandatory yang dihasilkan sudah cukup baik untuk diterima?

Mungkin secara teknis semuanya sudah bekerja, tetapi pengalaman pengguna ternyata membingungkan. Tim kemudian memutuskan bahwa perbaikan tertentu ternyata harus menjadi mandatory.

Sebaliknya, mungkin ada requirement yang awalnya dianggap penting, tetapi setelah melihat aplikasi berjalan ternyata tidak lagi diperlukan.

Bisa juga selama proses muncul kebutuhan baru.

Misalnya setelah mencoba pembayaran QRIS, tim menyadari bahwa user perlu mengetahui berapa lama QR code tersebut berlaku. Countdown timer yang sebelumnya dianggap optional kemudian dinaikkan menjadi mandatory.

Atau situasi bisnis berubah sehingga prioritas ikut berubah.

Semua keputusan tersebut bukan keputusan AI.

Manusialah yang menentukan apa yang cukup baik, apa yang masih kurang, dan apa yang paling bernilai untuk dikerjakan berikutnya.

Ketika seluruh kebutuhan mandatory sudah dapat diterima, tim kembali membuat keputusan.

Apakah manfaat mengerjakan fitur-fitur optional cukup besar sehingga pekerjaan perlu dilanjutkan?

Atau lebih baik berhenti dan menggunakan kemampuan engineering yang tersedia untuk mengerjakan item lain dalam backlog yang memberikan nilai lebih besar?

Dengan cara berpikir ini, pekerjaan tidak otomatis terus berkembang hanya karena masih ada waktu yang tersedia.

Waktu tidak menentukan kapan pekerjaan selesai. Keputusan manusia mengenai kecukupan outcome yang menentukannya.

## Manusia menjadi Decision Maker

Di sinilah Agentic Engineering berbeda dari sekadar menggunakan AI untuk mempercepat coding.

AI membuat siklus implementasi menjadi sangat cepat.

Sesuatu dibuat, manusia melihat hasilnya, memberikan feedback, kemudian AI menghasilkan versi berikutnya.

Siklusnya bisa menjadi:

<figure class="fig fig-img"><img src="{{ '/assets/images/ai-selesai-2-hari/new.jpg' | relative_url }}" alt="Siklus baru: Build (AI mengerjakan implementasi berdasarkan spesifikasi), Review (manusia meninjau hasilnya), Decide (memutuskan apa yang sudah cukup, apa yang perlu diubah, dan prioritas berikutnya), Adjust (memberi arahan perubahan, memperjelas requirement, atau menyesuaikan prioritas), Build Again (AI mengerjakan versi berikutnya). Iterate sampai outcome tercapai." width="2172" height="724" loading="lazy"></figure>

Dulu satu siklus seperti ini mungkin membutuhkan beberapa hari atau bahkan beberapa minggu.

Dengan AI, siklus yang sama bisa terjadi beberapa kali dalam satu hari.

Akibatnya, pekerjaan manusia bergeser.

Semakin sedikit waktu yang dibutuhkan untuk menerjemahkan keputusan menjadi code, semakin besar proporsi waktu manusia yang digunakan untuk membuat keputusan.

Manusia harus terus menjawab pertanyaan seperti:

- Apakah hasil ini sudah cukup baik?
- Apakah ada sesuatu yang baru kita pelajari setelah melihat hasilnya?
- Apakah ada requirement baru yang sekarang harus menjadi mandatory?
- Apakah sesuatu yang sebelumnya mandatory ternyata tidak terlalu penting?
- Apakah prioritas bisnis berubah?
- Apakah fitur optional berikutnya masih layak dikerjakan?
- Atau apakah lebih baik berhenti sekarang dan pindah ke backlog yang lebih bernilai?

Jadi dalam Agentic Engineering, manusia bukan sekadar orang yang memberikan instruksi kepada AI.

Manusia adalah pengambil keputusan dalam sebuah engineering loop yang berjalan jauh lebih cepat.

## Definition of Done menjadi keputusan yang hidup

Karena itu, Definition of Done dalam Agentic Engineering tidak selalu merupakan checklist yang dibuat di awal lalu diikuti secara mekanis sampai selesai.

Kita tetap membutuhkan definisi awal mengenai mandatory dan optional.

Tetapi ketika hasil nyata mulai terlihat, pemahaman kita juga berkembang.

Kita mungkin menemukan sesuatu yang sebelumnya tidak terpikirkan.

Kita mungkin salah memperkirakan kebutuhan user.

Kita mungkin menemukan bahwa sebuah fitur yang terlihat penting ternyata tidak memberikan banyak nilai.

Atau sebaliknya, sesuatu yang awalnya dianggap tambahan ternyata sangat menentukan keberhasilan produk.

Karena itu Definition of Done menjadi sesuatu yang terus dievaluasi oleh manusia sepanjang proses.

Bukan berarti target boleh berubah tanpa kendali.

Justru perubahan tersebut harus merupakan keputusan sadar berdasarkan apa yang kita pelajari dari hasil kerja yang sudah tersedia.

AI memperpendek jarak antara ide dan implementasi.

Manusia menggunakan hasil implementasi tersebut untuk membuat keputusan berikutnya.

## Jangan membuat AI lebih cepat. Percepat keputusan.

Ada kesalahan yang mungkin akan banyak dilakukan perusahaan.

Mereka membeli AI coding tools dan berharap produktivitas meningkat drastis. Developer memang kemudian menghasilkan code jauh lebih cepat. Tetapi proses organisasinya tidak berubah.

- Hasil pekerjaan menunggu review.
- Keputusan menunggu meeting berikutnya.
- Perubahan requirement menunggu approval.
- QA menunggu jadwal.
- Stakeholder baru melihat hasil pekerjaan pada akhir sprint.

Dalam kondisi seperti ini, AI sudah bekerja dalam hitungan jam, tetapi organisasi masih mengambil keputusan dalam hitungan hari atau minggu.

Bottleneck berpindah.

Dulu bottleneck-nya mungkin kemampuan menghasilkan software. Dalam Agentic Engineering, bottleneck semakin bergeser menjadi kemampuan manusia mengevaluasi hasil dan mengambil keputusan.

Karena itu transformasi menuju Agentic Engineering tidak cukup dilakukan dengan memberikan AI coding assistant kepada developer.

Kita juga harus mendesain ulang cara manusia review, belajar, memutuskan, dan menentukan prioritas.

## Dari Utilization menuju Outcome

Ini juga mengubah cara kita melihat produktivitas.

Dalam organisasi tradisional, manajemen sering merasa tidak nyaman melihat engineer yang tidak sibuk. Karena itu manajemen berusaha meningkatkan utilization.

Semua orang harus mempunyai task. Semua capacity harus terisi.

Tetapi dalam sistem yang banyak menggunakan AI, ukuran tersebut semakin tidak relevan.

Bayangkan sebuah tim berhasil menghasilkan seluruh fungsi mandatory yang dibutuhkan hanya dalam dua hari, padahal sebelumnya pekerjaan tersebut diperkirakan membutuhkan dua minggu.

Tim kemudian menilai hasilnya dan menyimpulkan:

Ini sudah cukup baik untuk digunakan. Masih ada delapan hari.

Apakah kita harus terus memperbaiki fitur tersebut hanya karena sprint belum berakhir? Belum tentu.

Mungkin terdapat lima fitur optional yang masih bisa dibuat. Tetapi mungkin ada backlog lain yang memberikan manfaat bisnis jauh lebih besar. Maka keputusan yang lebih rasional adalah:

Stop. Ini sudah cukup. Pindah ke outcome berikutnya.

Di sinilah hubungan Agentic Engineering dengan Parkinson’s Law menjadi sangat jelas.

Parkinson’s Law mengatakan:

> Work expands to fill the time available.

Agentic Engineering seharusnya mendorong kita melakukan kebalikannya:

Jangan membiarkan waktu yang tersedia menentukan besarnya pekerjaan. Biarkan kecukupan outcome dan prioritas menentukan kapan kita berhenti dan berpindah ke pekerjaan berikutnya.

## Prinsip sederhana untuk Agentic Engineering

AI membuat kemampuan kita menghasilkan software meningkat sangat cepat.

Tetapi itu tidak berarti kita harus menghasilkan sebanyak mungkin software.

Justru kemampuan menghasilkan software yang semakin murah membuat kemampuan memilih apa yang layak dibuat menjadi semakin penting.

Karena itu pertanyaan utama Agentic Engineering bukan lagi:

> “Apa lagi yang masih bisa kita kerjakan?”

Tetapi:

> “Apakah yang kita hasilkan sudah cukup untuk mencapai tujuan?”

Jika belum, lanjutkan.

Jika selama proses kita belajar sesuatu yang baru, evaluasi kembali mandatory, optional, dan prioritasnya.

Jika sudah cukup, putuskan apakah tambahan pekerjaan masih memberikan nilai.

Dan jika tidak, berhenti.

Pindah ke outcome berikutnya yang lebih bernilai.

Pada akhirnya, AI mungkin membuat engineering berjalan jauh lebih cepat.

Tetapi manusialah yang harus menentukan ke mana kita berjalan, kapan sesuatu sudah cukup, dan kapan saatnya berhenti.
