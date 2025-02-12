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
<li>White Box Testing</li>
<ul>
    <li>Deskripsi: Menguji aplikasi dengan memahami struktur internal dan logika kode.</li>
    <li>Pendekatan:</li>
        <ul>
            <li>Menggunakan teknik seperti statement coverage, branch coverage, dan path coverage.</li>
            <li>Memerlukan pengetahuan teknis tentang kode.</li>
        </ul>
    <li>Contoh:
        Memeriksa logika kondisi if-else dalam kode untuk memastikan semua cabang diuji.</li>
    <li>Keuntungan:
        Membantu menemukan bug dalam logika dan implementasi.</li>
</ul>
<li>Grey Box Testing</li>
    <ul>
    <li>Deskripsi: Kombinasi dari black box dan white box testing; tester memiliki sebagian pengetahuan tentang struktur internal sistem.</li>
    <li>Pendekatan:
        Menggunakan pemahaman sebagian tentang arsitektur untuk membuat test case yang lebih efektif.</li>
    <li>Contoh:
        Menguji bagaimana API backend memproses data yang diinput melalui UI frontend.</li>
    <li>Keuntungan:
        Lebih efektif dalam menemukan bug di sistem yang kompleks.</li>
    </ul>
<li>Functional Testing</li>
<ul>
    <li>Deskripsi: Menguji fungsionalitas sistem untuk memastikan aplikasi bekerja sesuai spesifikasi.</li>
    <li>Pendekatan:</li>
        <ul>
            <li>Membuat test case berdasarkan requirement specification.</li>
            <li>Memastikan setiap fungsi memberikan hasil yang benar.</li>
        </ul>
    <li>Contoh:
        Memeriksa apakah fitur pencarian menghasilkan hasil yang sesuai dengan kata kunci.</li>
    <li>Keuntungan:
        Fokus pada pengalaman pengguna.</li>
</ul>
<li>Non-Functional Testing</li>
<ul>
    <li>Deskripsi: Menguji aspek non-fungsional dari aplikasi seperti performa, keamanan, dan kegunaan.</li>
    <li>Pendekatan:
        Melakukan pengujian manual untuk kecepatan, kegunaan, atau daya tahan.</li>
    <li>Contoh:
        Memeriksa waktu yang dibutuhkan halaman untuk dimuat.</li>
    <li>Keuntungan:
        Mengidentifikasi potensi masalah di luar fungsionalitas dasar.</li>
</ul>
<li>Regression Testing</li>
<ul>
    <li>Deskripsi: Menguji kembali aplikasi setelah ada perubahan kode untuk memastikan fitur yang sebelumnya berfungsi masih berjalan dengan baik.</li>
    <li>Pendekatan:</li>
        <ul>
            <li>Menggunakan test case yang telah ada untuk fitur lama.</li>
            <li>Fokus pada area yang terpengaruh oleh perubahan.</li>
        </ul>
    <li>Contoh:
        Memastikan fitur login tetap berfungsi setelah pengembang menambahkan autentikasi dua faktor.</li>
    <li>Keuntungan:
        Menghindari bug baru saat fitur baru ditambahkan.</li>
</ul>
<li>Integration Testing</li>
<ul>
    <li>Deskripsi: Menguji bagaimana modul atau komponen yang berbeda dalam sistem bekerja bersama.</li>
    <li>Pendekatan:</li>
        <ul>
            <li>Top-Down: Menguji modul tingkat tinggi terlebih dahulu.</li>
            <li>Bottom-Up: Menguji modul tingkat rendah terlebih dahulu.</li>
        </ul>
    <li>Contoh:
        Memastikan bahwa data yang dimasukkan di UI frontend diterima dan diproses dengan benar oleh backend.</li>
    <li>Keuntungan:
        Mengidentifikasi masalah komunikasi antar modul.</li>
</ul>
<li>System Testing</li>
<ul>    
    <li>Deskripsi: Menguji seluruh sistem sebagai kesatuan untuk memastikan aplikasi memenuhi persyaratan akhir.</li>
    <li>Pendekatan:
        Menguji semua fungsi utama dan non-fungsional dalam satu lingkungan.</li>
    <li>Contoh:
        Menguji aplikasi e-commerce dari login hingga checkout.</li>
    <li>Keuntungan:
        Memberikan gambaran lengkap tentang kinerja aplikasi.</li>
</ul>

<li>Acceptance Testing</li>
<ul>
    <li>Deskripsi: Dilakukan untuk memastikan bahwa aplikasi memenuhi kebutuhan pengguna akhir atau bisnis sebelum rilis.</li>
    <li>Pendekatan:</li>
        <ul>
            <li>Alpha Testing: Dilakukan oleh tim internal di lingkungan pengujian.</li>
            <li>Beta Testing: Dilakukan oleh pengguna akhir di lingkungan sebenarnya.</li>
        </ul>
    <li>Contoh:
        Meminta pengguna untuk mencoba fitur baru dan memberikan feedback.</li>
    <li>Keuntungan:
        Memberikan validasi akhir sebelum peluncuran.</li>
</ul>
<li>Exploratory Testing</li>
<ul>
    <li>Deskripsi: Pengujian dinamis di mana tester secara aktif mengeksplorasi aplikasi untuk menemukan bug yang tidak terduga.</li>
    <li>Pendekatan:
        <ul>
            <li>Tidak menggunakan test case formal.</li>
            <li>Mengandalkan pengalaman dan intuisi tester.</li>
        </ul>
    <li>Contoh:
        Coba klik tombol beberapa kali dengan cepat untuk melihat apakah aplikasi crash.</li>
    <li>Keuntungan:
        Menemukan bug yang tidak terdeteksi oleh metode lain.</li>
</ul>
<li>Ad-Hoc Testing</li>
<ul>
    <li>Deskripsi: Pengujian tidak terstruktur di mana tester mencoba menemukan bug dengan pendekatan informal dan spontan.</li>
    <li>Pendekatan:
        Tidak ada dokumentasi atau skrip yang dibuat sebelumnya.</li>
    <li>Contoh:
        Mencoba fitur baru tanpa membaca spesifikasi.</li>
    <li>Keuntungan:
        Menghemat waktu untuk pengujian sederhana.</li>
</ul>
</ol>

<h3>Kesimpulan</h3>

Setiap metodologi memiliki tujuan dan kegunaan spesifik dalam siklus pengembangan perangkat lunak. Pilihan metodologi bergantung pada jenis aplikasi, tujuan pengujian, dan ketersediaan sumber daya. Tester sering menggabungkan beberapa metodologi untuk mencapai hasil pengujian yang maksimal.
