Manual Testing Methodologies adalah pendekatan atau strategi yang digunakan untuk menguji perangkat lunak secara manual, tanpa bantuan alat otomatisasi. Berikut adalah beberapa metodologi manual testing yang sering digunakan dalam pengujian perangkat lunak:

<ol>
    <li>Black Box Testing</li>
<ul>
    <li>Deskripsi: Fokus pada pengujian fungsionalitas aplikasi tanpa melihat struktur internal atau kode sumber.</li>
    <li>Pendekatan:
        Memeriksa input dan output berdasarkan persyaratan.
        Tidak memerlukan pengetahuan teknis tentang implementasi sistem.</li>
    <li>Contoh:
        Memasukkan data valid/invalid ke dalam formulir login dan memeriksa apakah sistem memberikan respons yang benar.</li>
    <li>Keuntungan:
        <ul>
            <li>Cocok untuk tester non-teknis.</li>
            <li>Fokus pada perspektif pengguna.</li>
        </ul>
    </li>
</ul>
2. White Box Testing

    Deskripsi: Menguji aplikasi dengan memahami struktur internal dan logika kode.
    Pendekatan:
        Menggunakan teknik seperti statement coverage, branch coverage, dan path coverage.
        Memerlukan pengetahuan teknis tentang kode.
    Contoh:
        Memeriksa logika kondisi if-else dalam kode untuk memastikan semua cabang diuji.
    Keuntungan:
        Membantu menemukan bug dalam logika dan implementasi.

3. Grey Box Testing

    Deskripsi: Kombinasi dari black box dan white box testing; tester memiliki sebagian pengetahuan tentang struktur internal sistem.
    Pendekatan:
        Menggunakan pemahaman sebagian tentang arsitektur untuk membuat test case yang lebih efektif.
    Contoh:
        Menguji bagaimana API backend memproses data yang diinput melalui UI frontend.
    Keuntungan:
        Lebih efektif dalam menemukan bug di sistem yang kompleks.

4. Functional Testing

    Deskripsi: Menguji fungsionalitas sistem untuk memastikan aplikasi bekerja sesuai spesifikasi.
    Pendekatan:
        Membuat test case berdasarkan requirement specification.
        Memastikan setiap fungsi memberikan hasil yang benar.
    Contoh:
        Memeriksa apakah fitur pencarian menghasilkan hasil yang sesuai dengan kata kunci.
    Keuntungan:
        Fokus pada pengalaman pengguna.

5. Non-Functional Testing

    Deskripsi: Menguji aspek non-fungsional dari aplikasi seperti performa, keamanan, dan kegunaan.
    Pendekatan:
        Melakukan pengujian manual untuk kecepatan, kegunaan, atau daya tahan.
    Contoh:
        Memeriksa waktu yang dibutuhkan halaman untuk dimuat.
    Keuntungan:
        Mengidentifikasi potensi masalah di luar fungsionalitas dasar.

6. Regression Testing

    Deskripsi: Menguji kembali aplikasi setelah ada perubahan kode untuk memastikan fitur yang sebelumnya berfungsi masih berjalan dengan baik.
    Pendekatan:
        Menggunakan test case yang telah ada untuk fitur lama.
        Fokus pada area yang terpengaruh oleh perubahan.
    Contoh:
        Memastikan fitur login tetap berfungsi setelah pengembang menambahkan autentikasi dua faktor.
    Keuntungan:
        Menghindari bug baru saat fitur baru ditambahkan.

7. Integration Testing

    Deskripsi: Menguji bagaimana modul atau komponen yang berbeda dalam sistem bekerja bersama.
    Pendekatan:
        Top-Down: Menguji modul tingkat tinggi terlebih dahulu.
        Bottom-Up: Menguji modul tingkat rendah terlebih dahulu.
    Contoh:
        Memastikan bahwa data yang dimasukkan di UI frontend diterima dan diproses dengan benar oleh backend.
    Keuntungan:
        Mengidentifikasi masalah komunikasi antar modul.

8. System Testing

    Deskripsi: Menguji seluruh sistem sebagai kesatuan untuk memastikan aplikasi memenuhi persyaratan akhir.
    Pendekatan:
        Menguji semua fungsi utama dan non-fungsional dalam satu lingkungan.
    Contoh:
        Menguji aplikasi e-commerce dari login hingga checkout.
    Keuntungan:
        Memberikan gambaran lengkap tentang kinerja aplikasi.

9. Acceptance Testing

    Deskripsi: Dilakukan untuk memastikan bahwa aplikasi memenuhi kebutuhan pengguna akhir atau bisnis sebelum rilis.
    Pendekatan:
        Alpha Testing: Dilakukan oleh tim internal di lingkungan pengujian.
        Beta Testing: Dilakukan oleh pengguna akhir di lingkungan sebenarnya.
    Contoh:
        Meminta pengguna untuk mencoba fitur baru dan memberikan feedback.
    Keuntungan:
        Memberikan validasi akhir sebelum peluncuran.

10. Exploratory Testing

    Deskripsi: Pengujian dinamis di mana tester secara aktif mengeksplorasi aplikasi untuk menemukan bug yang tidak terduga.
    Pendekatan:
        Tidak menggunakan test case formal.
        Mengandalkan pengalaman dan intuisi tester.
    Contoh:
        Coba klik tombol beberapa kali dengan cepat untuk melihat apakah aplikasi crash.
    Keuntungan:
        Menemukan bug yang tidak terdeteksi oleh metode lain.

11. Ad-Hoc Testing

    Deskripsi: Pengujian tidak terstruktur di mana tester mencoba menemukan bug dengan pendekatan informal dan spontan.
    Pendekatan:
        Tidak ada dokumentasi atau skrip yang dibuat sebelumnya.
    Contoh:
        Mencoba fitur baru tanpa membaca spesifikasi.
    Keuntungan:
        Menghemat waktu untuk pengujian sederhana.
</ol>

<h3>Kesimpulan</h3>

Setiap metodologi memiliki tujuan dan kegunaan spesifik dalam siklus pengembangan perangkat lunak. Pilihan metodologi bergantung pada jenis aplikasi, tujuan pengujian, dan ketersediaan sumber daya. Tester sering menggabungkan beberapa metodologi untuk mencapai hasil pengujian yang maksimal.
