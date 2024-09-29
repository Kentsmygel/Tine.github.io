<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf</title>

    <!-- Google Fonts for Typography -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">

    <!-- External CSS for icons (language switcher, etc.) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

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
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        /* Full screen layout for the intro section */
        .intro-section {
            height: 100vh;
            width: 100vw;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f5e6cc; /* Soft beige color */
            position: relative;
        }

        /* Title across the screen */
        .title-bar {
            display: flex;
            justify-content: space-between;
            width: 100%;
            padding: 1rem 2rem;
            color: #333;
            font-size: 2rem;
            font-family: 'Roboto Slab', serif;
            letter-spacing: 0.1rem;
        }
        .title-bar span {
            flex: 1;
            text-align: center;
        }

        /* Menu */
        .menu {
            position: absolute;
            top: 20px;
            right: 20px;
            display: flex;
            gap: 1.5rem;
            font-size: 1rem;
        }
        .menu a {
            text-decoration: none;
            color: #333;
            font-weight: 600;
            transition: color 0.3s;
        }
        .menu a:hover {
            color: #6b8f42;
        }

        /* Language Switcher (Flag icons) */
        .language-switcher {
            position: absolute;
            top: 20px;
            left: 20px;
            display: flex;
            gap: 1rem;
        }
        .language-switcher img {
            width: 30px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .language-switcher img:hover {
            transform: scale(1.1);
        }

        /* Projects Section */
        .projects-section {
            width: 100vw;
            padding: 6rem 2rem;
            background-color: #ffffff;
            text-align: center;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }
        .projects-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
            color: #333;
        }
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 0 2rem;
        }
        .project-card {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .project-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            transition: transform 0.3s;
        }
        .project-card:hover img {
            transform: scale(1.1);
        }
        .project-info {
            padding: 1rem;
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

        /* CV Section */
        .cv-section {
            padding: 6rem 2rem;
            background-color: #f7f7f7;
            text-align: center;
        }
        .cv-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
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
        .cv-download {
            margin-top: 2rem;
            font-size: 1.2rem;
            font-weight: 600;
            color: #6b8f42;
        }

        /* Art Section */
        .art-section {
            padding: 6rem 2rem;
            background-color: #ffffff;
            text-align: center;
        }
        .art-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
        }
        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        .art-card {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
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

        /* Contact Section */
        .contact-section {
            padding: 6rem 2rem;
            background-color: #f7f7f7;
            text-align: center;
        }
        .contact-section h2 {
            font-family: 'Roboto Slab', serif;
            font-size: 3rem;
            margin-bottom: 3rem;
        }
        .contact-info {
            font-size: 1.2rem;
            margin-bottom: 1rem;
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
            color: #6b8f42;
            margin: 0 10px;
            font-size: 1.2rem;
        }

        /* Smooth Scroll Animations */
        .scroll-active {
            opacity: 1 !important;
        }

        /* Mobile Responsive Adjustments */
        @media (max-width: 768px) {
            .title-bar {
                flex-direction: column;
                text-align: center;
                font-size: 1.5rem;
                letter-spacing: 0.05rem;
            }
            .menu {
                font-size: 0.9rem;
            }
            .language-switcher img {
                width: 25px;
            }
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Language Switcher with Norwegian and English Flags -->
    <div class="language-switcher">
        <img src="norwegian-flag.png" alt="Norwegian" onclick="changeLanguage('no')">
        <img src="english-flag.png" alt="English" onclick="changeLanguage('en')">
    </div>

    <!-- Minimalist Intro Section -->
    <section class="intro-section">
        <div class="title-bar">
            <div>MSc Architect</div>
            <span>Tine Kierulf</span>
            <div>MNAL</div>
        </div>
        <!-- Simple Menu -->
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#cv">CV</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects-section">
        <h2>Selected Projects</h2>
        <div class="projects-grid">
            <!-- Project 1: PULS Bathhouse -->
            <div class="project-card">
                <img src="Bathhouse_Rain" alt="PULS Bathhouse">
                <div class="project-info">
                    <h3 class="project-title">PULS Bathhouse</h3>
                    <p class="project-description">A pro-bono bathhouse project in Åsgårdstrand, designed to connect the local community with its history.</p>
                </div>
            </div>
            <!-- Project 2: Master Thesis - Reimagining Munch Museum -->
            <div class="project-card">
                <img src="https://source.unsplash.com/300x200/?museum" alt="Munch Museum">
                <div class="project-info">
                    <h3 class="project-title">Master Thesis - Munch Museum Reimagined</h3>
                    <p class="project-description">Biophilic public space redesign of the former Munch Museum, revitalizing the Tøyen borough in Oslo.</p>
                </div>
            </div>
            <!-- Project 3: Grounded Project -->
            <div class="project-card">
                <img src="https://source.unsplash.com/300x200/?underground" alt="Grounded Project">
                <div class="project-info">
                    <h3 class="project-title">Grounded - Mindfulness Space</h3>
                    <p class="project-description">Underground space in Oslo Center promoting mindfulness through interaction with light and a rediscovered river.</p>
                </div>
            </div>
            <!-- Project 4: New European Bauhaus -->
            <div class="project-card">
                <img src="https://source.unsplash.com/300x200/?architecture" alt="New European Bauhaus">
                <div class="project-info">
                    <h3 class="project-title">New European Bauhaus</h3>
                    <p class="project-description">A design solution for a future European University, focused on sustainable teaching and earthen architecture.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CV Section -->
    <section id="cv" class="cv-section">
        <h2>Curriculum Vitae</h2>
        <div class="cv-content">
            <h3>Experience</h3>
            <p><strong>Independent Architect</strong> - Arkitekt Tine Kierulf, 2023-present</p>
            <p><strong>Lead Architect</strong> - Badehuset PULS project, Norway</p>
            <p><strong>Speaker</strong> - New European Bauhaus Conference, 2022</p>
            <div class="cv-download">
                <a href="Tine-2023-Portfolio.pdf" download>Download Full CV (PDF)</a>
            </div>
        </div>
    </section>

    <!-- Art Section -->
    <section id="art" class="art-section">
        <h2>Art Portfolio</h2>
        <div class="art-grid">
            <div class="art-card">
                <img src="https://source.unsplash.com/300x300/?watercolor" alt="Art 1">
            </div>
            <div class="art-card">
                <img src="https://source.unsplash.com/300x300/?art" alt="Art 2">
            </div>
            <!-- Add more art cards as needed -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact-section">
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
            <a href="#">LinkedIn</a> |
            <a href="#">Twitter</a>
        </p>
    </footer>

    <script>
        /* Function to handle language change */
        function changeLanguage(lang) {
            if (lang === 'no') {
                // Change all text to Norwegian
                document.querySelector('.title-bar span').textContent = 'Tine Kierulf';
                document.querySelector('.menu a[href="#projects"]').textContent = 'Prosjekter';
                document.querySelector('.menu a[href="#cv"]').textContent = 'CV';
                document.querySelector('.menu a[href="#art"]').textContent = 'Kunst';
                document.querySelector('.menu a[href="#contact"]').textContent = 'Kontakt';
                document.querySelector('#cv h2').textContent = 'Curriculum Vitae';
                document.querySelector('#art h2').textContent = 'Kunst';
            } else {
                // Change all text to English
                document.querySelector('.title-bar span').textContent = 'Tine Kierulf';
                document.querySelector('.menu a[href="#projects"]').textContent = 'Projects';
                document.querySelector('.menu a[href="#cv"]').textContent = 'CV';
                document.querySelector('.menu a[href="#art"]').textContent = 'Art';
                document.querySelector('.menu a[href="#contact"]').textContent = 'Contact';
                document.querySelector('#cv h2').textContent = 'Curriculum Vitae';
                document.querySelector('#art h2').textContent = 'Art';
            }
        }

        // Smooth reveal of sections after scroll
        window.addEventListener('scroll', function () {
            const sections = document.querySelectorAll('.projects-section, .cv-section, .art-section');
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
