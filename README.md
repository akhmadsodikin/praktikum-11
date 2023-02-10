# praktikum-11

Nama    : Akhmad Sodikin
Kelas   : TI.22.C9
NIM     : 312210729

# Exception Handling
 - Exception (eksepsi) merupakan suatu kesalahan(error) yang terjadi saat proses eksekusi program sedang berjalan
 - Kesalahan ini akan menyebabkan program berakhir dengan tidak normal.

# Handling
 - Penanganan file adalah bagian penting dari aplikasi apapun.

# Assertion
 - Assertion (pernyataan) adalah kewajaran program yang bisa kamu aktifkan/nonaktifkan ketika kamu selesai menjalankan program.

## The Assert Statement
 - Saat menemukan pernyataan, Python mengevaluasi eskpresi yang menyertainya, yang mana semoga benar. Jika ekspresi salah, Python memunculkan pengecualian AssertionError.

Sintaks untuk pernyataan yaitu:
    assert Expression[, Arguments]
Jika pernyataan gagal, Python menggunakan ArgumentExpression. ArgumentExpression sebagai argumen-argumen untuk AssertionError. Pengecualian AssertionError dapat ditangkap dan ditangani seperti pengecualian lainnya menggunakan try kecuali pernyataan, tetapi jika dibiarkan mereka akan menghentikan program dan menghasilkan backtrace.

Contoh :
    - Berikut adalah fungsi fungsi yang mengubah suhu dari derajat Kelvin menjadi derajat Fahrenheit.Karena nol derajat Kelvin dingin, fungsi fungsi menyimpannya jika melihat negatif negatif suhu.
    - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:
    
   ![image](https://user-images.githubusercontent.com/123872661/218119421-1398a647-c7f1-4229-a2c5-5526d7c30c77.png)
 

# Menangani Pengecualian
Jika Anda memiliki beberapa kode mencurigakan yang mungkin mengeluarkan pengecualian, Anda dapat mempertahankan program Anda letakkan kode yang mencurigakan di *try: blok. Setelah coba: blok, sertakan pernyataan sertakan *except: statement, diikuti oleh blok kode yang menangani masalah seanggun mungkin.

Contoh :
 - Contoh-contoh ini membuka file, menulis konten file, dan keluar dengan aman karena ada tidak masalah
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image](https://user-images.githubusercontent.com/123872661/218119639-8247d211-61da-47a1-8c13-1d821377c0df.png)

 - Contoh ini mencoba membuka file yang Anda tidak memiliki izin menulis, sehingga membuat file pengecualian
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image](https://user-images.githubusercontent.com/123872661/218119801-7786439d-69cd-4895-b640-bcb6a1a94ee9.png)


# Fasal kecuali Tanpa Pengecualian
 - Anda juga dapat menggunakan pernyataan exception tanpa exception yang didefinisikan sebagai berikut:
    try: You do your operations here; ...................... except: If there is any exception, then execute this block. ...................... else: If there is no exception then execute this block.
Pernyataan coba-kecuali jenis ini menangkap semua pengecualian pengecualian yang terjadi. Menggunakan percobaan seperti try-expect pernyataan tidak dianggap sebagai praktik pemrograman yang baik, karena mereka menangkap semuanya pengecualian tetapi tidak membuat programmer mengidentifikasi kemungkinan penyebab masalah terjadi

# Klausa Kecuali dengan Berbagi Pengecualian
 - Anda juga dapat menggunakan pernyataan exception yang sama untuk menangani beberapa exception sebagai berikut:
    try: You do your operations here; ...................... except(Exception1[, Exception2[,...ExceptionN]]]): If there is any exception from the given exception list, then execute this block. ...................... else: If there is no exception then execute this block.

## Klausa coba-akhirnya

Contoh :
 - Jika anda tidak memiliki izin untuk membukafile dalam mode tulis yang dapat ditulis, maka ini akan menghasilkan hasil berikut:

![image](https://user-images.githubusercontent.com/123872661/218120097-8d2749fd-ec4d-47b9-b8e8-24a4eecc9250.png)


 - Contoh yang sama dapat ditulis lebih bersih seperti berikut:

![image](https://user-images.githubusercontent.com/123872661/218120189-d4688e10-1cd8-4a53-bed9-22ec3254a6a9.png)


 - Ketika exception dilempar ke dalam blok try, eksekusi segera dilanjutkan ke akhir memblok. Setelah semua pernyataan di blok akhirnya dieksekusi, pengecualian dimunculkan lagi dan ditangani dalam pernyataan kecuali jika ada di lapisan berikutnya yang lebih tinggi dari percobaan-kecuali penyataan.

## Argumen Pengecualian

Contoh :
 - Berikut adalah contoh untuk satu pengecualian
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image](https://user-images.githubusercontent.com/123872661/218120384-37a7f013-49a5-43f0-a018-80c288a9decb.png)


## Melempar Pengecualian

Contoh :
 - Pengecualian dapat berupa string, kelas, atau objek. Sebagian besar pengecualian adalah pengecualian dari inti Python menimbulkan adalah kelas dengan argumen=argumen yang merupakan turunan dari kelas. Mendefinisikan pengecualian baru cukup mudah dan dapat dilakukan sebagai berikut:

![image](https://user-images.githubusercontent.com/123872661/218120492-3a96783d-f7cc-468a-a115-57b7e0363bbd.png)


## Pengecualian yang Ditetapkan Pengguna
 - Python juga memungkinkan Anda membuat pengecualian sendiri dengan menurunkan kelas-kelas dari yang standar pengecualian bawaan.
 - Berikut adalah contoh-contoh yang terkait dengan RuntimeError. Di sini, kelas dibuat yang merupakan subkelas dari subkelas RuntimeError. Ini berguna saat anda perlu menampilkan tampilan informasi yang lebih spesifik saat e pengecualian tertangkap.
 - Di blok try, pengecualian yang ditentukan pengguna dimunculkan dan ditangkap di blok except. Itu variabel e digunakan untuk membuat instance dari kelas Networkerror.

![image](https://user-images.githubusercontent.com/123872661/218120594-9ea58572-660b-42a9-92b5-37f3c1b7a276.png)

 
 
