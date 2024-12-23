Exploratory Testing adalah metode pengujian yang melibatkan eksplorasi aplikasi secara dinamis tanpa mengikuti skrip pengujian yang telah ditentukan sebelumnya. Tujuannya adalah untuk menemukan potensi masalah, bug yang tidak terduga, atau area perbaikan yang mungkin terlewat oleh pengujian formal.

Berikut adalah contoh kasus penggunaan exploratory testing untuk memastikan kualitas produk:
1. Menguji Formulir Pendaftaran

Skenario:
Anda sedang menguji fitur pendaftaran pengguna pada sebuah aplikasi.

Langkah Explorasi:

    Masukkan karakter spesial dalam field nama (misalnya: @#$%^).
    Masukkan email yang tidak valid (contoh: user@mail atau user@com).
    Gunakan nama yang sangat panjang (lebih dari 100 karakter).
    Biarkan beberapa field kosong lalu klik tombol "Submit".
    Coba klik tombol "Submit" berulang kali untuk melihat apakah aplikasi crash.
    Gunakan input injection seperti SQL (' OR 1=1;--) untuk menguji keamanan.

Tujuan:

    Menemukan bug seperti error handling yang buruk, validasi input yang lemah, atau potensi celah keamanan.

2. Menguji Aplikasi E-Commerce

Skenario:
Anda menguji fitur "Add to Cart" pada aplikasi belanja online.

Langkah Explorasi:

    Tambahkan item yang sama ke keranjang beberapa kali, lalu ubah jumlahnya secara cepat.
    Coba tambahkan item ke keranjang, lalu logout, dan login kembali untuk melihat apakah keranjang masih ada.
    Hapus semua item dari keranjang dan coba checkout.
    Gunakan browser berbeda (Chrome, Firefox, Safari) untuk melihat perbedaan perilaku.
    Ubah kuantitas item ke angka negatif atau angka yang sangat besar (contoh: 99999).

Tujuan:

    Menemukan bug seperti ketidaksesuaian jumlah item, kerusakan data sesi, atau kerentanan UI.

3. Menguji Aplikasi Mobile Banking

Skenario:
Menguji fungsi transfer dana pada aplikasi mobile banking.

Langkah Explorasi:

    Masukkan nomor rekening tujuan yang tidak valid (misalnya: terlalu pendek atau berisi huruf).
    Gunakan jumlah transfer dengan banyak desimal (contoh: 100.12345).
    Lakukan transfer berulang kali dalam waktu yang sangat singkat untuk menguji throttling.
    Ubah pengaturan bahasa aplikasi dan coba transfer kembali.
    Matikan koneksi internet di tengah proses transfer.

Tujuan:

    Mengungkap masalah seperti bug validasi input, performa aplikasi, atau penanganan error jaringan.

4. Menguji API Backend

Skenario:
Menguji API untuk fitur pencarian dalam aplikasi.

Langkah Explorasi:

    Kirim request dengan parameter kosong.
    Masukkan parameter dengan nilai yang tidak sesuai format (contoh: string untuk parameter yang seharusnya integer).
    Kirim payload yang sangat besar untuk melihat bagaimana API menangani input berlebihan.
    Gunakan alat seperti Postman untuk mengirim request simultan ke endpoint yang sama.
    Periksa apakah API mengembalikan respons yang sesuai dengan waktu yang wajar.

Tujuan:

    Menemukan kelemahan dalam validasi parameter, respons waktu, atau stabilitas API.

5. Menguji Aplikasi Media Sosial

Skenario:
Menguji fitur unggah gambar pada aplikasi media sosial.

Langkah Explorasi:

    Unggah file dengan ukuran yang melebihi batas yang diizinkan.
    Unggah file dengan format yang tidak didukung (contoh: .exe).
    Matikan koneksi internet di tengah proses unggah.
    Coba unggah file yang sama berulang kali.
    Lihat bagaimana aplikasi menangani file dengan nama panjang atau karakter spesial.

Tujuan:

    Menemukan bug seperti crash, error handling yang buruk, atau batasan yang tidak diimplementasikan.

Manfaat Exploratory Testing

    Menemukan Bug Tak Terduga: Fokus pada area yang mungkin tidak terjangkau oleh test case biasa.
    Menjaga Kreativitas: Pendekatan bebas memungkinkan QA untuk berpikir di luar kebiasaan.
    Menguji dari Perspektif Pengguna: Mengungkap masalah yang hanya muncul dalam skenario dunia nyata.

Exploratory testing sangat efektif dilakukan pada tahapan akhir pengembangan atau sebelum rilis produk untuk memastikan aplikasi bebas dari masalah kritis.
