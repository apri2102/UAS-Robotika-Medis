<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Smart Pressure Alert System</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(180deg, #6a6fd1, #7c7fd9);
      color: white;
    }
    header {
      text-align: center;
      padding: 80px 20px;
    }
    header h1 {
      font-size: 48px;
      margin-bottom: 10px;
    }
    header p {
      font-size: 20px;
      opacity: 0.9;
    }
    .tags {
      margin-top: 20px;
    }
    .tag {
      display: inline-block;
      background: rgba(255,255,255,0.2);
      padding: 8px 16px;
      border-radius: 20px;
      margin: 5px;
      font-size: 14px;
    }
    section {
      background: rgba(255,255,255,0.1);
      margin: 30px;
      padding: 30px;
      border-radius: 20px;
    }
    h2 {
      margin-top: 0;
    }
    ul {
      line-height: 1.8;
    }
  </style>
</head>

<body>

<header>
  <h1>SMART PRESSURE ALERT SYSTEM</h1>
  <p>Sistem Monitoring Tekanan Berbasis ROS2 Menggunakan Sensor FSR</p>
  <div class="tags">
    <span class="tag">ESP32</span>
    <span class="tag">ROS 2</span>
    <span class="tag">FSR Sensor</span>
    <span class="tag">Buzzer</span>
    <span class="tag">Robotika Medis</span>
  </div>
</header>

<section>
  <h2>Profil Anggota Kelompok</h2>
  <p>
    Nama: Apri Ayu Lia<br>
    Program Studi: Teknik Biomedis<br>
    Institusi: Institut Teknologi Sumatera (ITERA)<br>
    Mata Kuliah: Robotika Medis
  </p>
</section>

<section>
  <h2>Pendahuluan</h2>
  <p>
    Smart Pressure Alert System merupakan sistem monitoring tekanan yang
    menggunakan sensor Force Sensitive Resistor (FSR), ESP32, dan middleware
    Robot Operating System 2 (ROS2). Sistem ini dirancang untuk mendeteksi
    tekanan dan memberikan peringatan berupa bunyi buzzer ketika tekanan
    melebihi ambang batas tertentu.
  </p>
</section>

<section>
  <h2>Alat dan Bahan</h2>
  <h3>Perangkat Keras</h3>
  <ul>
    <li>Force Sensitive Resistor (FSR)</li>
    <li>ESP32</li>
    <li>Buzzer</li>
    <li>Resistor pendukung</li>
    <li>Breadboard</li>
    <li>Kabel jumper</li>
    <li>Kabel USB</li>
  </ul>

  <h3>Perangkat Lunak</h3>
  <ul>
    <li>Ubuntu (WSL)</li>
    <li>ROS 2</li>
    <li>Arduino IDE</li>
    <li>Python</li>
    <li>GitHub Pages</li>
  </ul>
</section>

