Exploratory Testing adalah metode pengujian yang melibatkan eksplorasi aplikasi secara dinamis tanpa mengikuti skrip pengujian yang telah ditentukan sebelumnya. Tujuannya adalah untuk menemukan potensi masalah, bug yang tidak terduga, atau area perbaikan yang mungkin terlewat oleh pengujian formal.

Berikut adalah contoh kasus penggunaan exploratory testing untuk memastikan kualitas produk:
<ol><li>Menguji Formulir Pendaftaran</li>

Skenario: Anda sedang menguji fitur pendaftaran pengguna pada sebuah aplikasi.

Langkah Explorasi:
    <ul>
    <li>Masukkan karakter spesial dalam field nama (misalnya: @#$%^).</li>
    <li>Masukkan email yang tidak valid (contoh: user@mail atau user@com).</li>
    <li>Gunakan nama yang sangat panjang (lebih dari 100 karakter).</li>
    <li>Biarkan beberapa field kosong lalu klik tombol "Submit".</li>
    <li>Coba klik tombol "Submit" berulang kali (SPAM CLICK) untuk melihat apakah aplikasi crash.</li>
    <li>Gunakan input injection seperti SQL (' OR 1=1;--) untuk menguji keamanan.</li>
    </ul>

Tujuan:

    Menemukan bug seperti error handling yang buruk, validasi input yang lemah, atau potensi celah keamanan.

<li>Menguji Aplikasi E-Commerce</li>

Skenario: Anda menguji fitur "Add to Cart" pada aplikasi belanja online.

Langkah Explorasi:
    <ul>
        <li>Tambahkan item yang sama ke keranjang beberapa kali, lalu ubah jumlahnya secara cepat.</li>
        <li>Coba tambahkan item ke keranjang, lalu logout, dan login kembali untuk melihat apakah keranjang masih ada.</li>
        <li>Hapus semua item dari keranjang dan coba checkout.</li>
        <li>Gunakan browser berbeda (Chrome, Firefox, Safari) untuk melihat perbedaan perilaku.</li>
        <li>Ubah kuantitas item ke angka negatif atau angka yang sangat besar (contoh: 99999).</li>
    </ul>
Tujuan:

    Menemukan bug seperti ketidaksesuaian jumlah item, kerusakan data sesi, atau kerentanan UI.

<li>Menguji Aplikasi Mobile Banking</li>

Skenario: Menguji fungsi transfer dana pada aplikasi mobile banking.

Langkah Explorasi:
    <ul>
        <li>Masukkan nomor rekening tujuan yang tidak valid (misalnya: terlalu pendek atau berisi huruf).</li>
        <li>Gunakan jumlah transfer dengan banyak desimal (contoh: 100.12345).</li>
        <li>Lakukan transfer berulang kali dalam waktu yang sangat singkat untuk menguji throttling.</li>
        <li>Ubah pengaturan bahasa aplikasi dan coba transfer kembali.</li>
        <li>Matikan koneksi internet di tengah proses transfer.</li>

Tujuan:

    Mengungkap masalah seperti bug validasi input, performa aplikasi, atau penanganan error jaringan.

<li>Menguji API Backend</li>

Skenario: Menguji API untuk fitur pencarian dalam aplikasi.

Langkah Explorasi:
    <ul>
        <li>Kirim request dengan parameter kosong.</li>
        <li>Masukkan parameter dengan nilai yang tidak sesuai format (contoh: string untuk parameter yang seharusnya integer).</li>
        <li>Kirim payload yang sangat besar untuk melihat bagaimana API menangani input berlebihan.</li>
        <li>Gunakan alat seperti Postman untuk mengirim request simultan ke endpoint yang sama.</li>
        <li>Periksa apakah API mengembalikan respons yang sesuai dengan waktu yang wajar.</li>
    </ul>
Tujuan:

    Menemukan kelemahan dalam validasi parameter, respons waktu, atau stabilitas API.

<li>Menguji Aplikasi Media Sosial</li>

Skenario: Menguji fitur unggah gambar pada aplikasi media sosial.

Langkah Explorasi:
    <ul>
        <li>Unggah file dengan ukuran yang melebihi batas yang diizinkan.</li>
        <li>Unggah file dengan format yang tidak didukung (contoh: .exe).</li>
        <li>Matikan koneksi internet di tengah proses unggah.</li>
        <li>Coba unggah file yang sama berulang kali.</li>
        <li>Lihat bagaimana aplikasi menangani file dengan nama panjang atau karakter spesial.</li>

Tujuan:

    Menemukan bug seperti crash, error handling yang buruk, atau batasan yang tidak diimplementasikan.

Manfaat Exploratory Testing

    Menemukan Bug Tak Terduga: Fokus pada area yang mungkin tidak terjangkau oleh test case biasa.
    Menjaga Kreativitas: Pendekatan bebas memungkinkan QA untuk berpikir di luar kebiasaan.
    Menguji dari Perspektif Pengguna: Mengungkap masalah yang hanya muncul dalam skenario dunia nyata.

<h3>Kesimpulan:</h3>
Exploratory testing sangat efektif dilakukan pada tahapan akhir pengembangan atau sebelum rilis produk untuk memastikan aplikasi bebas dari masalah kritis.
</ol>
