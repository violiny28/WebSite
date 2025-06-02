<!DOCTYPE html>Add commentMore actions
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Manajemen Jaringan Komputer</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Fredoka:wght@400;600&display=swap');

    body {
      font-family: 'Fredoka', sans-serif;
      background: linear-gradient(to bottom, #d7ecf9, #f0f8ff);
      color: #2b3e50;
      text-align: center;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
      overflow-x: hidden;
    }

    h1 {
      font-size: 3em;
      color: #5b8fd1;
      margin-top: 60px;
      animation: popIn 1s ease-out;
    }

    .anggota-container {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
      margin-top: 30px;
    }

    .anggota {
      background: #e3f0fb;
      border: 3px dashed #7bb5e4;
      border-radius: 25px;
      width: 220px;
      padding: 20px;
      cursor: pointer;
      transition: transform 0.3s ease;
      box-shadow: 4px 4px 12px rgba(0, 0, 0, 0.08);
      animation: bounceIn 1.5s ease;
    }

    .anggota:hover {
      transform: rotate(-2deg) scale(1.05);
      background-color: #d1e8f9;
    }

    .anggota strong {
      color: #3d6fa3;
      font-size: 1.1em;
    }

    .nbi {
      display: none;
      margin-top: 10px;
      font-size: 0.9em;
      color: #444;
    }

    .footer {
      margin-top: 60px;
      padding: 40px 20px;
      font-size: 3em;
      font-weight: bold;
      background: linear-gradient(to right, #4a90e2, #8ab6f9);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: glowingText 3s ease-in-out infinite;
    }

    .clouds-svg {
      width: 100%;
      margin-top: 0;
    }

    .cat {
      position: absolute;
      bottom: 100px;
      left: 20px;
      width: 80px;
      animation: float 4s ease-in-out infinite;
    }

    /* Animations */
    @keyframes popIn {
      0% { opacity: 0; transform: scale(0.8); }
      100% { opacity: 1; transform: scale(1); }
    }

    @keyframes bounceIn {
      0% { transform: scale(0.5); opacity: 0; }
      60% { transform: scale(1.2); opacity: 1; }
      100% { transform: scale(1); }
    }

    @keyframes glowingText {
      0% { opacity: 0.8; transform: scale(1); }
      50% { opacity: 1; transform: scale(1.05); }
      100% { opacity: 0.8; transform: scale(1); }
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>

  <h1>Selamat Datang</h1>

  <div class="anggota-container">
    <div class="anggota" onclick="toggleNBI(this)">
      <strong>Anggota 1</strong>
      <div class="nbi">NBI: 1462300123</div>
    </div>
    <div class="anggota" onclick="toggleNBI(this)">
      <strong>Anggota 2</strong>
      <div class="nbi">NBI: 1462300134</div>
    </div>
    <div class="anggota" onclick="toggleNBI(this)">
      <strong>Neoriztinah Ratu Violiny</strong>
      <div class="nbi">NBI: 1462300142</div>
    </div>
  </div>

  <div class="footer">Manajemen Jaringan Komputer</div>

  <!-- Awan SVG -->
  <svg class="clouds-svg" viewBox="0 0 1440 320">
    <path fill="#dbefff" fill-opacity="1" d="M0,224L48,197.3C96,171,192,117,288,122.7C384,128,480,192,576,213.3C672,235,768,213,864,176C960,139,1056,85,1152,90.7C1248,96,1344,160,1392,192L1440,224L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path>
  </svg>

  <script>
    function toggleNBI(element) {
      const nbiDiv = element.querySelector('.nbi');
      nbiDiv.style.display = nbiDiv.style.display === 'block' ? 'none' : 'block';
    }
  </script>

</body>
</html>
