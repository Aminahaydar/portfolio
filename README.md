��#   p o r t f o l i o 
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio - Amina Haydar</title>
    <link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

    <style>
        /* General Styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            padding: 0;
            margin: 0;
            list-style: none;
        }

        h1, h3, h5, h6 {
            margin: 0;
        }

        p {
            margin: 10px 0;
        }

        /* Header */
        header {
            background-color: #501248; /* Purple */
            color: white;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 24px;
        }

        header nav {
            display: flex;
            align-items: center;
        }

        header nav ul {
            display: flex;
            gap: 20px;
        }

        header nav a {
            color: white;
            font-size: 18px;
        }
        header nav a:hover{
            color: #820050;
        }

        /* Navbar Toggle Button (for small screens) */
        .menu-toggle {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }

        /* Responsive Navbar Styling */
        @media (max-width: 768px) {
            header nav ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px;
                left: 0;
                width: 100%;
                background-color: #1a0114; /* Purple */
                padding: 0;
            }

            header nav ul.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            header {
                flex-direction: column;
            }
        }

        /* Section Styling */
        section {
            padding: 60px 20px;
            text-align: center;
        }

        /* Home Section */
        #home {
            background-color: #e6e6fa; /* Light Lavender */
            color: #4b0082; /* Indigo */
        }

        #home h1 {
            font-size: 36px;
            margin-bottom: 20px;
        }

        #home p {
            font-size: 18px;
            max-width: 700px;
            margin: 0 auto;
        }

        /* About Us Section */
        .profile {
            text-align: center;
            padding: 40px 20px;
            background-color: #fff;
        }

        .profile figure img {
            border-radius: 50%;
            width: 30%; /* Increased size */
            height: auto;
        }

        @media (max-width: 768px) {
            #about img {
                width: 200px; /* Responsive adjustment */
                height: 200px;
            }
        }

        @media (max-width: 480px) {
            #about img {
                width: 150px; /* Further adjustment for small screens */
                height: 150px;
            }
        }

        /* Skills Section */
        #skills {
            background-color: #f0f0f5; /* Light Gray */
            text-align: center;
            padding: 60px 20px;
        }

        #skills h3 {
            font-size: 32px;
            color: #5d3ebc; /* Purple */
        }

        .skills-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .skill-card {
            background-color: #fff;
            width: 28%;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .skill-card h5 {
            font-size: 22px;
            color: #5d3ebc; /* Purple */
        }

        .skill-card p {
            font-size: 16px;
        }

        
        @media (max-width: 768px) {
            .skill-card {
                width: 45%;
            }
        }

        @media (max-width: 480px) {
            .skill-card {
                width: 100%; /* Full width on small screens */
            }
        }

        /* Projects Section */
        #projects {
            background-color: #f5f5f5; /* Light Gray */
            color: #2f4f4f; /* Dark Slate Gray */
        }
        #projects h3{
            color: black;
            font-size: 2rem;
        }

        .project-grid {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .project-box {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            width: 30%;
            text-align: left;
            transition: transform 0.3s;
        }

        .project-box:hover {
            transform: scale(1.05);
        }

        .project-box img {
            width: 100%;
            height: auto;
        }

        .project-box .project-content {
            padding: 15px;
        }
.project-content h5{
    font-size: 1.5rem;
    color: black;
}
        @media (max-width: 768px) {
            .project-box {
                width: 45%;
            }
        }

        @media (max-width: 480px) {
            .project-box {
                width: 100%;
            }
        }

        /* Contact Us Section */
        #contact {
            background-color: #fffaf0; /* Light Peach */
            color: #483d8b; /* Dark Slate Blue */
        }

        .contact-form {
            max-width: 600px;
            margin: 20px auto;
            text-align: left;
        }

        .contact-form input, .contact-form textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        .contact-form button {
            background-color: #5d3ebc; /* Purple */
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px; /* Bigger text */
            transition: background-color 0.3s;
        }

        .contact-form button:hover {
            background-color: #473a8c; /* Darker Purple on Hover */
        }

        /* Footer */
        footer {
            background-color: #5d3ebc; /* Purple */
            color: white;
            padding: 20px;
            text-align: center;
        }

        footer ul li {
            display: inline-block;
            margin-right: 15px;
        }

        footer ul li a {
            color: white;
            font-size: 24px;
        }
    </style>
