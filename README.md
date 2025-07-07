# Xanonprofile
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Kenzo - Ethical Hacker</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    * {
      margin: 0; padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d0d0d;
      color: #f0f0f0;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px;
    }

    h1, h2 {
      color: #0ff;
      margin-bottom: 20px;
    }

    form, .profile {
      background: #1a1a1a;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 10px #00ffff20;
      width: 90%;
      max-width: 400px;
      text-align: center;
    }

    input {
      width: 100%;
      margin-bottom: 15px;
      padding: 12px;
      border: none;
      border-radius: 8px;
      background: #333;
      color: #fff;
    }

    button {
      background: #0ff;
      border: none;
      padding: 12px 25px;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background: #00cccc;
    }

    .skill-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 15px;
      margin-top: 25px;
    }

    .skill {
      background: #262626;
      padding: 15px;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
      text-align: center;
    }

    .skill:hover {
      background: #333;
      transform: scale(1.05);
    }

    .desc {
      margin-top: 10px;
      font-size: 14px;
      color: #ccc;
    }

    .hidden {
      display: none;
    }

    .footer {
      margin-top: 40px;
      color: #777;
      font-size: 13px;
    }
  </style>
</head>
<body>

  <form id="formIdentitas">
    <h2>Isi Identitas Anda</h2>
    <input type="text" id="nama" placeholder="Nama Anda" required>
    <input type="email" id="email" placeholder="Email Aktif" required>
    <input type="number" id="umur" placeholder="Umur" required>
    <button type="submit">Lihat Profil Kenzo</button>
  </form>

  <div class="profile hidden" id="profile">
    <h1>Kenzo - Ethical Hacker</h1>
    <p>Asal: Pekanbaru, Riau</p>
    <p>Email: pykcyber@gmail.com | Kontak: 083143490913</p>
    <h2>💻 Skill Hacking</h2>
    <div class="skill-list">
      <div class="skill" onclick="toggleDesc(0)">
        <i class="fas fa-user-secret"></i><br>Social Engineering
        <div class="desc hidden">Teknik memanipulasi target untuk mengungkap data rahasia.</div>
      </div>
      <div class="skill" onclick="toggleDesc(1)">
        <i class="fas fa-search"></i><br>OSINT
        <div class="desc hidden">Mengumpulkan informasi publik untuk keperluan analisis.</div>
      </div>
      <div class="skill" onclick="toggleDesc(2)">
        <i class="fas fa-fish"></i><br>Phishing
        <div class="desc hidden">Teknik jebakan untuk mencuri data melalui link palsu.</div>
      </div>
      <div class="skill" onclick="toggleDesc(3)">
        <i class="fas fa-globe"></i><br>Website Pentest
        <div class="desc hidden">Menguji keamanan sebuah website dari celah seperti SQLi, XSS.</div>
      </div>
      <div class="skill" onclick="toggleDesc(4)">
        <i class="fas fa-wifi"></i><br>WiFi Hacking
        <div class="desc hidden">Mengakses dan menganalisis jaringan nirkabel (edukasi).</div>
      </div>
      <div class="skill" onclick="toggleDesc(5)">
        <i class="fas fa-key"></i><br>Bypass Login
        <div class="desc hidden">Masuk ke akun atau sistem tanpa kredensial sah.</div>
      </div>
      <div class="skill" onclick="toggleDesc(6)">
        <i class="fas fa-terminal"></i><br>Tools Developer
        <div class="desc hidden">Membuat tools berbasis bash/python untuk keamanan digital.</div>
      </div>
    </div>
  </div>

  <div class="footer">
    &copy; 2025 Kenzo - All Rights Reserved
  </div>

  <script>
    const form = document.getElementById('formIdentitas');
    const profile = document.getElementById('profile');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      form.classList.add('hidden');
      profile.classList.remove('hidden');
    });

    function toggleDesc(index) {
      const allDesc = document.querySelectorAll('.desc');
      allDesc.forEach((desc, i) => {
        if (i === index) {
          desc.classList.toggle('hidden');
        } else {
          desc.classList.add('hidden');
        }
      });
    }
  </script>

</body>
</html>
