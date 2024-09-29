<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tine Kierulf - Architect MNAL</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --cream: #F5E6D3;
            --beige: #E6D2B5;
            --olive: #8A8558;
            --terracotta: #C66E4E;
            --dark-olive: #4A4A40;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body, html {
            font-family: 'Segoe UI', Arial, sans-serif;
            scroll-behavior: smooth;
            background-color: var(--cream);
            color: var(--dark-olive);
        }

        .intro-section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: var(--beige);
            position: relative;
        }

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
            color: var(--olive);
            white-space: nowrap;
        }

        .menu {
            position: absolute;
            bottom: 40px;
            display: flex;
            gap: 1.5rem;
            font-size: 1rem;
        }

        .menu a {
            text-decoration: none;
            color: var(--olive);
            font-weight: 600;
            transition: color 0.3s;
        }

        .menu a:hover {
            color: var(--terracotta);
        }

        .section {
            padding: 6rem 2rem;
            opacity: 0;
            transition: opacity 1s ease-in-out;
        }

        .section h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: var(--olive);
        }

        .project-grid {
            display: flex;
            flex-direction: column;
            gap: 4rem;
        }

        .project {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 2rem;
            position: relative;
            cursor: pointer;
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
            font-weight: bold;
            color: var(--olive);
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            transform: translateY(-50%);
            text-align: center;
            background: rgba(255, 255, 255, 0.8);
            padding: 1rem;
            transition: background 0.3s;
        }

        .project:hover .project-title {
            background: rgba(230, 210, 181, 0.8);
        }

        /* Hidden Project Details */
        .project-details {
            display: none;
            padding: 2rem;
        }

        .project.open .project-details {
            display: block;
        }

        .project.open img {
            width: 100%;
            transition: width 0.5s;
        }

        .art-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .art-card {
            background-color: var(--cream);
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

        .contact-info p {
            margin-bottom: 0.5rem;
        }

        .contact-info a {
            color: var(--terracotta);
            text-decoration: none;
        }

        .footer {
            background-color: var(--olive);
            color: var(--cream);
            padding: 2rem 0;
            text-align: center;
        }

        .footer a {
            color: var(--cream);
            margin: 0 10px;
            font-size: 1.2rem;
            text-decoration: none;
        }

        .scroll-active {
            opacity: 1 !important;
        }

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
    <section class="intro-section">
        <div class="title-bar">
            <span>MSc Architect</span>
            <span>Tine Kierulf</span>
            <span>MNAL</span>
        </div>
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#education">Education</a>
            <a href="#experience">Experience</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
    </section>

    <section id="projects" class="section">
        <h2>Selected Projects</h2>
        <div class="project-grid">
            <div class="project" id="badehuset">
                <img src="Badehus ute.png" alt="PULS Bathhouse Project">
                <div class="project-info">
                    <h3 class="project-title">PULS Bathhouse</h3>
                    <div class="project-details">
                        <p>A pro-bono project in Åsgårdstrand, inspired by the area's cultural history and evening sky. The bathhouse seeks to connect the community with nature and provide a tranquil, cultural space.</p>
                        <img src="Badehus inne.png" alt="PULS Bathhouse Interior">
                    </div>
                </div>
            </div>

            <div class="project" id="master-thesis">
                <img src="Master 1.png" alt="Master Thesis Project">
                <div class="project-info">
                    <h3 class="project-title">Master Thesis</h3>
                    <div class="project-details">
                        <p>Reimagining the former Munch Museum in Oslo as a biophilic public space, integrating nature and architecture to revitalize the community.</p>
                        <img src="Modell inne.jpg" alt="Master Thesis Model">
                    </div>
                </div>
            </div>

            <div class="project" id="grounded">
                <img src="Grounded inngang.png" alt="Grounded Project">
                <div class="project-info">
                    <h3 class="project-title">Grounded</h3>
                    <div class="project-details">
                        <p>An underground mindfulness space in central Oslo, restoring part of a forgotten river and creating a contemplative atmosphere for urban dwellers.</p>
                        <img src="Inspo.png" alt="Grounded Inspiration">
                    </div>
                </div>
            </div>

            <div class="project" id="neb">
                <img src="FORSIDE.png" alt="New European Bauhaus">
                <div class="project-info">
                    <h3 class="project-title">A New European Bauhaus</h3>
                    <div class="project-details">
                        <p>A theoretical project proposing a sustainable design for a European University focused on earth-based materials and environmentally conscious teaching practices.</p>
                        <img src="Texture.jpg" alt="Earth Textures for NEB">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="education" class="section">
        <h2>Education</h2>
        <div class="education-experience">
            <div class="education">
                <div class="item">
                    <h3 class="item-title">MSc Architecture (RIBA II), University of Liechtenstein</h3>
                    <p class="item-description">RIBA 1 and 2 accreditation. Thesis focused on integrating biophilic design and environmental psychological patterns in architecture.</p>
                </div>
                <div class="item">
                    <h3 class="item-title">BSc Building Design, University of Agder</h3>
                    <p class="item-description">Civil Engineering degree with electives in Architecture, Urban Planning and Development, Project Management, and Static Calculations.</p>
                </div>
                <div class="item">
                    <h3 class="item-title">Philosophy, NTNU</h3>
                    <p class="item-description">One-year study in philosophy focusing on aesthetics and ethics.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="experience" class="section">
        <h2>Experience</h2>
        <div class="education-experience">
            <div class="experience">
                <div class="item">
                    <h3 class="item-title">Architect Tine Kierulf</h3>
                    <p class="item-description">Self-employed architecture and design business. Working on the Badehuset PULS project and continuous projects in interior design, gardens, pergolas, art, and consultation on other bathhouse projects.</p>
                </div>
                <div class="item">
                    <h3 class="item-title">SEIAA Impact Academy</h3>
                    <p class="item-description">Participated in an international workshop on mediating constraints in building and architecture.</p>
                </div>
                <div class="item">
                    <h3 class="item-title">Speaker at NEB Conference for the European Commission</h3>
                    <p class="item-description">Invited by honorary UNESCO professor Anna Heringer as a guest lecturer at a conference organized by the European Commission, focusing on clay architecture.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="art" class="section">
        <h2>Art Portfolio</h2>
        <p>I enjoy hand drawing and watercolor painting, featuring both landscape and urban motifs.</p>
        <div class="art-grid">
            <div class="art-card">
                <img src="Maleri 1.jpg" alt="Painting 1">
            </div>
            <div class="art-card">
                <img src="Maleri 2.jpg" alt="Painting 2">
            </div>
            <div class="art-card">
                <img src="Modell 2.jpg" alt="Model 2">
            </div>
            <div class="art-card">
                <img src="Modell inne.jpg" alt="Interior Model">
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <h2>Contact</h2>
        <div class="contact-info">
            <p>Email: <a href="mailto:tine.kierulf@hotmail.com">tine.kierulf@hotmail.com</a></p>
            <p>Phone: +47 91 68 03 18</p>
            <p>Location: Oslo, Norway</p>
        </div>
    </section>

    <footer class="footer">
        <p>&copy; 2024 Tine Kierulf. All rights reserved.</p>
        <div>
            <a href="#" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="#" title="Instagram"><i class="fab fa-instagram"></i></a>
        </div>
    </footer>

  <!DOCTYPE html>
<html lang="en">
<head>
    <!-- ... -->
    <style>
        /* ... */
    </style>
</head>
<body>
    <!-- ... -->
    <section id="projects" class="section">
        <!-- ... -->
        <div class="project-grid">
            <div class="project-card">
                <!-- ... -->
                <div class="project-info">
                    <!-- ... -->
                </div>
            </div>
            <!-- ... -->
        </div>
    </section>
    <!-- ... -->
    <footer class="footer">
        <!-- ... -->
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const projects = document.querySelectorAll('.project-card');

            projects.forEach(project => {
                project.addEventListener('click', function() {
                    this.classList.toggle('open');
                });
            });
        });
    </script>
</body>
</html>
        document.addEventListener('DOMContentLoaded', function () {
            const sections = document.querySelectorAll('.section');

            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('scroll-active');
                    }
                });
            }, { threshold: 0.1 });

            sections.forEach(section => {
                observer.observe(section);
            });

            // Toggle project details on click
            const projects
.project-card {
    /* ... */
}

.project-card.open .project-info {
    display: block;
}

.project-card:not(.open) .project-info {
    display: none;
}
