# Soal test maggang Backend engineer dengan Springboot

Berikut adalah soal/pertanyaan yang perlu dijawab oleh peserta maggang

## knowledge base

1. Apa yang anda ketahui tentang Rest API?
   Jawaban : Rest API merupakan protokol yang biasanya ada dalam pengembangan web yang berfungsi sebagai alat interaksi antara klien dan server.Klien dapat melakukan operasi CRUD (Create, Read, Update, Delete) pada sumber daya tersebut melalui permintaan HTTP seperti GET, POST, PUT, DELETE, dan sebagainya.

2. Apa yang anda ketahui tentang Server side and Client side processing?
   Jawaban: Server-side processing dan client-side processing merupakan konsep-konsep penting dalam pengembangan aplikasi web. Kedua konsep tersebut berkaitan dengan cara pemrosesan data dan logika aplikasi, baik di sisi server maupun di sisi klien.Server-side processing terjadi ketika pemrosesan data dan logika aplikasi berlangsung di server. Dalam model ini, permintaan dan respons diolah sepenuhnya di server dan hanya hasil akhir yang dikirimkan ke klien. Contoh penggunaan server-side processing adalah mengambil data dari database, memproses data tersebut, dan menghasilkan output HTML atau data JSON. Sementara itu, client-side processing terjadi ketika pemrosesan data dan logika aplikasi terjadi di sisi klien. Dalam model ini, kode aplikasi diunduh ke browser klien dan dijalankan di sana. Hal ini memungkinkan aplikasi untuk merespons input pengguna secara real-time tanpa memerlukan permintaan ke server. Contoh penggunaan client-side processing adalah validasi formulir, manipulasi DOM, animasi, dan pemrosesan data yang didapat dari API.

3. Apa yang anda ketahui tentang Monolith dan Microservices, berikan contohnya?
   Jawaban: Monolith dan Microservices adalah dua arsitektur pengembangan perangkat lunak yang berbeda dalam pendekatan pengorganisasian dan pembangunan aplikasi. Monolith adalah arsitektur yang mengorganisasi seluruh aplikasi dalam satu kesatuan besar yang tidak dapat dibagi menjadi bagian-bagian yang lebih kecil. Dalam arsitektur Monolith, aplikasi dibangun sebagai satu kesatuan yang utuh, di mana seluruh komponen berjalan dalam satu proses dan dijalankan dalam satu server. Contoh Beberapa perusahaan teknologi besar yang menerapkan monolith adalah Facebook, Google, dan Amazon sebagian besar menggunakan arsitektur Monolith dalam pengembangan aplikasi mereka.Sedangkan Microservices adalah arsitektur yang mengorganisasi aplikasi menjadi beberapa layanan kecil dan terpisah yang berkomunikasi satu sama lain melalui protokol jaringan. Setiap layanan memiliki tugas spesifik dan dijalankan sebagai proses terpisah. Hal ini memungkinkan pengembang untuk membangun, menguji, dan memperbarui setiap layanan secara independen. Contoh Beberapa perusahaan teknologi besar yang menerapkan microservice adalah PT. Tokopedia,Netflix, Spotify, dan Uber menerapkan arsitektur Microservices dalam pengembangan aplikasi mereka.

4. Apa yang anda ketahui tentang Design pattern inversion of Control serta Dependency Injection?
   Jawaban: Inversion of Control (IoC) dan Dependency Injection (DI) adalah konsep yang sangat penting dalam desain perangkat lunak yang terkait dengan cara komponen-komponen aplikasi saling berinteraksi. Keduanya adalah Design Pattern yang digunakan untuk memudahkan manajemen ketergantungan antar komponen dalam sebuah sistem. Inversion of Control (IoC) adalah sebuah konsep di mana kontrol alur eksekusi sebuah aplikasi dipindahkan dari komponen aplikasi itu sendiri ke suatu framework atau container. Dalam model ini, suatu framework atau container bertanggung jawab untuk mengendalikan alur eksekusi aplikasi dan mengelola ketergantungan antar komponen. Konsep IoC memudahkan pengembang untuk memperbarui atau mengganti komponen aplikasi tanpa perlu memperhatikan bagaimana ketergantungan antar komponen diatur. Dependency Injection (DI) adalah sebuah konsep yang terkait dengan IoC di mana objek-objek yang saling berinteraksi disediakan (injected) oleh framework atau container, bukan dibuat secara langsung oleh objek yang membutuhkan. Dalam DI, komponen aplikasi tidak lagi bertanggung jawab untuk menciptakan atau menemukan objek yang dibutuhkan, melainkan hanya mendefinisikan ketergantungan dan mempercayakan container untuk menyediakan objek tersebut. Dengan menggunakan DI, ketergantungan antar komponen dapat dikelola dengan lebih mudah dan sistem menjadi lebih fleksibel dan modular.

