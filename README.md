# News Feed Simulator

## Deskripsi

News Feed Simulator adalah aplikasi sederhana yang dibuat menggunakan
Kotlin Multiplatform dan Compose Multiplatform. Aplikasi ini
mensimulasikan proses penerimaan berita secara berkala dan menerapkan
konsep Kotlin Coroutines dan Flow.

Aplikasi ini menerapkan beberapa konsep utama:

-   Flow untuk menghasilkan berita setiap 2 detik.
-   Filter untuk menyaring berita berdasarkan kategori.
-   Map untuk melakukan transformasi data.
-   StateFlow untuk menyimpan jumlah berita yang telah dibaca.
-   Async/Await untuk mengambil detail berita secara asynchronous.

## Persyaratan

Sebelum menjalankan proyek, pastikan sudah terpasang:

-   Android Studio
-   Kotlin
-   Android SDK
-   Android Emulator

## Cara Menjalankan

1.  Clone repository GitHub:

``` bash
git clone <URL_REPOSITORY>
```

2.  Buka folder project menggunakan Android Studio.
3.  Tunggu proses Gradle Sync selesai.
4.  Jalankan Android Emulator melalui Device Manager.
5.  Pilih konfigurasi `androidApp` pada Run Configuration.
6.  Pilih perangkat Android Emulator yang tersedia.
7.  Klik tombol **Run** untuk menjalankan aplikasi.
8.  Setelah aplikasi berjalan, halaman **News Feed Simulator** akan
    ditampilkan.

## Cara Kerja Aplikasi

Aplikasi menghasilkan berita menggunakan `Flow` setiap 2 detik. Berita
kemudian disaring menggunakan `filter` sehingga hanya berita dengan
kategori **Teknologi** yang diproses.

Data berita kemudian ditransformasikan menggunakan `map`. Setelah itu,
detail berita diambil menggunakan `async/await`. Setiap berita yang
berhasil diproses akan menambah jumlah berita yang dibaca melalui
`StateFlow`.

Alur proses:

``` text
News Flow
    ↓
Filter Kategori
    ↓
Map
    ↓
Async/Await
    ↓
Tampilkan Berita
    ↓
StateFlow
    ↓
Jumlah Berita Dibaca
```

## Struktur Project

``` text
NewsFeedSimulator/
├── androidApp/
│   └── MainActivity.kt
│
├── desktopApp/
│   └── Main.kt
│
└── shared/
    └── src/
        └── commonMain/
            └── kotlin/
                └── com.example.newsfeedsimulator/
                    ├── App.kt
                    ├── NewsFeed.kt
                    └── Greeting.kt
```

## Teknologi yang Digunakan

-   Kotlin
-   Kotlin Multiplatform
-   Compose Multiplatform
-   Kotlin Coroutines
-   Kotlin Flow
-   StateFlow
-   Android Studio
-   Android Emulator

## Author

**Muhammad Refah Alfarabi**\
NIM 124140216\
Teknik Informatika\
Institut Teknologi Sumatera (ITERA)
