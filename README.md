<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf</title>

    <!-- Google Fonts for Typography -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            width: 100%;
            height: 100%;
            margin: 0;
            font-family: 'Segoe UI', Arial, sans-serif;
            scroll-behavior: smooth;
            background-color: #f5f5f5;
            color: #333;
            overflow-x: hidden; /* Prevent horizontal scrolling */
        }

        /* Intro Section */
        .intro-section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f5e6cc; /* Soft beige color */
            position: relative;
        }

        /* Title across the screen */
        .title-bar {
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            transform: translateY(-50%);
            display: flex;
            justify-content: space-between;
            padding: 0 20px;
            font-size: 1.5rem;
            font-weight: 700;
            color: #556b2f;
            white-space: nowrap;
            max-width: 100vw;
        }

        /* Menu */
        .menu {
            position: absolute;
            bottom: 40px;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            font-size: 1rem;
        }

        .menu a {
            text-decoration: none;
            color: #556b2f;
            font-weight: 600;
            transition: color 0.3s;
        }

        .menu a:hover {
            color: #b5651d;
        }

        /* Sections */
        .section {
            width: 100vw;
            padding: 6rem 2rem;
            opacity: 1;
            transition: opacity 1s ease-in-out;
            display: flex;
            flex-direction: column;
            align-items: center; /* Center the content */
            justify-content: center;
        }

        .section h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #556b2f;
            font-weight: 400; /* Light, sleek font */
        }

        /* Project Grid */
        .project-grid {
            display: flex;
            flex-direction: column;
            gap: 4rem;
            max-width: 100%;
            align-items: center;
            justify-content: center;
        }

        .project {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 2rem;
            cursor: pointer;
            width: 80%; /* Centered and occupies 80% of the width */
            max-width: 1200px;
        }

        .project:nth-child(odd) {
            flex-direction: row-reverse;
        }

        .project img {
            width: 50%;
            height: 400px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .project:hover img {
            transform: scale(1.05);
        }

        .project-info {
            width: 50%;
            padding: 1rem;
            position: relative;
        }

        .project-title {
            font-size: 1.8rem;
            font-weight: 600;
            color: #556b2f;
            text-align: center;
            background: rgba(255, 255, 255, 0.8);
            padding: 1rem;
            transition: background 0.3s;
            opacity: 0;
            visibility: hidden;
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }

        /* Reveal project title on hover */
        .project:hover .project-title {
            opacity: 1;
            visibility: visible;
        }

        /* Art Section Grid */
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            width: 100vw;
            align-items: center;
            justify-content: center;
        }

        .art-card {
            background-color: #f5f5f5;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .art-card:hover {
            transform: translateY(-5px);
        }

        .art-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        /* Contact Info */
        .contact-info p {
            margin-bottom: 0.5rem;
            font-weight: 400;
        }

        .contact-info a {
            color: #b5651d;
            text-decoration: none;
        }

        /* Footer Section */
        .footer {
            background-color: #556b2f;
            color: #f5f5f5;
            padding: 2rem 0;
            text-align: center;
        }

        .footer a {
            color: #f5f5f5;
            margin: 0 10px;
            font-size: 1.2rem;
            text-decoration: none;
        }

        /* Show sections when scrolled */
        .scroll-active {
            opacity: 1 !important;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .title-bar {
                font-size: 1rem;
                flex-direction: column;
                align-items: center;
                text-align: center;
            }

            .menu {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }

            .project {
                flex-direction: column;
            }

            .project img, .project-info {
                width: 100%;
            }

            .section {
                padding: 4rem 1rem;
            }

            .section h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <!-- Intro Section -->
    <section class="intro-section">
        <div class="title-bar">
            <div>MSc Architect</div>
            <span>Tine Kierulf</span>
            <div>MNAL</div>
        </div>

        <!-- Menu at the bottom -->
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <!-- Project 1: Badehus -->
            <div class="project">
                <img src="Badehus%20regn.png" alt="Badehus Project 1">
                <div class="project-info">
                    <div class="project-title">Badehus - Rainy View</div>
                </div>
            </div>

            <div class="project">
                <img src="Badehus%20ute.png" alt="Badehus Project 2">
                <div class="project-info">
                    <div class="project-title">Badehus - Outside View</div>
                </div>
            </div>

            <div class="project">
                <img src="Badehus%20vindu.png" alt="Badehus Window View">
                <div class="project-info">
                    <div class="project-title">Badehus - Window View</div>
                </div>
            </div>

            <!-- Project 2: Grounded -->
            <div class="project">
                <img src="Grounded%20inngang.png" alt="Grounded Entrance">
                <div class="project-info">
                    <div class="project-title">Grounded - Entrance</div>
                </div>
            </div>

            <div class="project">
                <img src="Grounded%20refleksjon.png" alt="Grounded Reflection">
                <div class="project-info">
                    <div class="project-title">Grounded - Reflection</div>
                </div>
            </div>

            <!-- Project 3: Master Thesis -->
            <div class="project">
                <img src="Master%201.png" alt="Master Thesis Image 1">
                <div class="project-info">
                    <div class="project-title">Master Thesis - Overview 1</div>
                </div>
            </div>

            <div class="project">
                <img src="Master%202.png" alt="Master Thesis Image 2">
                <div class="project-info">
                    <div class="project-title">Master Thesis - Overview 2</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Art Section -->
    <section id="art" class="section">
        <h2>Art Gallery</h2>
        <div class="art-grid">
            <div class="art-card">
                <img src="Maleri%201.jpg" alt="Art 1">
            </div>
            <div class="art-card">
                <img src="Maleri%202.jpg" alt="Art 2">
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2>Contact</h2>
        <div class="contact-info">
            <p>Email: <a href="mailto:tine.kierulf@hotmail.com">tine.kierulf@hotmail.com</a></p>
            <p>Phone: +47 916 80 318</p>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>© 2024 Arkitekt Tine Kierulf. All Rights Reserved.</p>
        <p>Follow me on:
            <a href="#">Instagram</a> |
            <a href="#">LinkedIn</a>
        </p>
    </footer>

    <script>
        // Smooth fade-in of sections after scrolling
        window.addEventListener('scroll', function () {
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;
                if (sectionTop < window.innerHeight * 0.8) {
                    section.classList.add('scroll-active');
                }
            });
        });
    </script>
</body>
</html>
