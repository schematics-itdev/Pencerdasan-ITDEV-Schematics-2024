# Pencerdasan-ITDEV-Schematics-2024

## Daftar Isi

- [Pencerdasan-ITDEV-Schematics-2024](#pencerdasan-itdev-schematics-2024)
  - [Daftar Isi](#daftar-isi)
  - [Workflow](#workflow)
  - [Tech Stack](#tech-stack)
    - [Next JS](#next-js)
      - [Data Fetching](#data-fetching)
      - [SSR dan CSR](#ssr-dan-csr)
    - [TypeScript](#typescript)
      - [Perbedaan TypeScript dan JavaScript](#perbedaan-typescript-dan-javascript)
    - [React Hook Form](#react-hook-form)
      - [Kelebihan React Hook Form](#kelebihan-react-hook-form)
    - [Zustand](#zustand)
    - [React Query](#react-query)
  - [Express](#express)
    - [Routing](#routing)
    - [Middleware](#middleware)
    - [Controller](#controller)
    - [Service](#service)
    - [Repository](#repository)
  - [Prisma](#prisma)
  - [PostgreSQL (Supabase)](#postgresql-supabase)
  - [Layouting](#layouting)
  - [Design System](#design-system)
  - [Clean Code](#clean-code)
  - [Git \& Github](#git--github)
    - [Git](#git)
    - [GitHub](#github)
  - [Issues dan Project](#issues-dan-project)
  - [Git Branch](#git-branch)
  - [Git Commit dan Push:](#git-commit-dan-push)
  - [Pull Request](#pull-request)

## Workflow

Workflow Schematics 2024 menggunakan sistem agile project management yang terdiri dari sprint dan scrum.

## Tech Stack

### TypeScript

TypeScript adalah bahasa pemrograman open-source yang dikembangkan oleh Microsoft. TypeScript adalah `superset` dari JavaScript, yang berarti semua sintaksis dan fitur JavaScript juga tersedia di TypeScript, tetapi dengan penambahan kemampuan `tipe` (type) yang lebih kuat.

Kelebihan TypeScript antara lain:

1. Kemampuan tipe yang lebih kuat, sehingga kode menjadi lebih terstruktur dan mudah dipahami, serta memungkinkan untuk mendeteksi kesalahan pada saat kompilasi.
2. Meningkatkan produktivitas pengembang dengan memungkinkan otomatisasi refaktorisasi kode, dukungan untuk refactor yang lebih aman, dan fitur editor IntelliSense yang canggih.
3. TypeScript menawarkan fitur-fitur modern seperti async/await, dekorator, dan banyak lagi.
4. Lebih mudah untuk melakukan debugging kode TypeScript.

Kekurangan TypeScript antara lain:

1. Tidak semua pengembang atau tim pengembangan mengerti TypeScript, sehingga membutuhkan waktu belajar yang lebih lama.
2. Kode TypeScript memerlukan waktu kompilasi lebih lama daripada kode JavaScript biasa, karena memerlukan tahap kompilasi tambahan.
3. Kurangnya dukungan untuk beberapa pustaka JavaScript, terutama pustaka yang belum ditingkatkan ke TypeScript atau pustaka yang kurang populer.

#### Perbedaan TypeScript dan JavaScript

TypeScript dan JavaScript adalah dua bahasa pemrograman yang saling terkait, namun memiliki perbedaan-perbedaan berikut ini:

1. Tipe Data</br>
   JavaScript merupakan bahasa pemrograman yang bersifat dinamis, sehingga tipe data variabel bisa berubah-ubah sepanjang program berjalan. Sementara itu, TypeScript merupakan bahasa pemrograman yang statis, sehingga tipe data variabel harus didefinisikan pada saat penulisan kode.
2. Kompilasi </br>
   JavaScript dieksekusi secara langsung oleh browser atau runtime environment lainnya, sedangkan TypeScript harus dikompilasi terlebih dahulu menjadi JavaScript sebelum bisa dijalankan.
3. Fitur Baru </br>
   TypeScript memiliki fitur-fitur baru yang belum tersedia pada JavaScript, seperti interface, generic, union type, dan lain-lain.

Untuk memahami lebih detail tentang TypeScript, silahkan kunjungi [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/) untuk melihat dokumentasi lengkapnya.
Atau bisa juga kunjungi
https://youtube.com/playlist?list=PLNqp92_EXZBJ4CBroxVBJEpAXoz1g-naZ untuk melihat video tutorial lengkapnya.

## Express

Express adalah framework backend. Artinya, ia bertanggung jawab untuk mengatur fungsionalitas website, seperti pengelolaan routing dan session, permintaan HTTP, penanganan error, serta pertukaran data di server.

Beberapa fungsionalitas dari Express antara lainnya adalah

#### Routing

Routing adalah metode yang digunakan website (server) untuk merespons permintaan dari browser (client). Misalnya, permintaan untuk menampilkan halaman tertentu.

Cara kerja routing di Express adalah dengan sebuah metode bernama `app`. Metode tersebut akan merespons setiap permintaan berbentuk HTTP. Misalnya GET, POST, PUT, dan DELETE.

#### Middleware

Middleware adalah fungsi yang digunakan untuk mengakses permintaan object (req), respons object (res), dan setiap siklus permintaan dan respon tersebut (next).

Pada Express, cara kerja Middleware adalah dengan mengeksekusi setiap skrip, membuat perubahan terhadap permintaan dan respons object, mengakhiri siklus permintaan-respons, lalu menyiapkan Middleware untuk siklus berikutnya.

#### Controller

Controller adalah bagian yang menangani HTTP request yang masuk dan mengembalikan HTTP response yang sesuai. Controller bertindak sebagai perantara antara client dan server-side logic, menangani request yang masuk, memprosesnya, dan mengembalikan response yang sesuai.

#### Service

Implementasi service pada Express mendefinisikan dan merangkum seluruh business entity agar mudah diuji, dapat digunakan kembali, dan tidak bergantung pada infrastruktur atau teknologi tertentu. Lapisan ini tidak boleh bergantung pada external component seperti database atau API, dan hanya boleh berinteraksi dengannya melalui abstraksi.

#### Repository

Repository memiliki peran untuk melakukan abstraksi data layer dari aplikasi dan memberikan jalan untuk melakukan operasi data, tanpa perlu mengetahui bagaimana data itu disimpan maupun diambil.

Repository menggunakan metode-metode operasi CRUD (Create, Read, Update, Delete) untuk melakukan Query dan manipulasi data. Repository memungkinkan aplikasi untuk memecah instruksi-instruksi penyimpanan data, yang membuatnya lebih reliable, mudah di-scale, dan dimaintain, karena perubahan instruksi penyimpanan data tidak mempengaruhi aplikasi.

Penggunaan Repository pada Express acapkali digabungkan dengan penggunaan ORM (Prisma, Drizzle, Sequelize) yang memberikan kemudahan untuk melakukan manipulasi ataupun instruksi pengambilan data, dengan fitur tambahan seperti pengamanan Query, performa yang menjanjikan, dan kemudahan penggunaan Query.

## Prisma

Prisma Database adalah ORM (Object-Relational Mapping) generasi berikutnya yang dirancang khusus untuk Node.js dan TypeScript. ORM adalah teknik yang memungkinkan pengembang untuk bekerja dengan basis data relasional menggunakan objek dan kode pemrograman daripada menulis kueri SQL secara manual. Prisma Database mempermudah interaksi dengan berbagai jenis database seperti PostgreSQL, MySQL, SQLite, dan SQL Server.

Dengan Prisma Database, kita dapat dengan mudah membuat skema database menggunakan sintaks yang intuitif. Prisma akan secara otomatis menghasilkan kueri SQL yang diperlukan untuk mengakses dan memanipulasi data. Ini menghemat waktu dan usaha dalam penulisan kueri SQL secara manual, serta mengurangi risiko kesalahan manusia.

## PostgreSQL (Supabase)

PostgreSQL adalah sistem manajemen basis data relasional (RDBMS) yang memiliki kemampuan untuk memproses data yang besar dan kompleks. PostgreSQL dikembangkan oleh komunitas pengembang yang bekerja sama untuk menghasilkan software open-source yang kuat dan fleksibel. PostgreSQL mampu menjalankan berbagai macam aplikasi, dari aplikasi desktop hingga sistem backend yang digunakan oleh perusahaan-perusahaan besar.

PostgreSQL menggunakan arsitektur client-server, di mana server PostgreSQL berjalan sebagai proses yang terpisah dari aplikasi klien. Ketika aplikasi klien membutuhkan akses ke data di dalam basis data, itu mengirim permintaan ke server PostgreSQL. Server PostgreSQL kemudian memproses permintaan tersebut dan mengirimkan hasil kembali ke aplikasi klien.

## Git & Github

### Git

Git adalah version control system yang bertugas untuk mencatat setiap perubahan pada file. Git memiliki fungsi untuk mengelola versi source code. Git sangat penting digunakan pada sebuah projek yang dikerjakan oleh banyak orang karena git dapat membuat salinan kode yang dapat dimodifikasi tanpa mengubah dan mengganggu versi utama dari kode tersebut. Karena itu, tim yang bekerja untuk mengembangkan sebuah fitur, atau memperbaiki dapat bekerja secara pisah dan menggabungkannya kembali kepada kode utama

Git commands dasar yang biasa digunakan contohnya adalah add, commit, pull, dan push.

### GitHub

GitHub adalah tempat yang digunakan untuk menyimpan dan mengelola kode suatu project. GitHub dan git saling berhubungan, karena git menyimpan data hanya di local komputer kita saja, sedangkan github bisa menyimpan kode kita yang dapat diakses oleh banyak orang.

## Issues dan Project

Pada issues kalian dapat melihat tugas yang diberikan ke kalian, dan branch yang akan kalian gunakan untuk mengerjakan tugas tersebut. Kalian dapat melihat deadline tugas pada bagian Project. Jangan lupa keep track progress kalian di project seperti mengubah status todo menjadi in progress, dll.

## Git Branch

Kalian akan mengerjakan tugas yang diberikan pada branch yang seusai dengan Issue yang diberikan pada kalian. Untuk berpindah branch kalian dapat menggunakan perintah `git checkout -b` untuk beralih ke cabang lain:

```
git checkout -b nama_branch
```

## Git Commit dan Push:

Setelah melakukan perubahan, kalian harus melakukan commit untuk menyimpan perubahan tersebut secara lokal, dan kemudian push perubahan ke repo. Gunakan perintah berikut:

```
git add .
git commit -m "Pesan commit Anda di sini"
git push
```

Link contoh conventional commit:
https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13

## Pull Request

Setelah task yang kalian kerjakan selesai dan sudah di push ke repo, langkah selanjutnya adalah melakukan pull request. Dan meminta review kepada staff ahli.

Ketika pada review tersebut revisi, maka lakukanlah revisi sesusai dengan apa yang diminta.
Jika kalian sudah selesai mengerjakan revisi tersebut, ulangi langkah Commit dan push.
Dan kalian dapat menuggu kembali apakah revisi kalian di acc.
