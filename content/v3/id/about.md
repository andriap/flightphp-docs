# Flight PHP Framework

Flight adalah framework PHP yang cepat, sederhana, dan dapat diperluas—dibangun untuk pengembang yang ingin menyelesaikan pekerjaan dengan cepat, tanpa kerumitan. Saat Anda membangun aplikasi web klasik, API yang sangat cepat, atau bereksperimen dengan alat berbasis AI terbaru, desain sederhana dan ringan Flight membuatnya cocok dan sempurna. Flight dirancang untuk tetap ramping, namun tetap dapat memenuhi persyaratan arsitektur enterprise.

## Mengapa Memilih Flight?

- **Ramah untuk Pemula:** Flight bisa menjadi titik awal yang bagus untuk pengembang PHP baru. Strukturnya yang jelas dan sintaks sederhana membantu Anda belajar mengembangkan aplikasi berbasis web tanpa harus bingung dengan kode _boilerplate_.
- **Disukai oleh Profesional:** Pengembang berpengalaman menyukai Flight karena fleksibilitas dan kendalinya. Anda dapat mengembangkan dari prototipe kecil hingga aplikasi lengkap tanpa harus mengganti framework.
- **Kompatibel ke Belakang:** Kami menghargai waktu Anda. Flight v3 adalah peningkatan dari v2, dengan mempertahankan hampir seluruh API yang sama. Kami percaya pada evolusi, bukan revolusi—tidak ada lagi "merusak dunia" setiap kali versi utama baru dirilis.
- **Tanpa Dependensi:** Framework inti Flight bebas dependensi—tanpa _polyfills_, tanpa paket eksternal, bahkan tanpa PSR _interface_. Ini berarti vektor serangan lebih sedikit, lebih ringan, dan tidak ada perubahan yang mengejutkan ketika ada masalah pada dependensi. Plugin opsional mungkin menyertakan dependensi, tetapi framework inti Flight akan selalu tetap ramping dan aman.
- **Berfokus pada AI:** Flight dengan arsitektur yang bersih dan beban tambahan minimal, membuatnya ideal untuk diintegrasikan dengan alat maupun API AI. Ketika Anda membangun _chatbot_ pintar, dashboard berbasis AI, atau hanya ingin bereksperimen, Flight tidak mengganggu Anda untuk tetap fokus pada hal yang penting. Aplikasi [kerangka](https://github.com/flightphp/skeleton) sudah dilengkapi dengan file instruksi siap pakai untuk asisten pengkodean AI! [Pelajari lebih lanjut tentang menggunakan AI dengan Flight](/learn/ai)

## Video Gambaran Umum

<div class="flight-block-video">
  <div class="row">
    <div class="col-12 col-md-6 position-relative video-wrapper">
      <iframe class="video-bg" width="100vw" height="315" src="https://www.youtube.com/embed/VCztp1QLC2c?si=W3fSWEKmoCIlC7Z5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <div class="col-12 col-md-6 fs-5 text-center mt-5 pt-5">
      <span class="flight-title-video">Cukup sederhana, bukan?</span>
      <br>
      <a href="https://docs.flightphp.com/learn">Pelajari lebih lanjut</a> tentang Flight di dokumentasi!
    </div>
  </div>
</div>

## Mulai dengan Cepat

Untuk instalasi cepat tanpa tambahan, instal dengan Composer:

```bash
composer require flightphp/core
```

Atau Anda dapat mengunduh zip dari repo [di sini](https://github.com/flightphp/core). Kemudian Anda akan memiliki berkas `index.php` sederhana seperti berikut:

```php
<?php

// if installed with composer
require 'vendor/autoload.php';
// or if installed manually by zip file
// require 'flight/Flight.php';

Flight::route('/', function() {
  echo 'hello world!';
});

Flight::route('/json', function() {
  Flight::json([
	'hello' => 'world'
  ]);
});

Flight::start();
```

Itu saja! Anda memiliki aplikasi Flight sederhana. Anda sekarang dapat menjalankan file ini dengan `php -S localhost:8000` dan kunjungi `http://localhost:8000` di browser Anda untuk melihat hasilnya.

## Kerangka/Template Aplikasi

Ada aplikasi contoh untuk membantu Anda memulai proyek dengan Flight. Aplikasi kerangka ini memiliki tata letak terstruktur, konfigurasi dasar yang sudah diatur, dan skrip composer yang siap digunakan! Lihat [flightphp/skeleton](https://github.com/flightphp/skeleton) untuk proyek siap pakai, atau kunjungi halaman [contoh](/examples) untuk inspirasi. Ingin melihat bagaimana Flight cocok dengan AI? [Jelajahi contoh berbasis AI](/learn/ai).

## Install Aplikasi Kerangka

Cukup mudah!

```bash
# Create the new project
composer create-project flightphp/skeleton my-project/
# Enter your new project directory
cd my-project/
# Bring up the local dev-server to get started right away!
composer start
```

Ini akan membuat struktur proyek, menyiapkan file yang Anda butuhkan, dan Anda siap untuk memulai!

## Performa Tinggi

Flight adalah salah satu framework PHP tercepat. Dengan kode inti ringan berarti beban lebih sedikit dan kecepatan lebih tinggi—sempurna untuk aplikasi tradisional maupun proyek berbasis AI modern. Anda dapat melihat semua _benchmark_ di [TechEmpower](https://www.techempower.com/benchmarks/#section=data-r18&hw=ph&test=frameworks)

Lihat benchmark Flight dengan beberapa framework PHP populer lainnya di bawah ini.

| Framework | Plaintext Reqs/sec | JSON Reqs/sec |
| --------- | ------------ | ------------ |
| Flight      | 190,421    | 182,491 |
| Yii         | 145,749    | 131,434 |
| Fat-Free    | 139,238    | 133,952 |
| Slim        | 89,588     | 87,348  |
| Phalcon     | 95,911     | 87,675  |
| Symfony     | 65,053     | 63,237  |
| Lumen       | 40,572     | 39,700  |
| Laravel     | 26,657     | 26,901  |
| CodeIgniter | 20,628     | 19,901  |


## Flight dan AI

Penasaran bagaimana Flight menangani AI? [Temukan](/learn/ai) bagaimana Flight membuat bekerja dengan LLM favorit Anda menjadi mudah!

## Stabilitas dan Kompatibilitas Ke Belakang

Kami menghargai waktu Anda. Kami semua pernah melihat framework yang sepenuhnya menciptakan ulang diri mereka setiap beberapa tahun, meninggalkan pengembang dengan kode rusak dan migrasi mahal. Flight berbeda. Flight v3 dirancang sebagai peningkatan dari v2, yang berarti API yang Anda kenal dan sukai tidak dihilangkan. Bahkan, sebagian besar proyek v2 akan berfungsi tanpa perubahan apa pun di v3.

Kami berkomitmen untuk menjaga Flight tetap stabil sehingga Anda dapat fokus membangun aplikasi Anda, bukan memperbaiki framework Anda.

# Komunitas

Kami ada di Matrix Chat

[![Matrix](https://img.shields.io/matrix/flight-php-framework%3Amatrix.org?server_fqdn=matrix.org&style=social&logo=matrix)](https://matrix.to/#/#flight-php-framework:matrix.org)

Dan Discord

[![](https://dcbadge.limes.pink/api/server/https://discord.gg/Ysr4zqHfbX)](https://discord.gg/Ysr4zqHfbX)

# Berkontribusi

Ada dua cara Anda dapat berkontribusi ke Flight:

1. Berkontribusi ke framework inti dengan mengunjungi [core repository](https://github.com/flightphp/core).
2. Bantu membuat dokumentasi lebih baik! Situs web dokumentasi ini dihosting di [Github](https://github.com/flightphp/docs). Jika Anda menemukan kesalahan atau ingin meningkatkan sesuatu, jangan ragu untuk mengirimkan pull request. Kami menyukai pembaruan dan ide baru—terutama seputar AI dan teknologi baru!

# Persyaratan

Flight memerlukan PHP 7.4 atau lebih tinggi.

**Catatan:** PHP 7.4 didukung karena pada saat penulisan ini (2024) PHP 7.4 adalah versi default untuk beberapa distribusi Linux LTS. Memaksa perpindahan ke PHP >8 akan menyebabkan banyak masalah bagi pengguna tersebut. Framework juga mendukung PHP >8.

# Lisensi

Flight dirilis di bawah lisensi [MIT](https://github.com/flightphp/core/blob/master/LICENSE).