5. Apa yang anda ketahui tentang Java programming dan Spring framework khususnya spring-boot?
   Jawaban: Java programming adalah bahasa pemrograman yang digunakan untuk mengembangkan berbagai macam aplikasi, mulai dari aplikasi desktop hingga aplikasi web, mobile, dan enterprise. Java memiliki sintaks yang mudah dipahami dan jelas, sehingga memudahkan pengembang untuk membangun aplikasi yang kompleks. Spring Framework adalah kerangka kerja (framework) yang populer untuk pengembangan aplikasi berbasis Java. Spring Framework menyediakan berbagai fitur dan layanan yang membantu pengembang untuk membangun aplikasi secara cepat dan efektif. Beberapa fitur yang disediakan oleh Spring Framework meliputi Inversion of Control (IoC), Dependency Injection (DI), dan AOP (Aspect Oriented Programming). Spring Boot adalah proyek turunan dari Spring Framework yang dirancang untuk mempermudah pengembangan aplikasi dengan Spring Framework. Spring Boot memungkinkan pengembang untuk membuat aplikasi yang berdiri sendiri (self-contained) dengan mudah, tanpa harus mengatur konfigurasi dan dependensi secara manual. Spring Boot juga menyediakan berbagai fitur untuk pengembangan aplikasi web dan mikro-servis, seperti pengaturan database, manajemen dependensi, dan penggunaan endpoint RESTful. Dalam praktiknya, Spring Boot sering digunakan untuk membangun aplikasi web berbasis mikro-servis dengan arsitektur Microservices.
   
   Tambahan: Alasan saya memilih menggunakan module microservice dari e-commerce seperti Tokopedia. Karena penggunaan arsitektur microservices menjadi sangat relevan bagi Tokopedia yang memiliki jumlah transaksi yang sangat besar dan kompleksitas sistem yang tinggi. Dan juga Dalam arsitektur microservices, setiap layanan dapat ditangani secara independen. Jika terjadi kesalahan pada satu layanan, layanan lainnya masih dapat berjalan normal dan tidak terpengaruh. Ini memungkinkan untuk meminimalkan dampak dari kesalahan yang terjadi pada sistem.


## Design modules

Dalam suatu schenario ada requirement membuat aplikasi e-commerse seperti Tokopedia seperti berikut:

1. Catalog, pelanggan mencari product di toko
    ![catalog](imgs/catalog.png)
2. Item, bisa melihat detail informasi produk
    ![items](imgs/item.png)
3. Cart, pelanggan bisa menambahkan produk yang ingin di beli ke keranjang
    ![cart](imgs/cart.png)
4. Setelah di checkout, masuk ke list transaction
    ![list-transaction](imgs/list-transaction.png)
5. Kita juga bisa liat detail transactionya
    ![detail-transaction](imgs/detail-transaction.png)

Kemudian temen-temen buat design database, module (monolith/microservices) berdasarkan gambar atau schenario tersebut. Serta jelakan mengapa menggunakan design tersebut.

## Praktek

Berdasarkan analisa tersebut, buat project monorepo (pada repository ini) dengan menggunakan framework springboot seperti berikut specifikasinya:

- Database: `PostgreSQL 15`
- JDK version: `Oracle JDK 17 or later`
- Springboot version: `3.0.x`

terkait design system Toko, Barang, Pembelian pada ecommerse tersebut.