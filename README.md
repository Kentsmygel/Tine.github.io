<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf</title>

    <!-- Google Fonts for Professional Sleek Typography -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">

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
            padding: 0;
            font-family: 'Montserrat', sans-serif;
            scroll-behavior: smooth;
            background-color: #f5f5f5;
            color: #333;
            overflow-x: hidden;
        }

        /* Intro Section */
        .intro-section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f5e6cc;
            position: relative;
            width: 100%;
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
            font-weight: 600;
            color: #556b2f;
            white-space: nowrap;
            max-width: 100%;
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
            width: 100%;
            padding: 6rem 2rem;
            opacity: 1;
            transition: opacity 1s ease-in-out;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .section h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #556b2f;
            font-weight: 400;
            text-transform: uppercase;
        }

        /* Project Grid */
        .project-grid {
            display: flex;
            flex-direction: column;
            gap: 8rem;
            max-width: 1200px;
            width: 100%;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
        }

        .project {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 5rem;
            cursor: pointer;
            width: 100%;
        }

        .project:nth-child(odd) {
            flex-direction: row-reverse;
        }

        .project img {
            width: 70%;
            height: 500px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .project:hover img {
            transform: scale(1.05);
        }

        .project-info {
            width: 30%;
            padding: 1rem;
            position: relative;
        }

        .project-title {
            font-size: 1.4rem;
            font-weight: 300;
            color: #556b2f;
            text-align: center;
            padding: 1rem;
            transition: background 0.3s;
            opacity: 0;
            visibility: hidden;
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 100%;
        }

        .project:hover .project-title {
            opacity: 1;
            visibility: visible;
        }

        /* Art Section Grid */
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 4rem;
            width: 100%;
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
            height: auto;
            object-fit: contain;
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
            padding: 1rem 0;
            text-align: center;
            width: 100%;
            display: none;
        }

        .footer.visible {
            display: block;
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

            .footer {
                padding: 0.8rem 0;
            }

            .project-grid {
                padding: 0 1rem;
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
                    <div class="project-title">
                        Badehus - Rainy View<br>
                        <span>A community bathhouse designed to blend with its natural surroundings, featuring large windows to capture light and views of the sea.</span>
                    </div>
                </div>
            </div>

            <div class="project">
                <img src="Badehus%20ute.png" alt="Badehus Project 2">
                <div class="project-info">
                    <div class="project-title">
                        Badehus - Outside View<br>
                        <span>A sleek design, the bathhouse merges into the landscape while maintaining a strong architectural presence.</span>
                    </div>
                </div>
            </div>

            <div class="project">
                <img src="Badehus%20vindu.png" alt="Badehus Window View">
                <div class="project-info">
                    <div class="project-title">
                        Badehus - Window View<br>
                        <span>Innovative use of glass to frame the views, creating an immersive connection with the surrounding environment.</span>
                    </div>
                </div>
            </div>

            <!-- Project 2: Grounded -->
            <div class="project">
                <img src="Grounded%20inngang.png" alt="Grounded Entrance">
                <div class="project-info">
                    <div class="project-title">
                        Grounded - Entrance<br>
                        <span>An underground mindfulness space designed to promote relaxation and a deeper connection to nature.</span>
                    </div>
                </div>
            </div>

            <div class="project">
                <img src="Grounded%20refleksjon.png" alt="Grounded Reflection">
                <div class="project-info">
                    <div class="project-title">
                        Grounded - Reflection<br>
                        <span>A reflective area that incorporates natural light and elements of water to enhance tranquility.</span>
                    </div>
                </div>
            </div>

            <!-- Project 3: Master Thesis -->
            <div class="project">
                <img src="Master%201.png" alt="Master Thesis Image 1">
                <div class="project-info">
                    <div class="project-title">
                        Master Thesis - Overview 1<br>
                        <span>A comprehensive design proposal showcasing sustainable practices in urban settings.</span>
                    </div>
                </div>
            </div>

            <div class="project">
                <img src="Master%202.png" alt="Master Thesis Image 2">
                <div class="project-info">
                    <div class="project-title">
                        Master Thesis - Overview 2<br>
                        <span>Exploring innovative materials and techniques in modern architecture.</span>
                    </div>
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

        // Show the footer only when the user reaches the bottom of the page
        window.addEventListener('scroll', function () {
            const footer = document.querySelector('.footer');
            if (window.innerHeight + window.scrollY >= document.body.offsetHeight) {
                footer.classList.add('visible');
            } else {
                footer.classList.remove('visible');
            }
        });
    </script>
</body>
</html>
