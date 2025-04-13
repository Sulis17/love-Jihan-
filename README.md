# Folder Pertama
<!DOCTYPE html><html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Untuk Kak Jihan</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom right, #ffd6e8, #ffe6f0);
      font-family: 'Courier New', monospace;
      color: #8b005d;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    #puisi-container {
      max-width: 600px;
      padding: 30px;
      background: rgba(255, 255, 255, 0.85);
      border-radius: 20px;
      box-shadow: 0 0 30px rgba(0,0,0,0.2);
      font-size: 18px;
      line-height: 1.8;
      white-space: pre-line;
    }
    .penutup {
      margin-top: 30px;
      font-style: italic;
      text-align: center;
      color: #b30059;
    }
  </style>
</head>
<body>
  <div id="puisi-container"></div>  <script>
    const teks = `Untuk Kak Jihan

Ada nama yang tak pernah kusangka,
Namun hadirnya selalu membawa rasa.
Kak Jihan, kau seperti paragraf pertama dalam buku favoritku —
Belum terlalu kukenal, tapi sudah bikin penasaran terus-menerus.

Setiap senyummu seolah punya frekuensi sendiri,
Yang bisa menenangkan bahkan di hari paling sepi.
Aku tak tahu banyak tentangmu, dan mungkin kau pun tak kenal aku...
Tapi entah kenapa, aku suka caramu hadir, walau dari jauh.

Kalau nanti semesta beri kesempatan,
Aku cuma ingin bilang: kamu inspirasi dari bait yang diam-diam kutulis malam ini.

-- Dari seseorang yang sedang belajar mengenalmu perlahan.`;

    const container = document.getElementById("puisi-container");
    let i = 0;

    function ketik() {
      if (i < teks.length) {
        container.innerHTML += teks.charAt(i);
        i++;
        setTimeout(ketik, 40);
      } else {
        const penutup = document.createElement("div");
        penutup.className = "penutup";
        penutup.textContent = "Senyum, ya. Ini cuma dari seseorang yang mengagumimu diam-diam.";
        container.appendChild(penutup);
      }
    }

    ketik();
  </script></body>
</html>
