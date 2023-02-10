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

![image1.png](sikirinsot/lat1.png)

# Menangani Pengecualian
Jika Anda memiliki beberapa kode mencurigakan yang mungkin mengeluarkan pengecualian, Anda dapat mempertahankan program Anda letakkan kode yang mencurigakan di *try: blok. Setelah coba: blok, sertakan pernyataan sertakan *except: statement, diikuti oleh blok kode yang menangani masalah seanggun mungkin.

Contoh :
 - Contoh-contoh ini membuka file, menulis konten file, dan keluar dengan aman karena ada tidak masalah
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image2.png](sikirinsot/lat2.png)

 - Contoh ini mencoba membuka file yang Anda tidak memiliki izin menulis, sehingga membuat file pengecualian
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image3.png](sikirinsot/lat3.png)

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

![image4.png](sikirinsot/lat4.png)

 - Contoh yang sama dapat ditulis lebih bersih seperti berikut:

![image5.png](sikirinsot/lat5.png)

 - Ketika exception dilempar ke dalam blok try, eksekusi segera dilanjutkan ke akhir memblok. Setelah semua pernyataan di blok akhirnya dieksekusi, pengecualian dimunculkan lagi dan ditangani dalam pernyataan kecuali jika ada di lapisan berikutnya yang lebih tinggi dari percobaan-kecuali penyataan.

## Argumen Pengecualian

Contoh :
 - Berikut adalah contoh untuk satu pengecualian
 - Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![image6.png](sikirinsot/lat6.png)

## Melempar Pengecualian

Contoh :
 - Pengecualian dapat berupa string, kelas, atau objek. Sebagian besar pengecualian adalah pengecualian dari inti Python menimbulkan adalah kelas dengan argumen=argumen yang merupakan turunan dari kelas. Mendefinisikan pengecualian baru cukup mudah dan dapat dilakukan sebagai berikut:

 ![image7.png](sikirinsot/lat7.png)

## Pengecualian yang Ditetapkan Pengguna
 - Python juga memungkinkan Anda membuat pengecualian sendiri dengan menurunkan kelas-kelas dari yang standar pengecualian bawaan.
 - Berikut adalah contoh-contoh yang terkait dengan RuntimeError. Di sini, kelas dibuat yang merupakan subkelas dari subkelas RuntimeError. Ini berguna saat anda perlu menampilkan tampilan informasi yang lebih spesifik saat e pengecualian tertangkap.
 - Di blok try, pengecualian yang ditentukan pengguna dimunculkan dan ditangkap di blok except. Itu variabel e digunakan untuk membuat instance dari kelas Networkerror.

 ![image8.png](sikirinsot/lat8.png)
 
 
