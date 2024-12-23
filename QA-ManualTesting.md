1. Functional Testing

Deskripsi:
Menguji apakah fungsi spesifik dari aplikasi bekerja sesuai dengan persyaratan yang telah ditentukan. Fokus pada apa yang dilakukan aplikasi, bukan bagaimana aplikasi melakukannya.

Contoh dalam Daily Job:

    Tugas: Menguji fitur login.
    Langkah:
        Masukkan kredensial yang valid (email dan password).
        Klik tombol "Login".
        Verifikasi bahwa pengguna diarahkan ke halaman dashboard.
    Hasil yang Diharapkan: Pengguna berhasil login tanpa error.

Catatan: Jika ditemukan error (misalnya, pengguna valid tidak bisa login), bug akan dicatat dalam sistem pelacakan seperti JIRA.
2. Regression Testing

Deskripsi:
Memastikan bahwa perubahan kode baru (bug fix atau fitur baru) tidak merusak fitur yang sudah ada.

Contoh dalam Daily Job:

    Tugas: Regression test setelah fitur "Search" diperbarui.
    Langkah:
        Tes fitur baru "Search by Tag".
        Ulangi pengujian pada fitur lama seperti "Search by Name" dan "Search by Date".
    Hasil yang Diharapkan: Semua fungsi pencarian lama dan baru bekerja dengan baik.

Catatan: Regression testing sering dilakukan secara manual atau dengan skrip otomatis jika tersedia.
3. Integration Testing

Deskripsi:
Menguji integrasi antara modul atau komponen dalam sistem untuk memastikan mereka berinteraksi dengan baik.

Contoh dalam Daily Job:

    Tugas: Menguji integrasi antara sistem pembayaran dan layanan API pihak ketiga.
    Langkah:
        Pilih item dan lanjutkan ke checkout.
        Bayar menggunakan metode pembayaran kartu kredit.
        Verifikasi bahwa sistem menerima respons sukses dari API pembayaran.
    Hasil yang Diharapkan: Pesanan berhasil diproses, dan detail transaksi tercatat di database.

Catatan: Integration testing penting saat menggunakan banyak layanan eksternal.
4. UI Testing

Deskripsi:
Menguji antarmuka pengguna untuk memastikan elemen UI bekerja dengan benar dan tampil sesuai desain.

Contoh dalam Daily Job:

    Tugas: Menguji tampilan form pendaftaran.
    Langkah:
        Periksa apakah semua elemen (field input, label, tombol) ada dan terlihat dengan baik di berbagai resolusi layar.
        Isi semua field dan klik "Submit".
        Verifikasi bahwa data terkirim tanpa masalah.
    Hasil yang Diharapkan: Elemen UI tampil dengan benar, responsif, dan berfungsi sesuai spesifikasi.

Catatan: Tes ini sering mencakup validasi warna, ukuran font, dan responsivitas pada perangkat yang berbeda.
Rangkuman Penerapan di Daily Job:

    Functional Testing: Fokus pada validasi fitur spesifik, biasanya langkah pertama dalam pengujian manual.
    Regression Testing: Dilakukan setelah deployment atau patch update untuk memastikan stabilitas aplikasi.
    Integration Testing: Penting untuk proyek dengan banyak API atau layanan backend.
    UI Testing: Dilakukan secara reguler untuk memastikan user experience tetap optimal.
