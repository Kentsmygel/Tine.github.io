<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arkitekt Tine Kierulf</title>
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
            font-family: 'Montserrat', sans-serif;
            scroll-behavior: smooth;
            background-color: #f5f5f5;
            color: #333;
            overflow-x: hidden;
        }

        .intro-section {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #f5e6cc;
            position: relative;
            width: 100vw;
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
            font-weight: 600;
            color: #556b2f;
            white-space: nowrap;
            width: 100%;
        }

        .menu {
            position: absolute;
            bottom: 40px;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            font-size: 1rem;
            width: 100%;
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

        .section {
            width: 100%;
            padding: 4rem 2rem;
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

        .project-grid {
            display: flex;
            flex-direction: column;
            gap: 4rem;
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
            gap: 2rem;
            cursor: pointer;
            width: 100%;
        }

        .project:nth-child(even) {
            flex-direction: row-reverse;
        }

        .project img {
            width: 60%;
            height: auto;
            max-height: 400px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .project:hover img {
            transform: scale(1.05);
        }

        .project-info {
            width: 40%;
            padding: 1rem;
            position: relative;
        }

        .project-title {
            font-size: 1.2rem;
            font-weight: 300;
            color: #556b2f;
            text-align: center;
            padding: 1rem;
            transition: opacity 0.3s;
            opacity: 0;
            visibility: hidden;
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            width: 100%;
            background-color: rgba(255, 255, 255, 0.9);
        }

        .project:hover .project-title {
            opacity: 1;
            visibility: visible;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.8);
        }

        .modal-content {
            background-color: #f5f5f5;
            margin: 5% auto;
            padding: 20px;
            border: 1px solid #888;
            width: 80%;
            max-width: 800px;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: #000;
            text-decoration: none;
            cursor: pointer;
        }

        .modal-image {
            width: 100%;
            max-height: 400px;
            object-fit: cover;
            margin-bottom: 20px;
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
                flex-direction: column !important;
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
            <div>MSc Architect</div>
            <span>Tine Kierulf</span>
            <div>MNAL</div>
        </div>
        <div class="menu">
            <a href="#projects">Projects</a>
            <a href="#art">Art</a>
            <a href="#contact">Contact</a>
        </div>
    </section>

    <section id="projects" class="section">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <!-- Project 1: Badehus -->
            <div class="project" data-project="badehus">
                <img src="Badehus%20regn.png" alt="Badehus Project 1">
                <div class="project-info">
                    <div class="project-title">
                        Badehus - Rainy View<br>
                        <span>A community bathhouse designed to blend with its natural surroundings, featuring large windows to capture light and views of the sea.</span>
                    </div>
                </div>
            </div>

            <!-- Project 2: Grounded -->
            <div class="project" data-project="grounded">
                <img src="Grounded%20inngang.png" alt="Grounded Entrance">
                <div class="project-info">
                    <div class="project-title">
                        Grounded - Entrance<br>
                        <span>An underground mindfulness space designed to promote relaxation and a deeper connection to nature.</span>
                    </div>
                </div>
            </div>

            <!-- Project 3: Master Thesis -->
            <div class="project" data-project="master-thesis">
                <img src="Master%201.png" alt="Master Thesis Image 1">
                <div class="project-info">
                    <div class="project-title">
                        Master Thesis - Overview 1<br>
                        <span>A comprehensive design proposal showcasing sustainable practices in urban settings.</span>
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

    <!-- Modal for project details -->
    <div id="projectModal" class="modal">
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2 id="modalTitle"></h2>
            <img id="modalImage" class="modal-image" src="" alt="Project Image">
            <p id="modalDescription"></p>
        </div>
    </div>

    <script>
        // Existing scroll event listeners...

        // Project modal functionality
        const modal = document.getElementById("projectModal");
        const modalTitle = document.getElementById("modalTitle");
        const modalImage = document.getElementById("modalImage");
        const modalDescription = document.getElementById("modalDescription");
        const closeBtn = document.getElementsByClassName("close")[0];

        const projects = document.querySelectorAll('.project');
        projects.forEach(project => {
            project.addEventListener('click', () => {
                const projectId = project.getAttribute('data-project');
                openModal(projectId);
            });
        });

        closeBtn.onclick = function() {
            modal.style.display = "none";
        }

        window.onclick = function(event) {
            if (event.target == modal) {
                modal.style.display = "none";
            }
        }

        function openModal(projectId) {
            // You would typically fetch this data from a server
            const projectDetails = {
                'badehus': {
                    title: 'Badehus Project',
                    image: 'Badehus%20regn.png',
                    description: 'The Badehus project is a community bathhouse designed to seamlessly integrate with its natural surroundings. It features large windows that capture abundant natural light and provide stunning views of the sea. The design emphasizes a connection between indoor and outdoor spaces, creating a serene and rejuvenating environment for visitors.'
                },
                'grounded': {
                    title: 'Grounded Project',
                    image: 'Grounded%20inngang.png',
                    description: 'Grounded is an innovative underground mindfulness space that aims to promote relaxation and foster a deeper connection with nature. The project incorporates elements of biophilic design, using natural materials and integrating vegetation to create a calming atmosphere. The unique subterranean setting offers a retreat from the outside world, allowing visitors to focus inward and find peace.'
                },
                'master-thesis': {
                    title: 'Master Thesis Project',
                    image: 'Master%201.png',
                    description: 'This master thesis project presents a comprehensive design proposal that showcases sustainable practices in urban settings. The work explores innovative approaches to city planning, incorporating green spaces, energy-efficient buildings, and sustainable transportation solutions. The project demonstrates a holistic approach to urban development, considering environmental impact, social cohesion, and economic viability.'
                }
            };

            const project = projectDetails[projectId];
            modalTitle.textContent = project.title;
            modalImage.src = project.image;
            modalDescription.textContent = project.description;
            modal.style.display = "block";
        }
    </script>
</body>
</html>
