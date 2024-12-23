Test Data adalah data yang digunakan selama proses pengujian untuk memastikan aplikasi bekerja seperti yang diharapkan. Data ini bisa berupa data input (masukan) yang digunakan untuk menguji fitur atau data lingkungan yang mencerminkan kondisi sistem nyata. Berikut adalah panduan tentang cara membuat dan menggunakan Test Data:
Langkah-Langkah Membuat Test Data
1. Pahami Persyaratan Tes

    Tinjau dokumen spesifikasi, user stories, atau test case.
    Identifikasi jenis data yang diperlukan untuk setiap skenario (contoh: data valid, data invalid, data batas).

    Contoh: Jika menguji fitur pendaftaran pengguna, Anda mungkin membutuhkan:

    -Email yang valid
    -Email yang sudah digunakan
    -Format email yang salah (tanpa simbol @, domain tidak lengkap, dll.)

2. Tentukan Sumber Data

    -Manual Input: Data dibuat secara manual berdasarkan kebutuhan pengujian.
    -Database: Mengambil data langsung dari database sistem (dengan izin yang tepat).
    -Generator Data Otomatis: Menggunakan alat untuk membuat data uji (contoh: Mockaroo, Faker.js).
    -Data Riil: Menggunakan data nyata (anonymized) untuk skenario yang lebih kompleks.

3. Klasifikasikan Jenis Data
    Bagi data sesuai dengan jenis pengujian:

    -Data Valid: Data yang memenuhi semua persyaratan sistem.
        Contoh: Nama pengguna dengan panjang antara 5–20 karakter.
    -Data Invalid: Data yang melanggar aturan sistem.
        Contoh: Nama pengguna dengan simbol seperti @!#.
    -Data Boundary: Data yang berada di batas validasi.
        Contoh: Nama dengan panjang tepat 5 dan 20 karakter.
    -Data Non-Fungsional: Data untuk menguji beban atau stres sistem.
        Contoh: 10.000 entri untuk menguji kapasitas database.

4. Buat Template atau Dataset

    Gunakan spreadsheet untuk menyusun data yang mudah dipahami.
        -Kolom: Input, Expected Output, Remarks
        -Baris: Setiap skenario pengujian.

Contoh Template:
<table>
<tr><td>Input</td><td>Expected Output</td><td>Remarks</td></tr>
<tr><td>user@mail.com</td><td>Sukses pendaftaran</td><td>Data valid</td></tr>
<tr><td>usermail.com</td><td>Gagal: Format tidak valid</td><td>Email tanpa '@'</td></tr>
<tr><td>user@mail.com</td><td>Gagal: Email sudah ada</td><td>Data duplikat di database</td></tr>
</table>
5. Gunakan Alat untuk Membuat Data Otomatis

Beberapa alat populer untuk menghasilkan Test Data:

    Mockaroo: Membuat dataset acak berbasis format yang ditentukan.
    Faker.js: Library JavaScript untuk membuat data palsu seperti nama, alamat, email.
    Postman: Membuat data dinamis untuk pengujian API.
    SQL Queries: Membuat skrip untuk memasukkan data langsung ke database.

6. Pertimbangkan Data yang Dihapus atau Dimodifikasi
    Pastikan data tidak berdampak pada lingkungan pengujian atau data riil.
    Gunakan data dummy untuk mencegah kebocoran informasi sensitif.
    Contoh: Untuk data pelanggan, gunakan data anonimisasi (mengubah nama asli menjadi acak).

    Contoh Skenario Membuat Test Data

    Skenario: Menguji formulir pendaftaran pengguna.
    Langkah:

        1. Identifikasi input formulir: Nama, Email, Kata Sandi, Nomor Telepon.
        2. Tentukan aturan validasi:
            Nama: 5-20 karakter, tanpa simbol.
            Email: Format email valid.
            Kata Sandi: Minimal 8 karakter, mengandung angka dan huruf besar.
            Nomor Telepon: 10 digit, tanpa spasi atau simbol.
        3. Buat dataset:
            Valid: JohnDoe, john.doe@mail.com, Password123, 08123456789.
            Invalid:
                Nama: J@hn, J.
                Email: johnmail.com.
                Kata Sandi: pass, 12345678.
                Nomor Telepon: 08123abcd.

<h3>Tips</h3>

    -Simpan dataset dalam file terpisah (Excel, CSV, JSON) untuk kemudahan penggunaan ulang.
    -Automasi pembuatan data untuk skenario kompleks.
    -Selalu uji data Anda di lingkungan pengujian terlebih dahulu untuk menghindari masalah di produksi.
