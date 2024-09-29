<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf - Architecture Portfolio</title>

    <!-- Google Fonts for modern typography -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f7f7f7;
            color: #333;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* Navbar */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.95);
            padding: 1rem;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        .navbar ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }
        .navbar ul li a {
            text-decoration: none;
            color: #333;
            font-weight: 600;
            font-size: 1.1rem;
            transition: color 0.3s;
        }
        .navbar ul li a:hover {
            color: #4CAF50;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background-image: url('https://source.unsplash.com/1600x900/?modern-building');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
            position: relative;
        }
        .hero h1 {
            font-family: 'Roboto Slab', serif;
            font-size: 6rem;
            letter-spacing: 1.5rem;
            text-transform: uppercase;
            background: rgba(0, 0, 0, 0.4);
            padding: 0.5rem 2rem;
            backdrop-filter: blur(6px);
        }
        .hero p {
            font-size: 1.5rem;
            margin-top: 1rem;
            background: rgba(0, 0, 0, 0.5);
            padding: 0.5rem;
            backdrop-filter: blur(6px);
            color: #e0e0e0;
        }
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0, 0, 0, 0.3);
        }

        /* Parallax Scrolling Effect */
        .parallax {
            background-image: url('https://source.unsplash.com/1600x900/?nature,light');
            height: 70vh;
            background-attachment: fixed;
            background-size: cover;
            background-position: center;
        }

        /* Projects Section with Carousel */
        .projects-section {
            padding: 6rem 2rem;
            background-color: #f4f4f4;
            text-align: center;
        }
        .projects-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
            color: #333;
        }
        .carousel-container {
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
        }
        .carousel-wrapper {
            display: flex;
            overflow: hidden;
            width: 80%;
            max-width: 1200px;
            border-radius: 10px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
        }
        .carousel-track {
            display: flex;
            transition: transform 0.4s ease;
        }
        .project-card {
            min-width: 300px;
            margin: 0 1rem;
            background-color: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
            transform-style: preserve-3d;
            perspective: 1000px;
        }
        .project-card:hover {
            transform: translateY(-10px) rotateY(3deg);
        }
        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .project-info {
            padding: 1.5rem;
        }
        .project-title {
            font-family: 'Roboto Slab', serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        .project-description {
            color: #777;
            font-size: 1rem;
        }

        /* Carousel Navigation */
        .carousel-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(255, 255, 255, 0.7);
            color: #333;
            border: none;
            padding: 1rem;
            cursor: pointer;
            z-index: 1;
            transition: background-color 0.3s;
        }
        .carousel-btn:hover {
            background-color: #333;
            color: white;
        }
        .prev-btn {
            left: -50px;
        }
        .next-btn {
            right: -50px;
        }

        /* Art Section */
        .art-section {
            padding: 6rem 2rem;
            text-align: center;
        }
        .art-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
        }
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        .art-card {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
        }
        .art-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            transition: transform 0.3s;
        }
        .art-card:hover img {
            transform: scale(1.1);
        }

        /* Footer Section */
        .footer {
            background-color: #333;
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        .footer p {
            font-size: 1rem;
            margin: 0.5rem 0;
        }
        .footer a {
            color: #4CAF50;
            margin: 0 10px;
            font-size: 1.2rem;
        }
    </style>
</head>

<body>
    <!-- Navbar -->
    <nav class="navbar">
        <div class="brand-logo">
            <h3>Arkitekt Tine Kierulf</h3>
        </div>
        <ul>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#art">Art</a></li>
            <li><a href="#working">Current Work</a></li>
            <li><a href="#cv">CV</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div>
            <h1>Arkitekt Tine Kierulf</h1>
            <p>Innovative Design | Timeless Architecture</p>
        </div>
    </section>

    <!-- Parallax Scrolling Section -->
    <div class="parallax"></div>

    <!-- Projects Section with Carousel -->
    <section id="projects" class="projects-section">
        <h2>Featured Projects</h2>
        <div class="carousel-container">
            <button class="carousel-btn prev-btn" onclick="moveCarousel(-1)">&#10094;</button>
            <div class="carousel-wrapper">
                <div class="carousel-track">
                    <!-- Carousel items -->
                    <div class="project-card">
                        <img src="https://source.unsplash.com/300x200/?modern-building1" alt="Project 1">
                        <div class="project-info">
                            <h3 class="project-title">Modern Villa</h3>
                            <p class="project-description">A minimalistic modern villa design.</p>
                        </div>
                    </div>
                    <div class="project-card">
                        <img src="https://source.unsplash.com/300x200/?modern-building2" alt="Project 2">
                        <div class="project-info">
                            <h3 class="project-title">Sustainable Office</h3>
                            <p class="project-description">Eco-friendly office space.</p>
                        </div>
                    </div>
                    <!-- Add more project cards -->
                </div>
            </div>
            <button class="carousel-btn next-btn" onclick="moveCarousel(1)">&#10095;</button>
        </div>
    </section>

    <!-- Art Section -->
    <section id="art" class="art-section">
        <h2>Art Portfolio</h2>
        <div class="art-grid">
            <div class="art-card">
                <img src="https://source.unsplash.com/300x300/?abstract-art1" alt="Art 1">
            </div>
            <div class="art-card">
                <img src="https://source.unsplash.com/300x300/?abstract-art2" alt="Art 2">
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>© 2024 Arkitekt Tine Kierulf. All Rights Reserved.</p>
        <p>Follow me on:
            <a href="#">Instagram</a> | 
            <a href="#">LinkedIn</a> | 
            <a href="#">Twitter</a>
        </p>
    </footer>

    <script>
        let currentSlide = 0;

        function moveCarousel(direction) {
            const track = document.querySelector('.carousel-track');
            const slides = document.querySelectorAll('.project-card');
            const slideWidth = slides[0].offsetWidth + 32;  // Including margin

            currentSlide = (currentSlide + direction + slides.length) % slides.length;
            track.style.transform = 'translateX(' + (-currentSlide * slideWidth) + 'px)';
        }
    </script>
</body>
</html>
