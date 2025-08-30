<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tufail Abbas - MERN Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #2c3e50;
            --secondary: #4ca1af;
            --accent: #3498db;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #27ae60;
            --warning: #e67e22;
            --danger: #e74c3c;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 60px 20px;
            text-align: center;
            border-radius: 10px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 60%);
            transform: rotate(30deg);
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid rgba(255, 255, 255, 0.3);
            margin: 0 auto 20px;
            background: linear-gradient(45deg, #2c3e50, #4ca1af);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            color: white;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .subtitle {
            font-size: 1.5rem;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        .tagline {
            font-style: italic;
            margin-bottom: 20px;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-item {
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 30px;
            backdrop-filter: blur(5px);
        }
        
        .main-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }
        
        .card {
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 25px;
            transition: transform 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }
        
        h2 {
            color: var(--primary);
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--secondary);
            display: flex;
            align-items: center;
        }
        
        h2 i {
            margin-right: 10px;
            color: var(--secondary);
        }
        
        h3 {
            color: var(--accent);
            margin: 15px 0 10px;
        }
        
        ul, ol {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        li {
            margin-bottom: 8px;
        }
        
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 15px;
        }
        
        .skill-item {
            background: var(--light);
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            background: var(--secondary);
            color: white;
            transform: scale(1.05);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-link {
            display: inline-block;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            text-align: center;
            line-height: 50px;
            font-size: 20px;
            transition: all 0.3s ease;
        }
        
        .social-link:hover {
            transform: translateY(-3px);
            background: var(--secondary);
        }
        
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
        }
        
        .project-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
        }
        
        .project-img {
            height: 160px;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 40px;
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-desc {
            color: #666;
            margin-bottom: 15px;
            font-size: 0.9rem;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
            margin-bottom: 15px;
        }
        
        .tech-tag {
            background: var(--light);
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-link {
            display: inline-block;
            padding: 8px 15px;
            background: var(--primary);
            color: white;
            border-radius: 5px;
            text-decoration: none;
            font-size: 0.9rem;
            transition: background 0.3s;
        }
        
        .project-link:hover {
            background: var(--secondary);
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--light);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            color: var(--primary);
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #7f8c8d;
            border-top: 1px solid #ddd;
        }
        
        @media (max-width: 768px) {
            .main-content {
                grid-template-columns: 1fr;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .skills-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="profile-img">
                <i class="fas fa-user"></i>
            </div>
            <h1>Tufail Abbas</h1>
            <p class="subtitle">MERN Stack Developer</p>
            <p class="tagline">A passionate developer from Pakistan crafting digital solutions</p>
            
            <div class="stats">
                <div class="stat-item">
                    <i class="fas fa-eye"></i> <span id="profile-views">0</span> Profile Views
                </div>
                <div class="stat-item">
                    <i class="fas fa-code-branch"></i> <span id="repos">0</span> Repositories
                </div>
            </div>
        </header>
        
        <div class="main-content">
            <div class="content-left">
                <div class="card">
                    <h2><i class="fas fa-user"></i> About Me</h2>
                    <p>Hello! I'm Tufail Abbas, a passionate MERN Stack Developer with expertise in building modern web applications. I enjoy turning complex problems into simple, beautiful and intuitive solutions.</p>
                    <p>When I'm not coding, you can find me exploring new technologies, contributing to open source projects, or enjoying a good book.</p>
                    
                    <div class="social-links">
                        <a href="https://www.linkedin.com/in/tufail-abbas-bb9b83299/" class="social-link" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://www.facebook.com/tufail.abbassaltorovi" class="social-link" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://github.com/tufail206" class="social-link" target="_blank">
                            <i class="fab fa-github"></i>
                        </a>
                        <a href="mailto:tufail206abbas@gmail.com" class="social-link">
                            <i class="fas fa-envelope"></i>
                        </a>
                    </div>
                </div>
                
                <div class="card">
                    <h2><i class="fas fa-briefcase"></i> Experience</h2>
                    
                    <h3>MERN Stack Developer</h3>
                    <p><strong>DigiSync</strong> | 2022 - Present</p>
                    <ul>
                        <li>Developed and maintained web applications using MongoDB, Express.js, React.js, and Node.js</li>
                        <li>Implemented responsive UI components with modern CSS frameworks</li>
                        <li>Collaborated with cross-functional teams to define, design, and ship new features</li>
                    </ul>
                    
                    <h3>Frontend Developer</h3>
                    <p><strong>Freelance</strong> | 2020 - 2022</p>
                    <ul>
                        <li>Created responsive websites using HTML5, CSS3, JavaScript and React</li>
                        <li>Worked with clients to understand requirements and deliver tailored solutions</li>
                        <li>Optimized web applications for maximum speed and scalability</li>
                    </ul>
                </div>
                
                <div class="card">
                    <h2><i class="fas fa-graduation-cap"></i> Education</h2>
                    
                    <h3>Bachelor's in Computer Science</h3>
                    <p><strong>University of Pakistan</strong> | 2018 - 2022</p>
                    <p>Focus on Software Engineering and Web Technologies</p>
                </div>
            </div>
            
            <div class="content-right">
                <div class="card">
                    <h2><i class="fas fa-code"></i> Skills & Technologies</h2>
                    
                    <div class="skills-grid">
                        <div class="skill-item">JavaScript</div>
                        <div class="skill-item">React</div>
                        <div class="skill-item">Node.js</div>
                        <div class="skill-item">Express</div>
                        <div class="skill-item">MongoDB</div>
                        <div class="skill-item">HTML5</div>
                        <div class="skill-item">CSS3</div>
                        <div class="skill-item">Next.js</div>
                        <div class="skill-item">TypeScript</div>
                        <div class="skill-item">Python</div>
                        <div class="skill-item">Git</div>
                        <div class="skill-item">Redux</div>
                        <div class="skill-item">Tailwind</div>
                        <div class="skill-item">Bootstrap</div>
                        <div class="skill-item">REST APIs</div>
                        <div class="skill-item">Postman</div>
                    </div>
                </div>
                
                <div class="card">
                    <h2><i class="fas fa-project-diagram"></i> Projects</h2>
                    
                    <div class="project-grid">
                        <div class="project-card">
                            <div class="project-img">
                                <i class="fas fa-sync-alt"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">DigiSync</h3>
                                <p class="project-desc">A digital synchronization platform for seamless workflow management</p>
                                <div class="project-tech">
                                    <span class="tech-tag">React</span>
                                    <span class="tech-tag">Node.js</span>
                                    <span class="tech-tag">MongoDB</span>
                                </div>
                                <a href="https://github.com/digitalpineskd" class="project-link">View Project</a>
                            </div>
                        </div>
                        
                        <div class="project-card">
                            <div class="project-img">
                                <i class="fas fa-shopping-cart"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">E-Commerce Platform</h3>
                                <p class="project-desc">Full-featured online shopping platform with payment integration</p>
                                <div class="project-tech">
                                    <span class="tech-tag">MERN</span>
                                    <span class="tech-tag">Stripe</span>
                                    <span class="tech-tag">JWT</span>
                                </div>
                                <a href="#" class="project-link">View Project</a>
                            </div>
                        </div>
                        
                        <div class="project-card">
                            <div class="project-img">
                                <i class="fas fa-tasks"></i>
                            </div>
                            <div class="project-content">
                                <h3 class="project-title">Task Management App</h3>
                                <p class="project-desc">Productivity application for managing tasks and projects</p>
                                <div class="project-tech">
                                    <span class="tech-tag">React</span>
                                    <span class="tech-tag">Redux</span>
                                    <span class="tech-tag">Firebase</span>
                                </div>
                                <a href="#" class="project-link">View Project</a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="card">
                    <h2><i class="fas fa-envelope"></i> Contact</h2>
                    
                    <div class="contact-info">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h3>Email</h3>
                                <p>tufail206abbas@gmail.com</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h3>Location</h3>
                                <p>Pakistan</p>
                            </div>
                        </div>
                        
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-calendar-alt"></i>
                            </div>
                            <div>
                                <h3>Availability</h3>
                                <p>Open for new opportunities</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>© 2023 Tufail Abbas. All rights reserved.</p>
            <p>Made with <i class="fas fa-heart" style="color: #e74c3c;"></i> and <i class="fas fa-code" style="color: #3498db;"></i></p>
        </footer>
    </div>

    <script>
        // Animate stats counting
        function animateValue(id, start, end, duration) {
            let obj = document.getElementById(id);
            let range = end - start;
            let current = start;
            let increment = end > start ? 1 : -1;
            let stepTime = Math.abs(Math.floor(duration / range));
            let timer = setInterval(function() {
                current += increment;
                obj.textContent = current;
                if (current == end) {
                    clearInterval(timer);
                }
            }, stepTime);
        }
        
        // Start animations when page loads
        document.addEventListener('DOMContentLoaded', function() {
            animateValue('profile-views', 0, 1286, 2000);
            animateValue('repos', 0, 24, 1500);
        });
    </script>
</body>
</html>