<section>
  <h2>Tahap I – Environment Setup</h2>
  <p>
    Tahap ini bertujuan untuk menyiapkan lingkungan kerja perangkat lunak
    agar sistem dapat dikembangkan, dijalankan, dan diintegrasikan dengan
    ROS 2 secara optimal.
  </p>

  <h3>1. Menyiapkan Sistem Operasi Utama (Windows 11)</h3>
  <p>
    Windows 11 digunakan sebagai host system (sistem utama) untuk menjalankan
    seluruh proses pengembangan.
  </p>
    Fungsi Utama:
  <ul>
  <p> 
    <li>Menjalankan Arduino IDE</li>
    <li>Menjalankan Docker Desktop</li>
    <li>Menjalankan WSL 2 sebagai jembatan ke Linux</li>
  </ul>
  <p>
    <b>Catatan:</b> Pastikan Windows sudah ter-update, virtualisasi aktif di BIOS,
    dan RAM minimal 8 GB.
  </p>

  <h3>2. Mengaktifkan WSL 2 (Windows Subsystem for Linux)</h3>
  <p>
    WSL 2 memungkinkan menjalankan sistem operasi Linux langsung di dalam
    Windows tanpa dual boot.
  </p>
  Langkah-langkah:
  <ul>
  <p>
    <li>Buka PowerShell sebagai Administrator</li>
    <li>Jalankan perintah aktivasi WSL</li>
    <img src="images/gambar1.png">
    <li>Lakukan restart sistem komputer</li>
    <li>Pastikan WSL menggunakan versi 2</li>
    <img src="images/Gambar2.png">  
  </ul>

  <h3>3. Instalasi Ubuntu 24.04 LTS</h3>
  <p>
    Ubuntu digunakan sebagai sistem operasi Linux utama untuk menjalankan ROS 2.
  </p>
    Langkah-langkah:
  <ul>
  <p>
    <li>Unduh Ubuntu 24.04 LTS melalui Microsoft Store</li>
    <li>Lakukan Instal dan jalankan</li>
    <li>Buat username dan password pada Linux</li>
  </ul>

  <h3>4. Update Sistem Ubuntu</h3>
  <p>
    Update sistem dilakukan untuk memastikan seluruh package berada pada versi
    terbaru sebelum instalasi ROS 2.
  </p>
    Kode:
  <ul>
  <p><i>
  <img src="images/Gambar3.png">
   </ul>

  <h3>5. Instalasi ROS 2 Jazzy Jalisco</h3>
  <p>
    ROS 2 digunakan sebagai middleware komunikasi antara node publisher dan
    subscriber.
  </p>
  Langkah-langkah:
  <ul>
  <p>
    <li>Menambahkan locale sistem</li>
    <img src="images/Gambar4.png">
    <li>Menambahkan repository resmi ROS 2</li>
    <img src="images/gambar5.png">
    <li>Menginstal ROS 2 Jazzy Jalisco</li>
    <img src="images/gambar6.png">
    <li>Melakukan setup environment</li>
    <img src="images/gambar7.png">
  </ul>

  <h3>6. Instalasi Docker Desktop</h3>
  <p>
    Docker digunakan untuk menjalankan micro-ROS agent secara terisolasi.
  </p>
  Langkah-langkah:
  <ul>
  <p>
    <li>Unduh Docker Desktop for Windows</li>
    <li>Lakukan instalasi dan restart jika diperlukan</li>
  </ul>
  <img src="images/gambar8.png">
  </ul>

  <h3>7. Menjalankan micro-ROS Agent</h3>
  <p>
    Micro-ROS Agent berfungsi sebagai penghubung antara mikrokontroler ESP32
    dan ROS 2.
  </p>
  Jalankan container:
  <ul>
  <p>
  <img src="images/gambar9.png">
  </ul>

  <h3>8. Instalasi Arduino IDE</h3>
  <p>
    Arduino IDE digunakan untuk pemrograman ESP32 dan pembacaan sensor FSR.
  </p>
   Langkah-langkah:
  <ul>
  <p>
    <li>Instalasi Arduino IDE</li>
    <li>Penambahan board ESP32</li>
    <li>Instalasi library pendukung sensor FSR</li>
  </ul>

  <h3>9. Instalasi Python</h3>
  <p>
    Python digunakan untuk pengembangan node ROS 2 dan monitoring data sensor.
  </p>
  Pastikan Pyhton terinstal:
  <ul>
  <p>
  <img src="images/gambar10.png"> 
  </p>
  Jika belum, lakukan:
  <ul>
  <p>
   <img src="images/gambar11.png">   
</section>

<section>
  <h2>Langkah Pembuatan Sistem</h2>
  <p><b>Hardware:</b></p>
  <ul>
    <li>Menghubungkan sensor FSR ke ESP32 melalui pin analog</li>
    <li>Menghubungkan buzzer sebagai output peringatan</li>
    <li>Melakukan pengujian rangkaian</li>
  </ul>

  <p><b>Software:</b></p>
  <ul>
    <li>Menginstal Ubuntu dan ROS2</li>
    <li>Membuat node publisher untuk data FSR</li>
    <li>Membuat node subscriber untuk kontrol buzzer</li>
    <li>Melakukan pengujian komunikasi ROS2</li>
  </ul>
</section>

<section>
  <h2>Kendala dan Solusi</h2>
  <ul>
    <li>
      <b>Kendala:</b> Integrasi ESP32 dengan ROS2<br>
      <b>Solusi:</b> Melakukan simulasi data sensor sebelum integrasi penuh
    </li>
    <li>
      <b>Kendala:</b> Penentuan ambang batas tekanan<br>
      <b>Solusi:</b> Pengujian sensor secara bertahap
    </li>
  </ul>
</section>

</body>
</html>
