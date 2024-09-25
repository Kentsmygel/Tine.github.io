<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fun Architect Portfolio - Build and Destroy!</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: url('https://placekitten.com/1600/900') no-repeat center center fixed;
      background-size: cover;
      text-align: center;
      margin: 0;
      padding: 0;
    }

    h1 {
      font-size: 2.5rem;
      margin-top: 50px;
      color: #fff;
      text-shadow: 2px 2px 4px #000;
    }

    .fun-btn {
      margin: 20px;
      padding: 15px 30px;
      font-size: 1.2rem;
      color: white;
      background-color: #ff5733;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      z-index: 2;
      position: relative;
    }

    .fun-btn:hover {
      background-color: #c70039;
    }

    /* Skyscraper */
    #skyscraper-container {
      margin: 20px auto;
      width: 100px;
      display: flex;
      flex-direction: column-reverse; /* So blocks stack upward */
      align-items: center;
      transition: all 0.5s ease;
      z-index: 2;
      position: relative;
    }

    .skyscraper-block {
      width: 100px;
      height: 30px;
      background-color: #333;
      margin: 1px 0;
    }

    /* Wrecking Ball */
    #wrecking-ball {
      margin: 20px auto;
      width: 100px;
      height: 100px;
      background-color: #c70039;
      border-radius: 50%;
      display: none;
      position: relative;
      animation: swing 2s ease infinite;
      z-index: 2;
    }

    @keyframes swing {
      0% { transform: rotate(0); }
      50% { transform: rotate(20deg); }
      100% { transform: rotate(0); }
    }

    footer {
      margin-top: 100px;
      font-size: 0.8rem;
      color: #fff;
      text-shadow: 1px 1px 3px #000;
    }
  </style>
</head>
<body>

  <h1>Welcome to the Fun Architect Portfolio!</h1>

  <!-- Confetti Button -->
  <button class="fun-btn" id="confettiBtn">Click for Confetti Fun!</button>

  <!-- Build a Skyscraper Button -->
  <button class="fun-btn" id="buildBtn">Build a Skyscraper!</button>
  <div id="skyscraper-container"></div>

  <!-- Wrecking Ball Button -->
  <button class="fun-btn" id="wreckBtn">Bring the Wrecking Ball!</button>
  <div id="wrecking-ball"></div>

  <footer>
    <p>© 2024 Fun Architect. Now powered by kittens!</p>
  </footer>

  <!-- Confetti Script -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>

  <script>
    // Confetti Button
    const confettiBtn = document.getElementById('confettiBtn');
    confettiBtn.addEventListener('click', function() {
      confetti({
        particleCount: 100,
        spread: 70,
        origin: { y: 0.6 }
      });
    });

    // Build a Skyscraper
    const buildBtn = document.getElementById('buildBtn');
    const skyscraperContainer = document.getElementById('skyscraper-container');

    buildBtn.addEventListener('click', function() {
      // Create a new skyscraper block
      const newBlock = document.createElement('div');
      newBlock.classList.add('skyscraper-block');

      // Add the new block to the skyscraper container
      skyscraperContainer.appendChild(newBlock);
    });

    // Wrecking Ball Functionality
    const wreckBtn = document.getElementById('wreckBtn');
    const wreckingBall = document.getElementById('wrecking-ball');

    wreckBtn.addEventListener('click', function() {
      if (wreckingBall.style.display === "none") {
        wreckingBall.style.display = "block"; // Show the wrecking ball
        wreckSkyscraper();
      }
    });

    // Function to wreck the skyscraper
    function wreckSkyscraper() {
      // Remove all the blocks from the skyscraper
      skyscraperContainer.innerHTML = '';
      // Hide the wrecking ball after "wrecking" is done
      setTimeout(() => {
        wreckingBall.style.display = "none";
      }, 2000); // Hide the wrecking ball after 2 seconds
    }
  </script>

</body>
</html>
