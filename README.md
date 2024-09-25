<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fun Architect Portfolio</title>
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

    .fun-btn {
      margin: 20px;
      padding: 15px 30px;
      font-size: 1.2rem;
      color: white;
      background-color: #ff5733;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }

    .fun-btn:hover {
      background-color: #c70039;
    }

    /* Skyscraper */
    #skyscraper {
      margin: 20px auto;
      width: 100px;
      height: 0;
      background-color: #333;
      transition: height 1s ease;
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
    }

    @keyframes swing {
      0% { transform: rotate(0); }
      50% { transform: rotate(20deg); }
      100% { transform: rotate(0); }
    }

    #quote-box {
      margin-top: 20px;
      padding: 20px;
      background-color: #fff3cd;
      border: 2px dashed #ff5733;
      font-size: 1.2rem;
      font-style: italic;
      display: none;
    }

    footer {
      margin-top: 100px;
      font-size: 0.8rem;
      color: #666;
    }
  </style>
</head>
<body>

  <h1>Welcome to the Fun Architect Portfolio!</h1>

  <!-- Confetti Button -->
  <button class="fun-btn" id="confettiBtn">Click for Confetti Fun!</button>

  <!-- Build a Skyscraper Button -->
  <button class="fun-btn" id="buildBtn">Build a Skyscraper!</button>
  <div id="skyscraper"></div>

  <!-- Wrecking Ball Button -->
  <button class="fun-btn" id="wreckBtn">Bring the Wrecking Ball!</button>
  <div id="wrecking-ball"></div>

  <!-- Random Building Quote Button -->
  <button class="fun-btn" id="quoteBtn">Get an Architecture Quote!</button>
  <div id="quote-box"></div>

  <footer>
    <p>© 2024 Fun Architect. Master of questionable designs and fun buttons!</p>
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
    const skyscraper = document.getElementById('skyscraper');
    buildBtn.addEventListener('click', function() {
      skyscraper.style.height = "300px"; // Build the skyscraper
    });

    // Wrecking Ball Functionality
    const wreckBtn = document.getElementById('wreckBtn');
    const wreckingBall = document.getElementById('wrecking-ball');
    wreckBtn.addEventListener('click', function() {
      if (wreckingBall.style.display === "none") {
        wreckingBall.style.display = "block";
        wreckSkyscraper();
      }
    });

    // Function to wreck the skyscraper
    function wreckSkyscraper() {
      let height = 300; // Starting height of the skyscraper
      const interval = setInterval(() => {
        if (height > 0) {
          height -= 30; // Decrease height by 30px
          skyscraper.style.height = height + 'px';
        } else {
          clearInterval(interval); // Stop wrecking once it's fully demolished
        }
      }, 300); // Wreck every 300 milliseconds for a dramatic effect
    }

    // Random Building Quotes
    const quoteBtn = document.getElementById('quoteBtn');
    const quoteBox = document.getElementById('quote-box');
    const quotes = [
      "A doctor can bury his mistakes, but an architect can only advise his clients to plant vines. - Frank Lloyd Wright",
      "Architecture should speak of its time and place, but yearn for timelessness. - Frank Gehry",
      "To provide meaningful architecture is not to parody history, but to articulate it. - Daniel Libeskind",
      "I don't build in order to have clients. I have clients in order to build. - Ayn Rand",
      "Form ever follows function. - Louis Sullivan"
    ];

    quoteBtn.addEventListener('click', function() {
      const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
      quoteBox.innerText = randomQuote;
      quoteBox.style.display = "block";
    });
  </script>

</body>
</html>
