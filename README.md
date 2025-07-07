# Xanonprofile
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Kenzo | Cyber Intelligence</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box;}
    body {
      font-family: 'Orbitron', sans-serif;
      background: #000;
      color: #fff;
      overflow-x: hidden;
    }

    /* Background cyber animation */
    body::before {
      content: '';
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: repeating-linear-gradient(
        to bottom,
        rgba(0, 255, 150, 0.05),
        rgba(0, 255, 150, 0.05) 1px,
        transparent 2px,
        transparent 4px
      );
      animation: matrix 5s linear infinite;
      z-index: -1;
    }

    @keyframes matrix {
      from { background-position-y: 0; }
      to { background-position-y: 100%; }
    }

    .container {
      max-width: 600px;
      margin: auto;
      padding: 40px 20px;
      text-align: center;
    }

    h1 {
      color: #00fff7;
      font-size: 28px;
      text-shadow: 0 0 5px #00fff7;
      margin-bottom: 10px;
    }

    p {
      color: #ccc;
      font-size: 14px;
    }

    form, .content {
      background: rgba(0, 0, 0, 0.6);
      padding: 25px;
      border-radius: 12px;
      margin-top: 20px;
      box-shadow: 0 0 15px #00fff720;
    }

    input {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 8px;
      border: none;
      background: #111;
      color: #fff;
    }

    button {
      padding: 12px 25px;
      background: #00fff7;
      border: none;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;
    }

    .profile-pic {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid #00fff7;
      margin-bottom: 15px;
    }

    .info p {
      margin: 8px 0;
    }

    .info i {
      margin-right: 8px;
      color: #00fff7;
    }

    .skills {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 15px;
      margin-top: 25px;
    }

    .skill {
      background: #111;
      padding: 15px;
      border-radius: 10px;
      cursor: pointer;
      border: 1px solid #00fff7;
      transition: 0.3s;
    }

    .skill:hover {
      background: #1b1b1b;
      transform: scale(1.03);
    }

    .desc {
      font-size: 13px;
      margin-top: 8px;
      color: #aaa;
      display: none;
    }

    .footer {
      text-align: center;
      color: #777;
      margin-top: 40px;
      font-size: 12px;
    }

    .hidden {
      display: none;
    }

    a {
      color: #00fff7;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>Kenzo | Cyber Intelligence</h1>

    <form id="formIdentitas">
      <p>Silakan isi identitas Anda terlebih dahulu</p>
      <input type="text" id="nama" placeholder="Nama Lengkap" required>
      <input type="email" id="email" placeholder="Email Aktif" required>
      <input type="number" id="umur" placeholder="Umur" required>
      <button type="submit">Lanjutkan</button>
    </form>

    <div class="content hidden" id="kontenWeb">
      <img src="https://raw.githubusercontent.com/enzcyber/anonprofile/main/foto.jpg" alt="Foto Kenzo" class="profile-pic">
      
      <h2>KENZO</h2>
      <p>18 y/o Cybersecurity Enthusiast from Pekanbaru, Riau.<br>
      Focused on ethical hacking, OSINT, and digital security awareness.<br>
      Passionate about learning, building, and protecting the digital world.</p>
      <em>“Knowledge is my weapon. Ethics is my shield.”</em>

      <div class="info">
        <p><i class="fas fa-map-marker-alt"></i> Pekanbaru, Riau</p>
        <p><i class="fas fa-envelope"></i> 
          <a href="mailto:pykcyber@gmail.com?subject=Permintaan Bantuan&body=Saya butuh bantuan anda BLACK HAT CYBER">
            pykcyber@gmail.com
          </a>
        </p>
        <p><i class="fas fa-phone"></i> 
          <a href="https://wa.me/6283143490913?text=Saya%20butuh%20bantuan%20anda%20BLACK%20HAT%20CYBER">
            083143490913
          </a>
        </p>
        <p><i class="fab fa-tiktok"></i> 
          <a href="https://tiktok.com/@anonprofile_" target="_blank">@anonprofile_</a>
        </p>
      </div>

      <h3 style="margin-top: 30px; color:#0ff;">Skill Hacking</h3>
      <div class="skills">
        <div class="skill" onclick="toggleDesc(0)">OSINT<div class="desc">Open-source intelligence: mengumpulkan info dari data publik.</div></div>
        <div class="skill" onclick="toggleDesc(1)">Phishing<div class="desc">Membuat halaman tiruan untuk edukasi keamanan.</div></div>
        <div class="skill" onclick="toggleDesc(2)">Social Engineering<div class="desc">Manipulasi psikologis untuk akses sistem/akun.</div></div>
        <div class="skill" onclick="toggleDesc(3)">Website Pentest<div class="desc">SQL Injection, XSS, Path Traversal, dan uji keamanan web.</div></div>
        <div class="skill" onclick="toggleDesc(4)">WiFi Exploit<div class="desc">Pemantauan & analisa keamanan jaringan wireless.</div></div>
        <div class="skill" onclick="toggleDesc(5)">Bypass Login<div class="desc">Teknik masuk ke sistem tanpa login sah (for testing).</div></div>
        <div class="skill" onclick="toggleDesc(6)">Tools Developer<div class="desc">Membuat tools OSINT/bash/python untuk analisa digital.</div></div>
        <div class="skill" onclick="toggleDesc(7)">Malware Analysis<div class="desc">Analisa perilaku dan fungsi file berbahaya.</div></div>
        <div class="skill" onclick="toggleDesc(8)">Linux Exploit<div class="desc">Menggunakan command-line dan exploit di sistem Unix.</div></div>
      </div>
    </div>

    <div class="footer">
      &copy; 2025 Kenzo | Cyber Intelligence
    </div>
  </div>

  <script>
    const form = document.getElementById('formIdentitas');
    const konten = document.getElementById('kontenWeb');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      form.classList.add('hidden');
      konten.classList.remove('hidden');
    });

    function toggleDesc(index) {
      const allDesc = document.querySelectorAll('.desc');
      allDesc.forEach((desc, i) => {
        if (i === index) {
          desc.style.display = (desc.style.display === 'block') ? 'none' : 'block';
        } else {
          desc.style.display = 'none';
        }
      });
    }
  </script>

</body>
</html>
