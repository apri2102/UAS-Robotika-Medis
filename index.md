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
