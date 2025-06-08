<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Andri & Yessha - Undangan Pernikahan</title>
  <style>
    body {
      background: black;
      color: gold;
      font-family: serif;
      text-align: center;
      padding: 2rem;
    }
    h1 {
      font-size: 3em;
      margin-bottom: 0;
    }
    .countdown {
      font-size: 2em;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <h1>Andri & Yessha</h1>
  <p>Undangan Pernikahan - 9 Oktober, Sukadana</p>

  <div class="countdown" id="countdown"></div>

  <script>
    // Hitung mundur ke 9 Oktober
    const countDownDate = new Date("October 9, 2025 08:00:00").getTime();

    const countdownEl = document.getElementById("countdown");
    const x = setInterval(function() {
      const now = new Date().getTime();
      const distance = countDownDate - now;

      if (distance < 0) {
        clearInterval(x);
        countdownEl.innerHTML = "Hari Bahagia Telah Tiba!";
      } else {
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);
        countdownEl.innerHTML = `${days} Hari ${hours} Jam ${minutes} Menit ${seconds} Detik`;
      }
    }, 1000);
  </script>
</body>
</html>
