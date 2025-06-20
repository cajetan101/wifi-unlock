# wifi-unlock
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>WiFi Unlock | Cajeria Ventures</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Orbitron', sans-serif;
      background-color: #d4a14e;
      color: #000;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      text-align: center;
    }

    img.logo {
      width: 120px;
      height: auto;
      margin-bottom: 1.5rem;
    }

    h1 {
      font-size: 2.2rem;
      margin-bottom: 1rem;
      letter-spacing: 1px;
    }

    p {
      font-size: 1.1rem;
      margin-bottom: 1rem;
    }

    .follow-btn, .verify-btn {
      background-color: #000;
      color: #d4a14e;
      border: none;
      padding: 1rem 2rem;
      font-size: 1rem;
      font-weight: bold;
      border-radius: 10px;
      margin: 0.5rem;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .follow-btn:hover, .verify-btn:hover {
      background-color: #222;
    }

    input {
      padding: 0.8rem;
      border-radius: 8px;
      border: 1px solid #000;
      margin-top: 1rem;
      width: 250px;
      font-size: 1rem;
    }

    #wifi-info, #verifying {
      display: none;
      margin-top: 2rem;
      padding: 1rem;
      background: #000;
      color: #ffd700;
      border-radius: 10px;
      font-size: 1.1rem;
    }

    #verifying {
      color: #000;
      background: #ffd700;
    }
  </style>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
</head>
<body>
  <img src="https://cajetan101.github.io/wifi-unlock/logo.jpg" alt="Cajeria Ventures Logo" class="logo">
  <h1>🚀 Unlock Free WiFi</h1>
  <p>Follow us on Instagram to reveal WiFi access details</p>

  <a href="https://instagram.com/cajeriaventures" target="_blank">
    <button class="follow-btn">Follow @cajeriaventures</button>
  </a>

  <input type="text" id="username" placeholder="Enter your Instagram username" />

  <button class="verify-btn" onclick="verifyFollow()">Verify & Show WiFi Info</button>

  <div id="verifying">Verifying your follow... please wait ⏳</div>

  <div id="wifi-info">
    <p><strong>WiFi Name:</strong> cajetan</p>
    <p><strong>Password:</strong> Uaremine</p>
  </div>

  <script>
    function verifyFollow() {
      const username = document.getElementById('username').value.trim();
      if (username === '') {
        alert('Please enter your Instagram username.');
        return;
      }

      document.getElementById('verifying').style.display = 'block';

      setTimeout(() => {
        document.getElementById('verifying').style.display = 'none';
        document.getElementById('wifi-info').style.display = 'block';
      }, 4000); // Simulate 4-second verification delay
    }
  </script>
</body>
</html>
