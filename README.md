<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ramalan Aura Sigma</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 700px;
      margin: 40px auto;
      padding: 20px;
    }
    input, button {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      box-sizing: border-box;
    }
    .hasil {
      margin-top: 20px;
      padding: 12px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <h2>Ramalan Aura Sigma Skibidi Tuff Triple T Sahur</h2>

  <input id="nama" placeholder="Masukkan nama" />
  <input id="umur" type="number" placeholder="Masukkan umur" />
  <input id="brainrot" placeholder="Brainrot favorit" />
  <input id="phonk" placeholder="Lagu phonk favorit" />

  <button onclick="hitungAura()">Hitung Sekarang</button>

  <div class="hasil">
    <p><strong>Skor:</strong> <span id="skor">-</span></p>
    <p><strong>Level:</strong> <span id="level">-</span></p>
  </div>

  <script>
    function hitungAura() {
      const nama = document.getElementById('nama').value;
      const umur = parseInt(document.getElementById('umur').value || 0);
      const brainrot = document.getElementById('brainrot').value;
      const phonk = document.getElementById('phonk').value;

      let skor = 0;
      skor += nama.length * 17;
      skor += umur * 3;
      skor += brainrot.length * 11;
      skor += phonk.length * 9;
      skor = Math.max(-1000, Math.min(1000, skor - 300));

      let level = '';
      if (skor <= -750) level = 'Skibidi Chopped Aura';
      else if (skor <= -500) level = 'Skibidi Bad Aura';
      else if (skor <= -250) level = 'Chopped Aura';
      else if (skor <= 0) level = 'Negative Aura';
      else if (skor <= 250) level = 'Tuff Aura';
      else if (skor <= 500) level = 'Triple T Aura';
      else if (skor <= 750) level = 'Super Tuff Aura';
      else level = 'Super Triple T Aura';

      document.getElementById('skor').textContent = skor;
      document.getElementById('level').textContent = level;
    }
  </script>
</body>
</html>
