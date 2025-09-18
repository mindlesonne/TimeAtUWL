# TimeAtUWL
<!DOCTYPE html>
<html>
<head>
  <title>Time Since April 8, 2024</title>
</head>
<body>
  <h2>WRONG ONE:</h2>
  <p id="timer" style="font-size: 24px;"></p>

  <script>
    function updateTimer() {
      const startTime = new Date("2024-04-08T13:00:00Z"); // 8 AM CT = 13:00 UTC
      const now = new Date();
      let diff = Math.floor((now - startTime) / 1000);

      const years = Math.floor(diff / (365.25 * 24 * 3600));
      diff %= Math.floor(365.25 * 24 * 3600);
      const days = Math.floor(diff / (24 * 3600));
      diff %= 24 * 3600;
      const hours = Math.floor(diff / 3600);
      diff %= 3600;
      const minutes = Math.floor(diff / 60);
      const seconds = diff % 60;

      document.getElementById("timer").textContent =
        `${years} years, ${days} days, ${hours} hours, ${minutes} minutes, ${seconds} seconds`;
    }

    updateTimer();
    setInterval(updateTimer, 1000);
  </script>
</body>
</html>
