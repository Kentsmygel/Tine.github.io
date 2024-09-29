<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tine Kierulf - Architect MNAL</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* (Keep the existing CSS styles, but add or modify the following) */
        :root {
            --cream-white: #F5F5DC;
            --olive: #808000;
            --terracotta: #E2725B;
            --earthy-sage: #576E5A;
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background-color: var(--cream-white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .project-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .project-info {
            padding: 1rem;
        }
        
        .project-title {
            font-size: 1.2rem;
            color: var(--olive);
            margin-bottom: 0.5rem;
        }
        
        .project-description {
            font-size: 0.9rem;
            color: var(--earthy-sage);
        }
        
        .education-experience {
            display: flex;
            justify-content: space-between;
            margin-top: 2rem;
        }
        
        .education, .experience {
            width: 48%;
        }
        
        .section-title {
            font-size: 1.5rem;
            color: var(--olive);
            margin-bottom: 1rem;
        }
        
        .item {
            margin-bottom: 1rem;
        }
        
        .item-title {
            font-weight: bold;
            color: var(--terracotta);
        }
        
        .item-description {
            font-size: 0.9rem;
            color: var(--earthy-sage);
        }
    </style>
</head>
<body>
    <div class="language-switcher">
        <img src="norwegian-flag.png" alt="Norwegian" onclick="changeLanguage('no')">
        <img src="english-flag.png" alt="English" onclick="changeLanguage('en')">
    </div>

    <section class="intro-section">
        <div class="title-bar">
            <div>MSc Architect</div>
            <span>Tine Kierulf</span>
            <div>MNAL</div>
        </div>
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#education">Education</a>
            <a href="#experience">Experience</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
    </section>

    <section id="projects" class="projects-section">
        <h2>Selected Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <img src="Badehus ute.png" alt="PULS Bathhouse Project">
                <div class="project-info">
                    <h3 class="project-title">PULS Bathhouse</h3>
                    <p class="project-description">A pro-bono project in Åsgårdstrand, inspired by the area's cultural history and evening sky. Features a wave-like roof with reflective metal plates.</p>
                </div>
            </div>
            <div class="project-card">
                <img src="Master 1.png" alt="Master Thesis Project">
                <div class="project-info">
                    <h3 class="project-title">Master Thesis</h3>
                    <p class="project-description">Reimagining the former Munch Museum as a biophilic public space, revitalizing the Tøyen district in Oslo with a focus on biodiversity and environmental psychology.</p>
                </div>
            </div>
            <div class="project-card">
                <img src="Grounded inngang.png" alt="Grounded Project">
                <div class="project-info">
                    <h3 class="project-title">Grounded</h3>
                    <p class="project-description">An underground mindfulness space in central Oslo, restoring part of a forgotten river and manipulating light to create a sense of wonder and peace.</p>
                </div>
            </div>
            <div class="project-card">
                <img src="FORSIDE.png" alt="New European Bauhaus">
                <div class="project-info">
                    <h3 class="project-title">A New European Bauhaus</h3>
                    <p class="project-description">A design solution for a theoretical future university focusing on solution-oriented sustainable education.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="education-experience" class="education-experience">
        <div class="education">
            <h2 class="section-title">Education</h2>
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
        <div class="experience">
            <h2 class="section-title">Experience</h2>
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
    </section>

    <section id="art" class="art-section">
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

    <section id="contact" class="contact-section">
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

    <script>
        function changeLanguage(lang) {
            // Implement language change functionality here
            console.log("Changing language to: " + lang);
        }

        document.addEventListener('DOMContentLoaded', function() {
            const sections = document.querySelectorAll('.projects-section, .education-experience, .art-section, .contact-section');

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
        });
    </script>
</body>
</html>
