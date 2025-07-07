# Xanonprofile
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Kenzo | Cyber Intelligence</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0; padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Orbitron', sans-serif;
      color: #fff;
      background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364, #1b1b1b);
      background-size: 400% 400%;
      animation: gradient 15s ease infinite;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 40px 20px;
      min-height: 100vh;
    }

    @keyframes gradient {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    h1 {
      color: #00ffe1;
      font-size: 28px;
      margin-bottom: 10px;
      text-shadow: 0 0 5px #00ffe1;
    }

    form, .profile {
      background: rgba(0,0,0,0.4);
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 10px #00ffe130;
      width: 90%;
      max-width: 450px;
      text-align: center;
      margin-top: 20px;
    }

    input {
      width: 100%;
      margin-bottom: 15px;
      padding: 12px;
      border: none;
      border-radius: 8px;
      background: #1b1b1b;
      color: #fff;
    }

    button {
      background: #00ffe1;
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

    .profile-info {
      text-align: left;
      margin: 20px 0;
    }

    .profile-info p {
      margin: 10px 0;
    }

    .profile-info i {
      margin-right: 8px;
      color: #0ff;
    }

    .skill-list {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 15px;
      margin-top: 25px;
    }

    .skill {
      background: #111;
      padding: 15px;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
      text-align: center;
      border: 1px solid #0ff2;
    }

    .skill:hover {
      background: #222;
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
      color: #888;
      font-size: 13px;
    }
  </style>
</head>
<body>

  <form id="formIdentitas">
    <h1>Selamat Datang</h1>
    <p>Silakan isi identitas untuk melanjutkan</p>
    <input type="text" id="nama" placeholder="Nama Lengkap" required>
    <input type="email" id="email" placeholder="Email Aktif" required>
    <input type="number" id="umur" placeholder="Umur" required>
    <button type="submit">Lanjutkan</button>
  </form>

  <div class="profile hidden" id="profile">
    <h1>Kenzo | Cyber Intelligence</h1>
    <div class="profile-info">
      <p><i class="fas fa-map-marker-alt"></i> Pekanbaru, Riau</p>
      <p><i class="fas fa-envelope"></i> pykcyber@gmail.com</p>
      <p><i class="fas fa-phone"></i> 083143490913</p>
    </div>

    <h2>Skill Hacking</h2>
    <div class="skill-list">
      <div class="skill" onclick="toggleDesc(0)">
        <i class="fas fa-user-secret"></i><br>Social Engineering
        <div class="desc hidden">Manipulasi psikologis untuk akses data sensitif.</div>
      </div>
      <div class="skill" onclick="toggleDesc(1)">
        <i class="fas fa-search"></i><br>OSINT
        <div class="desc hidden">Penggalian info terbuka dari internet.</div>
      </div>
      <div class="skill" onclick="toggleDesc(2)">
        <i class="fas fa-fish"></i><br>Phishing
        <div class="desc hidden">Link palsu untuk jebak pengguna awam.</div>
      </div>
      <div class="skill" onclick="toggleDesc(3)">
        <i class="fas fa-globe"></i><br>Web Pentest
        <div class="desc hidden">Uji keamanan web (SQLi, XSS, dll).</div>
      </div>
      <div class="skill" onclick="toggleDesc(4)">
        <i class="fas fa-wifi"></i><br>WiFi Exploit
        <div class="desc hidden">Analisa & akses jaringan wireless secara etis.</div>
      </div>
      <div class="skill" onclick="toggleDesc(5)">
        <i class="fas fa-terminal"></i><br>Tools Dev
        <div class="desc hidden">Membuat tools bash/python untuk audit keamanan.</div>
      </div>
    </div>
  </div>

  <div class="footer">
    &copy; 2025 Kenzo | pykcyber
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
