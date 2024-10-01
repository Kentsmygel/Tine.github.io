<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            font-family: 'Montserrat', sans-serif;
            background-color: #f5f5f5;
            color: #333;
            overflow-x: hidden;
        }

        /* Intro Section */
        .intro {
            height: 100vh; /* Full height of viewport */
            width: 100vw;  /* Full width of viewport */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f5e6cc;
            text-align: center;
        }

        .title {
            font-size: 3rem;
            font-weight: 600;
        }

        .subtitle {
            font-size: 1.5rem;
            margin: 20px 0;
        }

        /* Navigation Menu */
        .menu {
            position: absolute;
            top: 20px;
            right: 20px;
            display: flex;
            gap: 20px;
        }

        .menu a {
            text-decoration: none;
            color: #556b2f;
            font-weight: 600;
        }

        .menu a:hover {
            color: #b5651d;
        }

        /* Projects Section */
        .projects {
            width: 100%; 
            padding: 0px 0px;
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: auto;
        }

        .project {
            display: flex;
            width: 100%;
            margin: 20px 0;
            align-items: center;
            justify-content: space-between;
            transition: transform 0.3s;
            overflow: hidden;
        }

        .project img {
            max-width: 100%;
            height: auto;
            max-height: 400px; /* Limit maximum height */
            transition: transform 0.3s;
        }

        .project-info {
            width: 50%;
            padding: 20px;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }

        .project:hover img {
            transform: scale(1.05);
        }

        .project:hover .project-info {
            opacity: 1;
            visibility: visible;
        }

        .project:nth-child(even) {
            flex-direction: row-reverse;
        }

        .project-title {
            font-size: 1.2rem;
            font-weight: 300;
            color: #556b2f;
            text-align: center;
            padding: 10px;
        }

        /* Art Section */
        .art-gallery {
            width: 1200px;
            padding: 50px 20px;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin: auto;
        }

        .art-card {
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .art-card:hover {
            transform: translateY(-5px);
        }

        .art-card img {
            width: 100%;
            height: auto;
        }

        /* Contact Section */
        .contact {
            width: 1200px;
            padding: 50px 20px;
            text-align: center;
            margin: auto;
        }

        /* Footer Section */
        .footer {
            background-color: #556b2f;
            color: #f5f5f5;
            padding: 20px;
            text-align: center;
        }

        .footer a {
            color: #f5f5f5;
            margin: 0 10px;
            text-decoration: none;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .project {
                flex-direction: column;
            }

            .project img {
                width: 100%;
            }

            .project-info {
                width: 100%;
            }

            .menu {
                flex-direction: column;
            }

            .projects,
            .art-gallery,
            .contact {
                width: 100%;
                padding: 0 10px;
            }
        }
    </style>
</head>

<body>
    <!-- Intro Section -->
    <div class="intro">
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
        <h1 class="title">MSc Architect</h1>
        <h2 class="subtitle">Tine Kierulf</h2>
        <h3 class="subtitle">MNAL</h3>
    </div>

    <!-- Projects Section -->
    <div id="projects" class="projects">
        <h2>Featured Projects</h2>
        <div class="project">
            <img src="Badehus regn.png" alt="Badehus Project 1">
            <div class="project-info">
                <div class="project-title">Badehus - Rainy View<br>
                    <span>A community bathhouse designed to blend with its natural surroundings.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Badehus ute.png" alt="Badehus Project 2">
            <div class="project-info">
                <div class="project-title">Badehus - Outside View<br>
                    <span>A sleek design, merging into the landscape.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Badehus vindu.png" alt="Badehus Window View">
            <div class="project-info">
                <div class="project-title">Badehus - Window View<br>
                    <span>Innovative use of glass to frame the views.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Grounded inngang.png" alt="Grounded Entrance">
            <div class="project-info">
                <div class="project-title">Grounded - Entrance<br>
                    <span>An underground mindfulness space designed for relaxation.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Grounded refleksjon.png" alt="Grounded Reflection">
            <div class="project-info">
                <div class="project-title">Grounded - Reflection<br>
                    <span>A reflective area incorporating natural light and water.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Master 1.png" alt="Master Thesis Image 1">
            <div class="project-info">
                <div class="project-title">Master Thesis - Overview 1<br>
                    <span>A comprehensive design proposal showcasing sustainability.</span>
                </div>
            </div>
        </div>

        <div class="project">
            <img src="Master 2.png" alt="Master Thesis Image 2">
            <div class="project-info">
                <div class="project-title">Master Thesis - Overview 2<br>
                    <span>Exploring innovative materials in architecture.</span>
                </div>
            </div>
        </div>
    </div>

    <!-- Art Section -->
    <div id="art" class="art-gallery">
        <h2>Art Gallery</h2>
        <div class="art-card">
            <img src="Maleri 1.jpg" alt="Art 1">
        </div>
        <div class="art-card">
            <img src="Maleri 2.jpg" alt="Art 2">
        </div>
    </div>

    <!-- Contact Section -->
    <div id="contact" class="contact">
        <h2>Contact</h2>
        <p>Email: <a href="mailto:tine.kierulf@hotmail.com">tine.kierulf@hotmail.com</a></p>
        <p>Phone: +47 916 80 318</p>
    </div>

    <!-- Footer -->
    <footer class="footer">
        <p>© 2024 Arkitekt Tine Kierulf. All Rights Reserved.</p>
        <p>Follow me on:
            <a href="#">Instagram</a> |
            <a href="#">LinkedIn</a>
        </p>
    </footer>
</body>

</html>
