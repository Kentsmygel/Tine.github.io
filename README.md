<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Architecture Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Open+Sans&display=swap" rel="stylesheet">
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Open Sans', sans-serif;
            scroll-behavior: smooth;
            background-color: #f4f4f4;
        }

        /* Global Styles */
        h1, h2, h3 {
            font-family: 'Montserrat', sans-serif;
        }
        a {
            text-decoration: none;
            color: inherit;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(45deg, #e2efe2, #d4d7f2);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('/api/placeholder/1600/900') center/cover no-repeat;
            opacity: 0.2;
            z-index: 1;
        }

        .hero-content {
            text-align: center;
            z-index: 2;
        }

        h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            color: #333;
        }

        .tagline {
            font-size: 1.5rem;
            color: #5c5c5c;
        }

        .cta-button {
            display: inline-block;
            margin-top: 2rem;
            padding: 1rem 2rem;
            background-color: #556b2f;
            color: #fff;
            font-weight: bold;
            border-radius: 25px;
            transition: background-color 0.3s, transform 0.3s;
        }

        .cta-button:hover {
            background-color: #6b8f42;
            transform: translateY(-3px);
        }

        /* Projects Section */
        .projects {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 4rem 2rem;
            background-color: #f8f8f8;
        }

        .project-card {
            width: 320px;
            margin: 1rem;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 6px 12px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
        }

        .project-image {
            width: 100%;
            height: 220px;
            object-fit: cover;
        }

        .project-info {
            padding: 1.2rem;
        }

        .project-title {
            font-size: 1.4rem;
            margin-bottom: 0.7rem;
            color: #333;
        }

        .project-description {
            font-size: 1rem;
            color: #777;
        }

        /* Footer Section */
        .footer {
            padding: 2rem 1rem;
            background-color: #333;
            color: #fff;
            text-align: center;
        }

        .footer a {
            color: #fff;
            margin: 0 10px;
            font-size: 1.2rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 3rem;
            }

            .project-card {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Your Name</h1>
            <p class="tagline">Innovative Architectural Designs</p>
            <a href="#projects" class="cta-button">View Projects</a>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="project-card">
            <img src="/api/placeholder/320/220" alt="Project 1" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Modern Residence</h3>
                <p class="project-description">A sleek, minimalist home designed for urban living.</p>
            </div>
        </div>
        <div class="project-card">
            <img src="/api/placeholder/320/220" alt="Project 2" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Sustainable Office Complex</h3>
                <p class="project-description">An eco-friendly workspace that harmonizes with nature.</p>
            </div>
        </div>
        <div class="project-card">
            <img src="/api/placeholder/320/220" alt="Project 3" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Cultural Center</h3>
                <p class="project-description">A dynamic space celebrating arts and community interaction.</p>
            </div>
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