</head>

<body>
    <!-- Header with Navigation -->
    <header>
        <h1>Amina Haydar's Portfolio</h1>
        <span class="menu-toggle"><i class="fas fa-bars"></i></span>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home">
        <h1>Welcome to My Portfolio</h1>
        <p>I am Amina Haydar, a Full Stack Developer and Designer with a passion for crafting engaging digital experiences.</p>
    </section>

    <!-- About Us Section -->
    <section id="about" class="profile">
        <figure>
            <img src="image/WhatsApp Image 2024-10-03 at 10.36.58 PM.jpeg" alt="Profile Image">
        </figure>
        <h1>Amina Haydar</h1>
        <br>
        <em>Full Stack Developer & Designer</em>
        <blockquote>"Turning ideas into reality through code and creativity."</blockquote>
        <blockquote>With over 2 years of experience, I aim to create innovative digital experiences for users across the globe.</blockquote>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h3>Skills</h3>
        <br>
        <div class="skills-list">
            <div class="skill-card">
                <h5>HTML</h5>
                <p>Experienced in creating structured and semantic web content.</p>
            </div>
            <div class="skill-card">
                <h5>CSS</h5>
                <p>Proficient in styling and layout for responsive designs.</p>
            </div>
            <div class="skill-card">
                <h5>JavaScript</h5>
                <p>Skilled in building interactive web applications.</p>
            </div>
            <div class="skill-card">
                <h5>React</h5>
                <p>Familiar with building single-page applications with React.</p>
            </div>
            <div class="skill-card">
                <h5>Node.js</h5>
                <p>Experienced in backend development with Node.js.</p>
            </div>
            <div class="skill-card">
                <h5>Laravel</h5>
                <p>Skilled in developing web applications using Laravel framework.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <!-- Projects Section -->
<section id="projects">
    <h3>Projects</h3>
    <br>
    <div class="project-grid">
        <div class="project-box">
            <img src="image/hotel.png" alt="Hotel Management System">
            <div class="project-content">
                <h5>Hotel Management System</h5>
                <p>A comprehensive system to manage hotel bookings, customer details, and services, ensuring a seamless experience for guests.</p>
            </div>
        </div>
        <div class="project-box">
            <img src="image/Screenshot 2024-10-15 145700.png" alt="Event Calendar">
            <div class="project-content">
                <h5>Event Calendar</h5>
                <p>A user-friendly calendar to browse, manage, and RSVP to events, making it easier to stay organized and connected.</p>
            </div>
        </div>
        <div class="project-box">
            <img src="image/Screenshot 2024-10-03 223950.png" alt="Personal Blog">
            <div class="project-content">
                <h5> Blog</h5>
                <p>A blog platform to share thoughts, experiences, and insights on various topics, fostering engagement and community.</p>
            </div>
        </div>
    </div>
</section>


    <!-- Contact Us Section -->
    <section id="contact">
        <h3>Contact Me</h3>
        <form class="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Amina Haydar. All Rights Reserved.</p>
        <ul>
            <li><a href="#"><i class="fab fa-facebook"></i></a></li>
            <li><a href="#"><i class="fab fa-twitter"></i></a></li>
            <li><a href="#"><i class="fab fa-linkedin"></i></a></li>
        </ul>
    </footer>

    <script>
        // Navbar toggle script
        document.querySelector('.menu-toggle').addEventListener('click', function () {
            const navList = document.querySelector('nav ul');
            navList.classList.toggle('active');
        });
    </script>
</body>

</html>

 
 
