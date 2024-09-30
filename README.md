# Laporan Tugas Git

## Deskripsi Tugas

Tugas ini mencakup implementasi penggunaan Git dengan skenario Fast-Forward dan Three-Way Merge.

## Proses yang Dilakukan

1. Membuat branch Parent dan Child.
2. Melakukan Fast-Forward Merge.
3. Menyelesaikan konflik dan melakukan Pull Request.

## Screenshots

[Screenshot 1](https://drive.google.com/file/d/1R8aUdhm38Ss9ihg4fiOwSO9ubz2DmP8p/view?usp=sharing)

Pada sesi Git tersebut, dilakukan serangkaian langkah untuk menangani masalah LF/CRLF yang biasa terjadi saat bekerja lintas platform, terutama antara Linux dan Windows. Pertama, sebuah file bernama `ParentWahyu.md` dibuat dengan menambahkan teks "Ini adalah branch ParentWahyu". Setelah file tersebut ditambahkan ke staging area menggunakan perintah `git add .`, muncul peringatan bahwa Git akan mengganti karakter akhir baris dari LF ke CRLF pada file `ParentWahyu.md` saat file tersebut dimodifikasi di lingkungan Windows.

Untuk mengatasi masalah ini, file `ParentWahyu.md` dikeluarkan dari staging area menggunakan perintah `git rm --cached`, yang hanya menghapusnya dari staging tanpa menghapus file itu sendiri dari direktori kerja. Setelah itu, file tersebut ditambahkan kembali ke staging menggunakan `git add`. Kemudian, commit dilakukan dengan pesan "Menghapus dan menambahkan kembali ParentWahyu.md untuk mengatasi masalah LF/CRLF". Setelah commit selesai, Git menampilkan informasi bahwa satu file telah diubah dengan satu baris tambahan dan menegaskan bahwa file tersebut memiliki izin file `100644`, yang berarti file tersebut dapat dibaca dan ditulis oleh pemilik, serta dapat dibaca oleh grup dan pengguna lain.

Proses ini menunjukkan bagaimana Git menangani konversi baris akhir otomatis serta bagaimana pengguna bisa melakukan langkah-langkah untuk memperbaiki masalah ini.

[Screenshot 2](https://drive.google.com/file/d/18H3iW7R69uuSSHEjR_GCnxHxHBXkXhBt/view?usp=sharing)

Gambar tersebut menunjukkan alur kerja di Git untuk membuat dan bekerja di cabang baru. Berikut adalah penjelasannya:

Membuat Cabang Baru: Perintah git checkout -b ChildWahyu digunakan untuk membuat cabang baru bernama "ChildWahyu" dan langsung beralih ke cabang tersebut. Ini dilakukan agar perubahan yang dilakukan selanjutnya tidak mempengaruhi cabang utama (master).

Menambahkan File Baru: Pengguna membuat file baru bernama ChildWahyu.md dengan perintah echo "Ini adalah branch ChildWahyu" > ChildWahyu.md, yang menulis teks ke dalam file tersebut.

Menambahkan File ke Staging Area: Perintah git add ChildWahyu.md digunakan untuk menambahkan file ChildWahyu.md ke dalam staging area, yaitu tahap sebelum file siap untuk di-commit.

Commit Perubahan: Setelah file berada di staging area, pengguna menjalankan perintah git commit -m "Menambahkan ChildWahyu.md di ChildWahyu". Ini untuk menyimpan perubahan tersebut ke dalam repository Git dengan pesan commit yang menjelaskan perubahan, yaitu "Menambahkan ChildWahyu.md di ChildWahyu".

Setelah ini, perubahan disimpan secara permanen di cabang "ChildWahyu" tanpa memengaruhi cabang utama.

[Screenshot 3](https://drive.google.com/file/d/1CnqD1NyrGAMCNUukSi4E0mzPhT8wsJPW/view?usp=sharing)

Gambar tersebut menunjukkan langkah-langkah tambahan dalam bekerja dengan cabang di Git. Berikut penjelasan mengenai perintah yang digunakan:

Membuat Cabang Baru: Perintah git checkout -b ParentWahyu digunakan untuk membuat cabang baru bernama "ParentWahyu" dan langsung beralih ke cabang tersebut. Ini mirip dengan langkah sebelumnya ketika pengguna membuat cabang "ChildWahyu". Cabang "ParentWahyu" dibuat dari cabang yang aktif saat itu, yaitu "ChildWahyu".

Beralih ke Cabang Lain: Perintah git checkout ChildWahyu digunakan untuk kembali beralih ke cabang "ChildWahyu". Ini memungkinkan pengguna untuk bekerja kembali di cabang "ChildWahyu" setelah sebelumnya berada di cabang "ParentWahyu".

Dengan perintah-perintah ini, pengguna membuat cabang "ParentWahyu" dari "ChildWahyu", lalu kembali beralih ke cabang "ChildWahyu" untuk melanjutkan pekerjaan di sana. Hal ini umum dilakukan ketika pengguna ingin menjaga perubahan di cabang yang berbeda tanpa saling mempengaruhi.

[Screenshot 4](https://drive.google.com/file/d/1Y1_f5jn_oyyA4DQHjhe0wpuWcGKcFin7/view?usp=sharing)

Gambar ini menunjukkan proses penggabungan (merge) cabang di Git. Berikut penjelasan dari perintah yang digunakan:

1. Merge Cabang: Perintah `git merge ChildWahyu` dijalankan dari cabang "ParentWahyu". Tujuan dari perintah ini adalah untuk menggabungkan perubahan yang telah dilakukan di cabang "ChildWahyu" ke dalam cabang "ParentWahyu". Proses ini menggunakan mode _fast-forward_, yang berarti tidak ada konflik, dan perubahan dari cabang "ChildWahyu" dapat langsung diterapkan ke "ParentWahyu" tanpa perlu membuat commit merge baru.

2. Perubahan yang Terjadi: Output menunjukkan bahwa satu file, `ChildWahyu.md`, mengalami perubahan dengan 1 penambahan (+) dan 1 penghapusan (-). Ini menunjukkan ada satu baris yang diubah di dalam file tersebut.

Proses ini memperbarui cabang "ParentWahyu" dengan semua perubahan yang dilakukan di cabang "ChildWahyu", menyinkronkan keduanya.

[Screenshot 5](https://drive.google.com/file/d/1i454XQGfnZQSHz1wypgBSyPclZQCxSiD/view?usp=sharing)

Gambar ini menunjukkan proses pengunggahan (push) cabang (branch) baru bernama "ParentWahyu" ke repositori GitHub menggunakan Git dari command line. Berikut adalah penjelasan langkah-langkah yang terjadi:

1. git push origin ParentWahyu: Perintah ini digunakan untuk mendorong (push) cabang "ParentWahyu" ke repositori jarak jauh (remote repository) di GitHub.
2. Enumerating objects: Git menghitung objek-objek yang akan dikirim ke repositori jarak jauh. Di sini terdapat 16 objek yang dihitung.

3. Compressing and writing objects: Proses ini adalah tahap kompresi objek-objek yang akan diunggah dan penulisan data ke server GitHub. Semua objek berhasil dikompresi dan diunggah.

4. Delta compression: Git menggunakan kompresi delta untuk menghemat ruang dan mempercepat pengunggahan dengan hanya mengirim perubahan (delta) dari data yang ada.

5. Resolving deltas: Proses ini menyelesaikan perubahan delta untuk memastikan bahwa semua perubahan diterapkan dengan benar di server GitHub.

6. Pull request suggestion: Setelah pengunggahan selesai, GitHub memberikan saran untuk membuat pull request agar cabang baru ini dapat digabungkan (merged) ke cabang utama. Ada tautan yang disediakan untuk memudahkan pembuatan pull request.

7. Branch tracking: Pada bagian akhir, ditunjukkan bahwa cabang "ParentWahyu" sekarang terlacak (tracked) di repositori jarak jauh (remote).

Ini adalah tahapan standar untuk mengunggah cabang baru ke repositori GitHub dan biasanya diikuti dengan pembuatan pull request jika Anda ingin menggabungkan perubahan dari cabang tersebut ke cabang lain, misalnya cabang utama (main/master).

[Screenshot 6](https://drive.google.com/file/d/1WLFzfzEGfLRcP2lqnjoyqK3I4p93EJaj/view?usp=sharing)

Gambar ini menunjukkan langkah-langkah dalam proses pengeditan, penambahan, dan komit file baru ke dalam repositori Git menggunakan command line. Berikut adalah penjelasan dari setiap langkah:

1. echo "Perubahan di ParentWahyu" >> ParentWahyu.md: Perintah ini digunakan untuk menambahkan teks "Perubahan di ParentWahyu" ke dalam file bernama `ParentWahyu.md`. Jika file ini belum ada, perintah ini akan membuat file baru.

2. git add ParentWahyu: Di sini, pengguna mencoba menambahkan file `ParentWahyu` ke staging area Git, tetapi terdapat kesalahan karena tidak ada file dengan nama `ParentWahyu`. Itu sebabnya Git menampilkan pesan error _"fatal: pathspec 'ParentWahyu' did not match any files"_.

3. git add ParentWahyu.md: Perintah ini digunakan untuk menambahkan file `ParentWahyu.md` (yang sudah benar sesuai nama file) ke dalam staging area Git. Git juga memberikan peringatan tentang perbedaan baris akhir file (LF diubah menjadi CRLF) yang akan diterapkan saat file disentuh oleh Git pada sistem operasi tertentu (misalnya, Windows biasanya menggunakan CRLF, sementara Linux/Unix menggunakan LF).

4. git commit -m "Perubahan di ParentWahyu": Perintah ini membuat sebuah commit dengan pesan deskriptif "Perubahan di ParentWahyu". Commit ini menyimpan snapshot dari perubahan yang telah ditambahkan ke staging area. Commit berhasil dilakukan, ditunjukkan dengan pesan "1 file changed, 1 insertion(+)", yang berarti satu file telah diubah dengan satu baris yang ditambahkan.

Secara keseluruhan, langkah-langkah ini menggambarkan proses pembuatan file, menambahkan perubahan ke dalam staging area, dan membuat commit di Git untuk melacak perubahan pada file tersebut.

[Screenshot 7](https://drive.google.com/file/d/1prO-xIfwA2H4h3oZqmLuLaifvYMnPejI/view?usp=sharing)

Gambar ini menunjukkan proses perpindahan cabang (branch) di Git, penambahan perubahan pada file, dan pembuatan commit di cabang baru. Berikut penjelasan dari setiap langkah:

1. git checkout ChildWahyu: Perintah ini digunakan untuk beralih (switch) dari cabang "ParentWahyu" ke cabang "ChildWahyu". Setelah perintah dijalankan, terminal menampilkan pesan bahwa Anda berhasil berpindah ke cabang "ChildWahyu".

2. echo "Perubahan di ChildWahyu" >> ParentWahyu.md: Perintah ini digunakan untuk menambahkan teks "Perubahan di ChildWahyu" ke dalam file `ParentWahyu.md`. Jika file tersebut sudah ada, maka teks akan ditambahkan ke akhir file; jika belum ada, file tersebut akan dibuat.

3. git add ParentWahyu.md: Perintah ini menambahkan file `ParentWahyu.md` ke dalam staging area untuk persiapan commit. Staging area adalah tempat di mana perubahan disiapkan sebelum benar-benar dicatat (commit) di repositori.

4. git commit -m "Perubahan di ChildWahyu": Perintah ini membuat commit dengan pesan "Perubahan di ChildWahyu". Commit ini mencatat perubahan yang telah ditambahkan ke staging area. Pesan "Merge made by the 'ort' strategy" muncul karena Git menggunakan strategi _merge_ baru yang disebut "ort" ketika menggabungkan perubahan dari beberapa cabang.

5. 1 file changed, 1 insertion(+): Ini menunjukkan bahwa satu file (`ParentWahyu.md`) telah diubah dan satu baris baru telah ditambahkan.

6. create mode 100644 ParentWahyu.md: Pesan ini menandakan bahwa file `ParentWahyu.md` telah dibuat dengan izin akses 100644, yang berarti file tersebut adalah file biasa dengan izin baca dan tulis untuk pemiliknya, dan izin baca untuk pengguna lain.

Secara keseluruhan, ini menggambarkan proses berpindah cabang, menambahkan perubahan baru pada file, dan melakukan commit untuk melacak perubahan tersebut di cabang "ChildWahyu".
