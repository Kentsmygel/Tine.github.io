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

    /* Make the button clearly visible */
    .confetti-btn:focus {
      outline: none;
      border: 2px solid #ffc300;
    }

    footer {
      margin-top: 100px;
      font-size: 0.8rem;
      color: #666;
    }

    /* Confetti "Placeholder" */
    #confetti-container {
      margin-top: 40px;
      height: 300px;
      background: #fff3cd;
      border: 2px dashed #ff5733;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    #confetti-message {
      font-size: 1.5rem;
      color: #c70039;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <h1>Welcome to the Confetti Architect Extravaganza!</h1>

  <!-- Confetti Button -->
  <button class="confetti-btn" id="confettiBtn">Click for Confetti Fun!</button>

  <!-- Placeholder for confetti or message -->
  <div id="confetti-container">
    <p id="confetti-message">Confetti Goes Here! 🎉 (When magic happens)</p>
  </div>

  <footer>
    <p>© 2024 Confetti Architect. No actual buildings were harmed in the making of this confetti.</p>
  </footer>

  <!-- You would typically use JavaScript here for the confetti effect -->
  <!-- <script src="confetti.js"></script> -->

</body>
</html>
