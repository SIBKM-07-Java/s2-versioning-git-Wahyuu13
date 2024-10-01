[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/7AKPvxX-)

## Laporan Tugas Git

## Deskripsi Tugas

Tugas ini mencakup implementasi penggunaan Git dengan skenario Fast-Forward dan Three-Way Merge.

## Proses yang Dilakukan

1. Membuat branch Parent dan Child.
2. Melakukan Fast-Forward Merge.
3. Menyelesaikan konflik dan melakukan Pull Request.

## Hasil

## GAMBAR 1

![Screenshot 1](https://drive.google.com/file/d/1NQqsLpHZQvLAS-a6Y2YjpHtl31ZBqTeM/view?usp=sharing)

Pada gambar tersebut, saya sedang menggunakan terminal Git Bash untuk berpindah ke direktori yang berisi tugas Git saya. Pertama, saya menjalankan perintah `cd "D:\Kuliah\MSIB\Tugas 4\S2-Git"` untuk masuk ke folder yang berlokasi di drive D, tempat saya menyimpan tugas tersebut. Setelah masuk, saya menjalankan perintah `pwd` untuk memastikan bahwa saya berada di direktori yang benar. Hasilnya menunjukkan path `/d/Kuliah/MSIB/Tugas 4/S2-Git`, yang berarti saya sudah berada di lokasi yang tepat untuk melanjutkan pekerjaan dengan Git.

## GAMBAR 2

![Screenshot 2](https://drive.google.com/file/d/1oie0aVpr4hISEHaEpOAOD33re6jT7e06/view?usp=sharing)

Pada gambar ini, saya sedang melakukan serangkaian langkah untuk mengelola perubahan di Git. Pertama, saya menjalankan perintah `git status` untuk melihat status file di repositori. Di sini, saya melihat bahwa file `README.md` telah dimodifikasi, namun belum ditambahkan ke staging area.

Kemudian, saya menambahkan perubahan tersebut ke staging area dengan perintah `git add .`, yang berarti saya menambahkan semua perubahan yang ada dalam direktori.

Setelah itu, saya membuat commit dengan menjalankan perintah `git commit -m "add : implement task at initial git"`, yang berfungsi untuk menyimpan snapshot perubahan ke repositori lokal dengan pesan commit yang menjelaskan bahwa saya menambahkan tugas implementasi awal pada Git.

Untuk memastikan commit saya berhasil, saya menjalankan perintah `git log`, yang menampilkan informasi commit terbaru. Commit tersebut memiliki hash `d73a249`, dan saya juga dapat melihat bahwa HEAD saat ini menunjuk ke branch `master`, yang menunjukkan bahwa commit terbaru ini berada di branch utama repositori saya.

## GAMBAR 3

![Screenshot 3](https://drive.google.com/file/d/1MeZa0qCKY49U4lQ6AC0167q96DLNOTap/view?usp=drive_link)

Pada gambar ini, saya sedang membuat dan berpindah antar branch dalam proyek Git saya.

Pertama, saya menjalankan perintah `git branch` untuk melihat daftar branch yang ada. Di sini, saya memiliki tiga branch: `master`, `ChildWahyu`, dan `ParentWahyu`, dengan branch `master` sebagai branch aktif (ditandai dengan simbol `*`).

Kemudian, saya membuat branch baru yang bernama `ParentWahyu2` dengan perintah `git checkout -b ParentWahyu2`. Perintah ini tidak hanya membuat branch baru, tetapi juga langsung berpindah ke branch tersebut, seperti yang terlihat dari pesan "Switched to a new branch 'ParentWahyu2'".

Selanjutnya, saya membuat branch baru lagi bernama `ChildWahyu2` dengan cara yang sama, menggunakan perintah `git checkout -b ChildWahyu2`, dan Git mengonfirmasi bahwa saya telah beralih ke branch baru ini.

Terakhir, saya memeriksa kembali daftar branch dengan menjalankan `git branch`. Di sini terlihat bahwa saya sekarang memiliki lima branch: `master`, `ChildWahyu`, `ParentWahyu`, `ParentWahyu2`, dan `ChildWahyu2`, dengan branch `ChildWahyu2` sebagai branch aktif saat ini.

## GAMBAR 4

![Screenshot 4](https://drive.google.com/file/d/1-jZpQKYAiCmE_Tq79Q901h5zRm_sQdTw/view?usp=drive_link)

Pada gambar tersebut, saya sedang melakukan serangkaian perintah Git untuk mencatat perubahan pada file `README.md` di branch "ChildWahyu2". Pertama, saya menjalankan perintah `git status` untuk memeriksa status perubahan yang ada. Hasilnya menunjukkan bahwa file `README.md` telah dimodifikasi dan siap untuk dikomit setelah berada di staging area. Selanjutnya, saya menggunakan perintah `git add .` untuk menambahkan semua perubahan ke dalam staging area agar siap dikomit. Setelah itu, saya melakukan komit dengan perintah `git commit -m "add: implement for fast forward child"` yang mencatat perubahan tersebut sebagai bagian dari riwayat Git. Komit tersebut berisi penambahan dua baris pada file `README.md`. Dengan langkah-langkah ini, saya memastikan bahwa perubahan yang saya buat tersimpan dengan baik di dalam repositori Git.

## GAMBAR 5

![Screenshot 5](https://drive.google.com/file/d/1f7wO61OHWEAOM87EPs_m-9FTLZBwazH4/view?usp=drive_link)

Pada gambar tersebut, saya sedang melakukan proses penggabungan (merge) antara dua branch di Git. Langkah pertama, saya menjalankan perintah `git branch` untuk melihat daftar branch yang ada di repositori. Terlihat ada beberapa branch, termasuk `ChildWahyu`, `ChildWahyu2`, `ParentWahyu`, `ParentWahyu2`, dan `master`.

Selanjutnya, saya berpindah ke branch `ParentWahyu2` menggunakan perintah `git checkout ParentWahyu2`. Setelah berhasil berpindah ke branch tersebut, saya melakukan penggabungan branch `ChildWahyu2` ke dalam `ParentWahyu2` dengan perintah `git merge ChildWahyu2`. Proses merge ini berjalan mulus dengan metode _fast-forward_, yang berarti tidak ada konflik antara kedua branch. Sebagai hasil dari merge ini, satu file berubah yaitu `README.md`, dengan dua baris tambahan yang terlihat dari output Git.

Proses ini memastikan bahwa perubahan yang sebelumnya saya lakukan di branch `ChildWahyu2` sekarang telah tergabung ke dalam branch `ParentWahyu2`.

## GAMBAR 6

![Screenshot 6](https://drive.google.com/file/d/1XZICcfJZjfP9LCrDwp6LqxSafzOIfgzt/view?usp=drive_link)

Pada gambar tersebut, saya sedang melakukan proses push branch `ParentWahyu2` ke repositori remote di GitHub. Berikut langkah-langkah yang saya lakukan:

1. **git remote -v**: Saya menjalankan perintah ini untuk memeriksa konfigurasi remote repositori yang terhubung. Output menunjukkan bahwa repositori saya terhubung dengan remote bernama `origin`, yang mengarah ke URL GitHub `s2-versioning-git-Wahyu13.git` untuk operasi _fetch_ dan _push_.

2. **git push**: Ketika saya mencoba melakukan push branch `ParentWahyu2`, Git memberikan pesan bahwa branch tersebut belum terhubung ke upstream di repositori remote. Oleh karena itu, saya perlu mengatur remote upstream untuk branch ini.

3. **git push --set-upstream origin ParentWahyu2**: Saya menjalankan perintah ini untuk melakukan push sekaligus mengatur remote upstream branch `ParentWahyu2`. Setelah ini, branch `ParentWahyu2` akan otomatis tersinkronisasi dengan repositori remote di GitHub (`origin/ParentWahyu2`).

4. Setelah perintah ini selesai, Git menunjukkan bahwa push berhasil. Semua objek dikompres dan dikirim ke server dengan sukses. Git juga memberi tahu bahwa saya bisa membuat pull request untuk branch `ParentWahyu2` di GitHub dengan URL yang disediakan.

Branch `ParentWahyu2` sekarang sudah di-_push_ ke GitHub dan diatur untuk melacak remote branch `origin/ParentWahyu2`, sehingga saya dapat terus mengerjakan dan melakukan sinkronisasi antara repositori lokal dan remote.

## GAMBAR 7

![Screenshot 7](https://drive.google.com/file/d/13wGlvlXqG8Q-3daVZJnsCeyGz8vxvbFS/view?usp=drive_link)

Pada gambar di atas, saya melakukan beberapa langkah di Git untuk membuat dan mengatur cabang baru serta mendorongnya ke repository GitHub. Pertama, saya menggunakan perintah `git checkout ChildWahyu2` untuk beralih ke cabang yang bernama **ChildWahyu2**. Setelah itu, saya mendorong perubahan dari cabang ini ke GitHub dengan perintah `git push --set-upstream origin ChildWahyu2`. Ini dilakukan agar cabang **ChildWahyu2** dapat di-tracking oleh Git terhadap cabang yang sama di repository GitHub.

Saat saya menjalankan perintah tersebut, Git menampilkan informasi bahwa cabang **ChildWahyu2** belum ada di GitHub, sehingga saya diminta untuk membuat pull request (PR) jika ingin menggabungkan cabang ini dengan cabang lain (misalnya ke cabang **master** atau **main**). Setelah itu, Git juga menunjukkan bahwa cabang **ChildWahyu2** berhasil dibuat di GitHub dan sekarang diatur untuk di-tracking oleh Git lokal. Dengan demikian, setiap perubahan di cabang **ChildWahyu2** di lokal bisa langsung didorong dan dilacak pada cabang yang sama di GitHub.

## GAMBAR 8

![Screenshot 8](https://drive.google.com/file/d/1noe0beGcs06ZRBkVdsn1jWzQjesE7wVq/view?usp=drive_link)

Pada gambar di atas, saya menjalankan beberapa langkah di Git untuk menyalin repository dari GitHub ke direktori lokal. Pertama, saya mengecek isi direktori dengan perintah `ls` dan terlihat hanya ada satu folder bernama **s2-versioning-git-UpscaleTim-A/** di dalam direktori **Tugas 4**.

Kemudian, saya menjalankan perintah `git clone https://github.com/SIBKM-07-Java/s2-versioning-git-Wahyuu13.git` untuk mengkloning repository **s2-versioning-git-Wahyuu13** dari GitHub ke lokal. Proses kloning ini berhasil dengan Git menampilkan bahwa seluruh objek dari repository tersebut (sebanyak 46 objek) telah diunduh, dikompres, dan disimpan ke dalam direktori lokal. Setelah proses selesai, saya kembali mengecek isi direktori dengan perintah `ls`, dan hasilnya menunjukkan bahwa repository baru, **s2-versioning-git-Wahyuu13/**, telah muncul di samping direktori yang sudah ada sebelumnya.

Dengan demikian, sekarang saya memiliki dua folder proyek di dalam direktori **Tugas 4**, yaitu **s2-versioning-git-UpscaleTim-A/** dan **s2-versioning-git-Wahyuu13/**.

## GAMBAR 9

![Screenshot 9](https://drive.google.com/file/d/140X9OPqUq4Cbq8ycFrV9ZpVZZFJa42_o/view?usp=drive_link)

Pada gambar di atas, saya melakukan beberapa langkah untuk mengelola cabang (branch) di Git dalam repository lokal **s2-versioning-git-Wahyuu13**. Langkah pertama adalah saya masuk ke direktori repository tersebut dengan perintah `cd s2-versioning-git-Wahyuu13/`. Setelah itu, saya memeriksa daftar cabang yang ada menggunakan perintah `git branch`, dan hanya ada cabang **main** yang terlihat.

Kemudian, saya membuat cabang baru yang bernama **ParentWahyu2** dengan perintah `git checkout -b ParentWahyu2`. Perintah ini membuat cabang baru sekaligus berpindah ke cabang tersebut. Setelah itu, cabang **ParentWahyu2** diatur untuk melacak cabang yang sama di GitHub (tracking ke `origin/ParentWahyu2`). Setelah saya cek ulang menggunakan `git branch`, cabang **ParentWahyu2** berhasil ditambahkan ke daftar cabang di repository lokal.

Langkah selanjutnya adalah saya membuat cabang lain bernama **ChildWahyu2** dengan cara yang sama, yaitu menggunakan perintah `git checkout -b ChildWahyu2`. Cabang ini juga otomatis ditracking oleh Git terhadap cabang yang sama di GitHub. Setelah saya periksa lagi dengan `git branch`, sekarang ada tiga cabang di repository lokal saya, yaitu **main**, **ParentWahyu2**, dan **ChildWahyu2**, dan saat ini saya berada di cabang **ChildWahyu2**.

## GAMBAR 10

![Screenshot 10](https://drive.google.com/file/d/1iW6V4dN_eflEFHfuTo2B1CgBQgEVbRjA/view?usp=drive_link)

Pada gambar di atas, saya sedang melakukan pengecekan status branch menggunakan perintah `git status`. Dari hasil perintah tersebut, terlihat bahwa saya berada di branch `ChildWahyu2`, yang telah di-update sesuai dengan `origin/ChildWahyu2`. Di sini, saya juga melihat bahwa ada perubahan yang belum di-stage untuk commit, yaitu pada file `README.md`.

Selanjutnya, saya menambahkan semua perubahan tersebut ke dalam stage area dengan menggunakan perintah `git add .`, yang artinya semua file yang telah diubah akan di-stage. Setelah itu, saya melakukan commit dengan pesan `add: implementation for three way merge from child`, menggunakan perintah `git commit -m`. Dengan perintah ini, saya mencatat bahwa perubahan ini terkait dengan implementasi dari merge tiga arah pada branch `ChildWahyu2`. Terakhir, git menunjukkan bahwa satu file telah berubah dengan dua baris tambahan pada file tersebut.

## GAMBAR 11

![Screenshot 11](https://drive.google.com/file/d/12PLn9BoSBfVmYNPm38B32rAeaGdmvtns/view?usp=drive_link)

Pada gambar ini, saya sedang bekerja di branch `ParentWahyu2`. Langkah pertama yang saya lakukan adalah mengecek status repository dengan perintah `git status`. Hasilnya menunjukkan bahwa saya berada di branch `ParentWahyu2`, yang telah sinkron dengan `origin/ParentWahyu2`. Sama seperti sebelumnya, ada perubahan yang belum di-stage pada file `README.md`.

Saya kemudian menambahkan perubahan ini ke dalam stage area dengan menggunakan perintah `git add .`, yang berarti semua perubahan di dalam direktori kerja akan di-stage. Setelah itu, saya membuat commit baru dengan perintah `git commit -m "add: implementation for three way merge from parent"`, yang mencatat perubahan ini sebagai implementasi merge tiga arah dari branch parent. Git mencatat bahwa satu file berubah dengan dua baris tambahan.

Selanjutnya, saya menjalankan `git status` kembali, yang menginformasikan bahwa branch `ParentWahyu2` sekarang lebih maju satu commit dibandingkan dengan `origin/ParentWahyu2`. Karena commit belum di-push ke remote, saya menjalankan perintah `git push` untuk mengirimkan perubahan tersebut. Setelah push selesai, perubahan berhasil dikirim ke repository remote, dan status branch kembali sinkron.

## GAMBAR 12

![Screenshot 12](https://drive.google.com/file/d/1Oh3kElCBDkmNJpLy6BiHY_r2iPTbKy_c/view?usp=drive_link)

Pada gambar ini, saya pertama kali melakukan checkout ke branch `ChildWahyu2` menggunakan perintah `git checkout ChildWahyu2`. Setelah berpindah ke branch tersebut, git mengonfirmasi bahwa branch saya telah up-to-date dengan `origin/ChildWahyu2`.

Selanjutnya, saya mencoba menarik (pull) perubahan dari branch `ParentWahyu2` ke `ChildWahyu2` dengan perintah `git pull origin ParentWahyu2`. Proses ini bertujuan untuk melakukan merge otomatis antara branch `ParentWahyu2` dengan `ChildWahyu2`. Namun, saat git mencoba melakukan merge otomatis, terdeteksi konflik pada file `README.md`. Git memberikan pesan bahwa merge otomatis gagal karena ada konflik yang harus diperbaiki secara manual. Saya perlu menyelesaikan konflik ini terlebih dahulu sebelum bisa melakukan commit hasil merge tersebut.

## GAMBAR 13

![Screenshot 13](https://drive.google.com/file/d/15vGb6AQJf7z7z7gZH21e6px7-RYXO2QG/view?usp=drive_link)

Pada gambar tersebut, saya melakukan beberapa perintah Git untuk mengelola branch `ChildWahyu2`. Pertama, saya menjalankan **git status** untuk melihat status branch saya. Terlihat bahwa branch `ChildWahyu2` berada di depan remote `origin/ChildWahyu2` dengan 2 commit dan ada perubahan pada file `README.md` yang belum di-staging.

Kemudian, saya menggunakan perintah **git add .** untuk menambahkan semua perubahan pada staging area, siap untuk di-commit. Setelah itu, saya melakukan **git commit -m "fix: conflict from pull"** yang mencatat perubahan dengan pesan commit yang menunjukkan bahwa saya memperbaiki konflik yang muncul saat melakukan pull dari remote.

Setelah commit selesai, saya menjalankan **git push** untuk mengirim perubahan lokal ke repository remote pada branch `ChildWahyu2`. Push ini berhasil dengan menulis objek yang di-commit ke repository remote, dan branch `ChildWahyu2` sekarang sudah sinkron dengan remote repository.

## GAMBAR 14

![Screenshot 14](https://drive.google.com/file/d/1lPtjfAoKZRQ1HYU1n3z1cO5xxF5aon-2/view?usp=drive_link)

Pada gambar ini, saya menjalankan perintah **git pull** pada branch `ParentWahyu2`. Perintah ini berfungsi untuk mengambil perubahan terbaru dari remote repository dan menggabungkannya dengan branch lokal saya.

Proses pull ini berhasil, di mana Git menampilkan bahwa 1 objek baru diambil dan tidak ada perubahan signifikan pada file selain file `README.md`. Git juga menggunakan metode **Fast-forward**, yang berarti tidak ada konflik atau perubahan signifikan dalam penggabungan tersebut. Dalam pembaruan ini, terdapat 2 baris baru yang ditambahkan ke file `README.md`, dengan total 2 insertions.

Dengan demikian, pull ini memastikan bahwa branch `ParentWahyu2` pada local repository saya kini sinkron dengan perubahan yang ada di remote repository.

## GAMBAR 15

![Screenshot 15](https://drive.google.com/file/d/11Rg1T9VaLB5I33cDilalNd4CkBdwTU7y/view?usp=drive_link)

Pada gambar tersebut, saya menampilkan git graph untuk melihat histori commit yang dilakukan pada repository, serta bagaimana branch-branch seperti ParentWahyu2 dan ChildWahyu2 berkembang dan berinteraksi satu sama lain.
