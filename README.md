<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tine Kierulf - Architecture & Art Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Open+Sans&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Open Sans', sans-serif;
            background-color: #fafafa;
            color: #333;
        }
        /* Navbar */
        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.9);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }
        .navbar ul {
            display: flex;
            justify-content: space-around;
            padding: 1rem;
            list-style-type: none;
        }
        .navbar ul li a {
            text-decoration: none;
            color: #333;
            font-size: 1.1rem;
            font-weight: bold;
            transition: color 0.3s;
        }
        .navbar ul li a:hover {
            color: #6b8f42;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background-image: url('https://source.unsplash.com/1600x900/?architecture');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-align: center;
        }
        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
        }
        .hero p {
            font-size: 1.5rem;
            margin-top: 1rem;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
        }

        /* Projects Section */
        .projects-section {
            padding: 4rem 2rem;
            background-color: #f5f5f5;
            text-align: center;
        }
        .projects-section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #333;
        }
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 0 2rem;
        }
        .project-card {
            background-color: white;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            border-radius: 10px;
            transition: transform 0.3s;
        }
        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            transition: transform 0.3s;
        }
        .project-card:hover img {
            transform: scale(1.05);
        }
        .project-info {
            padding: 1.5rem;
        }
        .project-title {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        .project-description {
            color: #777;
            font-size: 1rem;
        }

        /* Art Section */
        .art-section {
            padding: 4rem 2rem;
            text-align: center;
        }
        .art-section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            padding: 0 2rem;
        }
        .art-card {
            position: relative;
        }
        .art-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
        }
        .art-card:hover img {
            opacity: 0.8;
        }

        /* What I'm Working On Section */
        .working-section {
            padding: 4rem 2rem;
            background-color: #fafafa;
            text-align: center;
        }
        .working-section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }
        .working-content {
            max-width: 800px;
            margin: 0 auto;
            color: #555;
            font-size: 1.2rem;
        }

        /* CV Section */
        .cv-section {
            padding: 4rem 2rem;
            background-color: #e2efe2;
            text-align: center;
        }
        .cv-section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }
        .cv-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: left;
            font-size: 1.2rem;
            line-height: 1.8;
        }
        .cv-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        /* Footer Section */
        .footer {
            background-color: #333;
            color: #fff;
            padding: 2rem 0;
            text-align: center;
        }
        .footer p {
            font-size: 1rem;
            margin: 0.5rem 0;
        }
        .footer a {
            color: #6b8f42;
            margin: 0 10px;
            font-size: 1.2rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 3rem;
            }
            .projects-grid, .art-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar">
        <ul>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#art">Art</a></li>
            <li><a href="#working">What I'm Working On</a></li>
            <li><a href="#cv">CV</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div>
            <h1>Your Name</h1>
            <p>Architectural Designer & Visual Artist</p>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects-section">
        <h2>Featured Projects</h2>
        <div class="projects-grid">
            <!-- 6 Project Cards -->
            <div class="project-card">
                <img src="https://source.unsplash.com/300x200/?building1" alt="Project 1">
                <div class="project-info">
                    <h3 class="project-title">Modern Skyscraper</h3>
                    <p class="project-description">A sleek, innovative tower in the heart of the city.</p>
                </div>
            </div>
            <div class="project-card">
                <img src="https://source.unsplash.com/300x200/?building2" alt="Project 2">
                <div class="project-info">
                    <h3 class="project-title">Eco-friendly Office</h3>
                    <p class="project-description">A sustainable, green office space harmonizing with nature.</p>
                </div>
            </div>
            <!-- Add 4 more project cards similarly -->
        </div>
    </section>

    <!-- Art Section -->
    <section id="art" class="art-section">
        <h2>Art Gallery</h2>
        <div class="art-grid">
            <!-- Paintings or Artworks -->
            <div class="art-card">
                <img src="https://source.unsplash.com/250x300/?art1" alt="Painting 1">
            </div>
            <div class="art-card">
                <img src="https://source.unsplash.com/250x300/?art2" alt="Painting 2">
            </div>
            <!-- Add 4 more art cards similarly -->
        </div>
    </section>

    <!-- What I'm Working On Section -->
    <section id="working" class="working-section">
        <h2>What I’m Working On Now</h2>
        <div class="working-content">
            <p>Currently, I’m exploring sustainable architecture solutions and designing an eco-friendly retreat in a rural setting. I'm also creating a series of paintings inspired by natural landscapes and abstract forms.</p>
        </div>
    </section>

    <!-- CV Section -->
    <section id="cv" class="cv-section">
        <h2>Curriculum Vitae</h2>
        <div class="cv-content">
            <h3>Experience</h3>
            <p><strong>Lead Architect</strong> - ABC Design Studio, 2019-2023</p>
            <p><strong>Architectural Intern</strong> - XYZ Architects, 2017-2019</p>

            <h3>Education</h3>
            <p><strong>M.Arch</strong> - University of Design, 2016</p>
            <p><strong>B.Arch</strong> - University of Fine Arts, 2014</p>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="footer">
        <p>© 2024 Your Name - All Rights Reserved</p>
        <p>Contact: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
        <p>
            <a href="https://linkedin.com" target="_blank">LinkedIn</a> |
            <a href="https://instagram.com" target="_blank">Instagram</a> |
            <a href="https://behance.net" target="_blank">Behance</a>
        </p>
    </footer>

</body>
</html>
