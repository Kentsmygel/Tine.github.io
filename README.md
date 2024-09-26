<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name - Architecture Portfolio</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            scroll-behavior: smooth;
        }
        .hero {
            height: 100vh;
            background: linear-gradient(45deg, #f3f3f3, #e1e1e1);
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
            color: #666;
        }
        .cta-button {
            display: inline-block;
            margin-top: 2rem;
            padding: 1rem 2rem;
            background-color: #333;
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        .cta-button:hover {
            background-color: #555;
        }
        .projects {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 4rem 2rem;
        }
        .project-card {
            width: 300px;
            margin: 1rem;
            background-color: #fff;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }
        .project-card:hover {
            transform: translateY(-10px);
        }
        .project-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .project-info {
            padding: 1rem;
        }
        .project-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }
        .project-description {
            font-size: 0.9rem;
            color: #666;
        }
    </style>
</head>
<body>
    <section class="hero">
        <div class="hero-content">
            <h1>Your Name</h1>
            <p class="tagline">Innovative Architectural Designs</p>
            <a href="#projects" class="cta-button">View Projects</a>
        </div>
    </section>

    <section id="projects" class="projects">
        <div class="project-card">
            <img src="/api/placeholder/300/200" alt="Project 1" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Modern Residence</h3>
                <p class="project-description">A sleek, minimalist home designed for urban living.</p>
            </div>
        </div>
        <div class="project-card">
            <img src="/api/placeholder/300/200" alt="Project 2" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Sustainable Office Complex</h3>
                <p class="project-description">An eco-friendly workspace that harmonizes with nature.</p>
            </div>
        </div>
        <div class="project-card">
            <img src="/api/placeholder/300/200" alt="Project 3" class="project-image">
            <div class="project-info">
                <h3 class="project-title">Cultural Center</h3>
                <p class="project-description">A dynamic space celebrating arts and community interaction.</p>
            </div>
        </div>
    </section>
</body>
</html>
