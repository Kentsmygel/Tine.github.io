<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Architectural Marvels & Misadventures</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to [Your Name]'s Marvelous Architecture Portfolio</h1>
    <p>"Designing spaces... and sometimes knocking over the occasional lamp."</p>
  </header>

  <nav>
    <ul>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#bio">About Me</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section id="projects">
    <h2>My Greatest (and Funniest) Projects</h2>

    <div class="project">
      <h3>The Wobbly Tower</h3>
      <img src="images/wobbly_tower.jpg" alt="Wobbly Tower" />
      <p>This building has a unique 'lean'—totally intentional. Some call it avant-garde; others call it a "structural concern." But hey, it hasn’t fallen yet!</p>
    </div>

    <div class="project">
      <h3>The Floating Pavilion</h3>
      <img src="images/floating_pavilion.jpg" alt="Floating Pavilion" />
      <p>This project was supposed to 'float on air.' But gravity disagreed. Now it 'floats' with a foundation so deep, it could be Atlantis' cousin.</p>
    </div>

    <div class="project">
      <h3>The Invisible House</h3>
      <img src="images/invisible_house.jpg" alt="Invisible House" />
      <p>A brilliant concept that nobody ever saw. Like, literally. If you find it, let me know. Reward offered.</p>
    </div>
  </section>

  <section id="bio">
    <h2>About Me</h2>
    <p>I'm [Your Name], an architect with big ideas and an even bigger collection of coffee mugs. I've designed everything from sky-high skyscrapers to stylish doghouses. When I'm not obsessing over blueprints, you can find me wondering why my plants never survive in the office.</p>
  </section>

  <section id="contact">
    <h2>Contact Me</h2>
    <p>If you're interested in my work (or just want to talk about architecture memes), feel free to reach out!</p>
    <form id="contactForm">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>

      <label for="message">Message:</label>
      <textarea id="message" name="message" required></textarea>

      <button type="submit">Send Message</button>
    </form>
  </section>

  <footer>
    <p>© 2024 [Your Name] Architecture. All rights (and wrongs) reserved.</p>
  </footer>

  <script src="scripts.js"></script>
</body>
</html>
