<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Confetti Architect Extravaganza</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      text-align: center;
      margin: 0;
      padding: 0;
    }

    h1 {
      font-size: 2.5rem;
      margin-top: 50px;
      color: #333;
    }

    .confetti-btn {
      margin-top: 20px;
      padding: 15px 30px;
      font-size: 1.2rem;
      color: white;
      background-color: #ff5733;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .confetti-btn:hover {
      background-color: #c70039;
    }

    footer {
      margin-top: 100px;
      font-size: 0.8rem;
      color: #666;
    }
  </style>
</head>
<body>

  <h1>Welcome to the Confetti Architect Extravaganza!</h1>

  <!-- Confetti Button -->
  <button class="confetti-btn" id="confettiBtn">Click for Confetti Fun!</button>

  <footer>
    <p>© 2024 Confetti Architect. No actual buildings were harmed in the making of this confetti.</p>
  </footer>

  <!-- Confetti Script -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>

  <script>
    // Get the button
    const confettiBtn = document.getElementById('confettiBtn');

    // Add a click event listener to the button
    confettiBtn.addEventListener('click', function() {
      // Trigger the confetti when the button is clicked
      confetti({
        particleCount: 100,
        spread: 70,
        origin: { y: 0.6 }
      });
    });
  </script>

</body>
</html>
