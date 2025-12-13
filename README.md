<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wedalestari Dashboard</title>

  <!-- Chart.js -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

  <!-- Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(180deg, #E8F4FF, #F7FFF9);
      color: #123;
    }

    header {
      padding: 24px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .brand {
      font-size: 22px;
      font-weight: 600;
      color: #1A73E8;
    }

    .tagline {
      font-size: 14px;
      color: #2E7D32;
    }

    .container {
      padding: 20px 40px;
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 24px;
    }

    .card {
      background: #ffffffcc;
      backdrop-filter: blur(8px);
      border-radius: 20px;
      padding: 24px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.05);
    }

    .card h2 {
      margin-top: 0;
      font-size: 18px;
      color: #1A73E8;
    }

    .lestari-box {
      display: flex;
      gap: 16px;
      align-items: center;
    }

    .lestari-box img {
      width: 90px;
    }

    .speech {
      background: #E3F2FD;
      border-radius: 16px;
      padding: 14px 18px;
      font-size: 14px;
    }

    footer {
      text-align: center;
      padding: 16px;
      font-size: 12px;
      color: #789;
    }
  </style>
</head>
<body>

  <header>
    <div>
      <div class="brand">WEDALESTARI</div>
      <div class="tagline">Dibalas: <strong>HIJAU</strong></div>
    </div>
  </header>

  <section class="container">

    <!-- Charts -->
    <div class="card">
      <h2>Kualitas Air</h2>
      <canvas id="waterChart"></canvas>
    </div>

    <!-- Lestari AI Guide -->
    <div class="card">
      <h2>Lestari</h2>
      <div class="lestari-box">
        <img src="assets/lestari.png" alt="Lestari Mascot" />
        <div class="speech">
          Halo! Aku Lestari 🌿<br/>
          Kondisi kualitas air hari ini berada dalam status <strong>Hijau</strong>.
        </div>
      </div>
    </div>

    <div class="card">
      <h2>Curah Hujan</h2>
      <canvas id="rainChart"></canvas>
    </div>

  </section>

  <footer>
    © 2026 Wedalestari Enviro · Guardian of Water
  </footer>

<script>
  const waterCtx = document.getElementById('waterChart');
  new Chart(waterCtx, {
    type: 'line',
    data: {
      labels: ['Jan','Feb','Mar','Apr','Mei'],
      datasets: [
        {
          label: 'pH',
          data: [7.1, 7.0, 6.9, 7.2, 7.1],
          borderWidth: 2,
          tension: 0.4
        },
        {
          label: 'TSS',
          data: [30, 40, 45, 38, 32],
          borderWidth: 2,
          tension: 0.4
        }
      ]
    }
  });

  const rainCtx = document.getElementById('rainChart');
  new Chart(rainCtx, {
    type: 'bar',
    data: {
      labels: ['Jan','Feb','Mar','Apr','Mei'],
      datasets: [{
        label: 'Curah Hujan (mm)',
        data: [120, 180, 220, 160, 140]
      }]
    }
  });
</script>

</body>
</html># WEDALESTARI
