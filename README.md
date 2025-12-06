# M
<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Bizim Zamanımız</title>
<style>
  body {
    margin: 0;
    background: #1a001f;
    color: white;
    font-family: "Montserrat", sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    text-align: center;
  }
  .timeBox {
    font-size: 2.2rem;
    font-weight: 700;
    line-height: 1.6;
    background: rgba(255, 255, 255, 0.1);
    padding: 25px 40px;
    border-radius: 20px;
    box-shadow: 0 0 25px rgba(170, 0, 255, 0.4);
    border: 2px solid rgba(255, 255, 255, 0.2);
  }
</style>
</head>
<body>
  <div class="timeBox" id="timeBox"></div>
<script>
  const startDate = new Date("2025-11-03T04:19:00");
  function updateTime() {
    const now = new Date();
    let diff = now - startDate;
    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    diff -= days * 1000 * 60 * 60 * 24;
    const hours = Math.floor(diff / (1000 * 60 * 60));
    diff -= hours * 1000 * 60 * 60;
    const minutes = Math.floor(diff / (1000 * 60));
    diff -= minutes * 1000 * 60;
    const seconds = Math.floor(diff / 1000);
    document.getElementById("timeBox").innerHTML =
      `💜 Biz <br><br>${days} gün ${hours} saat<br>${minutes} dakika ${seconds} saniyedir birlikteyiz 💜`;
  }
  setInterval(updateTime, 1000);
  updateTime();
</script>

