# adityaTugas_6.github.io

### Node JS - NPM
#### * _. NPM adalah singkatan dari Node Package Manager. NPM adalah sebuah tools yang otomatis terinstal jika anda menginstal Node JS. Manfaat dari NPM ini adalah untuk menginstal modul/library – library yang dimiliki Node JS dan juga untuk menjalankan script pada command line, Cara Kerja NPM:_
````
* Sebagai repositori untuk menerbitkan project open-source Node.js. Yang berarti, 
  platform ini menjadi wadah offline dimana siapapun dapat menerbitkan
  dan membagikan tool yang ditulis dengan JavaScript.
* Npm adalah tool command line yang dapat menyalurkan interaksi pada platform online, 
  contohnya browser dan server. Utilitas ini dapat menginstal dan uninstal package, 
  mengelola versi dan dependensi yang diperlukan untuk menjalankan proyek.
````

#####  - Initation Npm
###### * _Melakukan inisialisasi NPM pada project, pertama masuk ke folder project yang akan memakai NPM atau bisa dengan membuat folder project baru_
````
- Buka Terminal
- mkdir 'Folder yang akan dibuat'
- cd 'masuk ke folder yang telah dibuat'
- npm init -y
````

##### - Package Json
###### * _File package.json adalah file yang berisi keterangan dari project Javascript, seperti: judul project, deskripsi, versi, library yang dibutuhkan, dan script untuk mengeksekusi project. File ini akan dibutuhkan oleh npm dan yarn. Secara sederhana, file package.json dapat diibaratkan seperti SOP yang akan diikuti oleh npm dan yarn dalam membangun (build) project_
````
{
  "name": "Tugas_3",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT",
  "devDependencies": {
    "jest": "^25.1.0"
  },
     "scripts": {
        "build": "node app.js",
        "test": "standard"
  },
 "dependencies": {
    "async": "^0.2.10",
    "npm2es": "~0.4.2",
    "optimist": "~0.6.0",
    "request": "~2.30.0",
    "skateboard": "^1.5.1",
    "split": "^0.3.0",
    "weld": "^0.2.2"
  },
````

##### - Install Third Library
###### * _Untuk menginstall library dari luar bisa dengan menggunakan npm i packge_name. Instalasi library tersebut untuk lingkup production, untuk lingkup development npm i packge_name --save-dev dan untuk lingkup global atau device (PC / Komputer) bisa dengan menggunakan npm i packge_name -g_
````
const moment = require ('moment)
console.log (moment().toISOString())
````

##### - Remove Third Library
###### * _Untuk menghapus library pihak ketiga bisa dengan melakukan perintah npm unpackage_name atau npm un package_name -g untuk third library yang bersifat global._

##### - NPM Basic Command
###### * _Perintah Umum_
````
npm i package_name
npm i package_name1 package_name2
npm un package_name
npm un package_name1 package_name2
npm up
npm up package_name
npm up -g
npm list
npm help
````

### - NodeJS - CLI
#### * _CLI adalah tipe antarmuka dimana pengguna berinteraksi dengan sistem operasi melalui text-terminal. Pengguna menjalankan perintah dan program di sistem operasi tersebut dengan cara mengetikkan baris-baris tertentu. Meskipun konsepnya sama, tiap-tiap sistem operasi memiliki nama atau istilah yang berbeda untuk CLI-nya. UNIX memberi nama CLI-nya sebagai bash, ash, ksh, dan lain sebagainya._

##### Filosofi Unix
````
1. Kecil itu indah.
2. Setiap program mampu melakukan satu pekerjaan dengan baik.
3. Bangun prototip sesegera mungkin.
4. Portabilitas lebih utama dibandingkan efisiensi.
5. Simpan data dalam file teks murni.
6. Manfaatkan keunggulan perangkat lunak demi keuntunganmu.
7. Gunakan shell scripts untuk meningkatkan keunggulan dan portabilitas.
8. Hindari antarmuka pengguna yang menghambat kerja.
9. Jadikan setiap program sebuah filter (standard input to standard output)
````

##### - Build CLI App
###### * _Beberapa package yang membantu dalam pengembangan aplikasi command line pada Node JS, diantaranya: caporal, commander, yargs dsb._

##### - Carporal
````
$ npm install caporal
Atau
$ yarn add caporal

//Simple Program
const prog = require('caporal');
prog
  .version('1.0.0')
  .description('A simple program that says "biiiip"')
  .action(function(args, options, logger) {
    logger.info("biiiip")
  });
 
prog.parse(process.argv);
````
