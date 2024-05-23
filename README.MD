## Belajar Git Dasar From Mabuchi

## Docs

1. Mengubah File, Menambahkan File dan Git Diff:

   ## diff itu difference ( apa yang berbeda dari versi sebelumnya dari perubahan aplikasi kita )

   ```bash
    git diff | untuk melihat perubahan
    git status | untuk mengecek perubahan apapun dari codingan kita
    git add . | memasuki perubahan ke staging area lalu sudah siap untuk di commit
   ```

2. Melihat History dengan Git Log:

   ## Jadi git log itu untuk melihat perubahan perjalanan di aplikasi kita

   ```bash
    git log | untuk melihat perubahan lengkapnya
    git log --oneline | untuk melihat simplenya

   ```

3. Membatalkan Perubahan dengan Git Restore:

   ## MEMBATALKAN PERUBAHAN YANG ADA DI WORKING DIRECTORY

   Jika kita mempunyai 3 file dan menambahkan 1 file di codingan kita lalu sudah ditambahkan dan ingin membatalkannya Ketika sudah di rubah, kita bisa menggunakan git restore

   ```bash
    git status | terlebih dahulu untuk mengecek file yang telah ditambahkan di aplikasi kita lalu
    git restore | menghapus 1 file yang baru ditambahkan
    git restore . | mengembalikan 1 file baru yang telah dihapus
   ```

4. Git Restore:

   ## Mencoba MEMBATALKAN PERUBAHAN YANG SUDAH ADA DI STAGING AREA :

   Memakai Restore atau Reset

   ```bash
    git restore index.php | ( saja, ini adalah mengembalikan file yang masih diworking directory )
    git restore -S | ( Mengembalikan file perubahan dari staging area ke working directory )
   ```

5. Branch dan Merge:

   ## MEMBATALKAN PERUBAHAN YANG ADA DI WORKING DIRECTORY

   ```bash
    git checkout -b nama/nama branch (feat/multiply) | membuat nama branch pertama dan menambahkan fitur pertama dicodingan
    git add .
    git commit -m "menambahkan fitur di branch pertama"
    git checkout master | memasukan branch ke master
    git merge nama/nama branch (feat/multiply) | menggabungkan branch ke master
   ```

   ```bash
    git checkout -b feat/divide | membuat branch baru dengan menambahkan fitur baru
    git add .
    git commit -m "menambahkan fitur baru dibranch kedua"
    git checkout master | memasukan branch dan fitur kedua ke master
    git merge feat/divide | menambahkan atau menggabungkan fitur di master dan dicodingan
    git log --oneline | mengecek log atau mengecek fitur yang sudah ditambahkan
   ```

6. Cara Merevisi Commit Menggunakan:

   ## - checkout

   ## - reset

   ## - revert

   ## perbedaannya adalah

   - checkout = sifatnya untuk sementara untuk melihat perubahan saja
   - reset = jika kita mengcommit 5 branch dan ingin Kembali ke commit ke 3 maka commit 4 & 5 akan dihapus
   - revert = jika kita mengcommit 5 branch dan ingin Kembali ke commit ke 3 maka kita akan membuat commit baru setelah 5, dan commit baru akan melakukan atau terjadi konfliks. Jadi dengan menggunakan revert kita Kembali ke commit sebelumnya tanpa menghancurkan commit2 terbaru, Konsekuensinya jadi kita akan memperbaiki konfliks yang terjadi antara commit ke 5 atau ke 4

   ```bash
    git status = terlebih dahulu untuk mengecek file yang telah ditambahkan di aplikasi kita lalu
    git restore = menghapus 1 file yang baru ditambahkan
    git restore . = mengembalikan 1 file baru yang telah dihapus
   ```

7. Cara Menggunakan Git Revert:

   ```bash
    git log --oneline | terlebih dahulu untuk menyalin hashnya lalu
    git revert (hash)
   ```

8. Cara menggunakan Git Clone:

   ```bash
    git clone https://github.com/Cramouchegit/Simple-App-Music.git | (link repositori project digithub)
    git add .
    git commit -m "pesan"
    git push origin master | mengupdate dan mengupload project dari local ke master/repositori
   ```

9. Cara Menggunakan GitHub Pull Request:

   ## - Buat branch baru terlebih dahulu ( git checkout -b feat/nama branch )

   ## - ubah codingannya atau edit codingan mu

   ## - git status = untuk mengecek

   ```bash
    git add .
    git commit -m "pesan"
    push branchnya seperti ( git push origin feat/nama branch )
    git checkout master
    git log --oneline
    git pull origin master | jadi ini untuk menyinkronkan antara GitHub ke local kita
    git log --oneline | lagi
   ```

   ## GitHub pull request ini digunakan untuk jika kita menambahkan codingan misalnya ke project repositori milik developer lain, dalam tim kita misalnya. Jadi semua orang bisa mereview perubahan codingan di project repositori kita / milik developer lain, jadi ga dimerge begitu saja, dan harus dicek terlebih dahulu

10. Aturan Menulis Commit:

    ## referensi : https://www.conventionalcommits.org/en/v1.0.0/#summary

```bash
    git commit -m "fix: fungsi untuk merubah atau ngefix error dicodingan"

    git commit -m "feat: penambahan fitur dicodingan"

    git commit -m "build: build proses"

    git commit -m "chore: memperbaiki atau menambahkan fitur ditools project kita"

    git commit -m "ci: continues integration"

    git commit -m "feat: penambahan fitur dicodingan"

    git commit -m "docs: mengedit documentasi"

    git commit -m "style: improfmen atau memperbaiki dari sebuah style css dari project kita"

    git commit -m "refactor: kalau commit suatu project dan merefactor code yang banyak dan ga efisien lalu kitab ikin jadi lebih efisien lagi maka kita gunakan ini dia tida akan mengubah alur tapi memperbaiki agar lebih mudah dibaca codenya"

    git commit -m "test: penambahan fitur unitesting" | jika penambahan fitur belum selesai
```

## Terimakasih, Jangan Lupa kasih bintang :)
