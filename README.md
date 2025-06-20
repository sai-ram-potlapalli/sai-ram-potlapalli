<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sai Ram Potlapalli - Data Scientist & ML Engineer</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Animated Background */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }

        .floating-shape {
            position: absolute;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(180deg); }
        }

        /* Header */
        .header {
            text-align: center;
            padding: 60px 0;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            margin-bottom: 40px;
            border-radius: 20px;
            margin-top: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .header:hover {
            transform: translateY(-5px);
        }

        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 60px;
            color: white;
            animation: pulse 2s infinite;
            padding: 5px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .profile-img img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid rgba(255, 255, 255, 0.3);
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .header h1 {
            font-size: 3.5rem;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            animation: slideInDown 1s ease-out;
        }

        .header .subtitle {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 300;
            animation: slideInUp 1s ease-out;
        }

        @keyframes slideInDown {
            from { opacity: 0; transform: translateY(-50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideInUp {
            from { opacity: 0; transform: translateY(50px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Contact Section */
        .contact-section {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .contact-card:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
            background: rgba(255, 255, 255, 0.2);
        }

        .contact-card i {
            font-size: 2rem;
            margin-bottom: 10px;
            color: #4ecdc4;
        }

        .contact-card a {
            color: white;
            text-decoration: none;
            font-weight: 500;
        }

        /* Skills Section */
        .skills-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            margin: 40px 0;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }

        .skills-section h2 {
            color: white;
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.1);
            padding: 25px;
            border-radius: 15px;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .skill-category:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.2);
        }

        .skill-category h3 {
            color: #4ecdc4;
            margin-bottom: 15px;
            font-size: 1.3rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill-tag {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            transition: transform 0.2s ease;
        }

        .skill-tag:hover {
            transform: scale(1.1);
        }

        /* Projects Section */
        .projects-section {
            margin: 40px 0;
        }

        .projects-section h2 {
            color: white;
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 20px;
            margin-bottom: 30px;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.2);
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s;
        }

        .project-card:hover::before {
            left: 100%;
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
        }

        .project-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }

        .project-header i {
            font-size: 2rem;
            margin-right: 15px;
            color: #4ecdc4;
        }

        .project-header h3 {
            color: white;
            font-size: 1.5rem;
        }

        .project-description {
            color: rgba(255, 255, 255, 0.9);
            font-style: italic;
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .project-details {
            color: rgba(255, 255, 255, 0.8);
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .project-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .tool-tag {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.9rem;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            color: white;
            padding: 12px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .project-link i {
            margin-right: 8px;
        }

        /* Currently Working Section */
        .current-work {
            background: linear-gradient(135deg, rgba(255, 107, 107, 0.2), rgba(78, 205, 196, 0.2));
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            margin: 40px 0;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .current-work h2 {
            color: white;
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .current-work ul {
            list-style: none;
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.2rem;
            line-height: 1.8;
        }

        .current-work li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 30px;
        }

        .current-work li::before {
            content: '🚀';
            position: absolute;
            left: 0;
            top: 0;
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 0;
            color: rgba(255, 255, 255, 0.8);
            font-size: 1.5rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .contact-section {
                flex-direction: column;
                align-items: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Interactive Elements */
        .interactive-btn {
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            border: none;
            color: white;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            margin: 10px;
        }

        .interactive-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <div class="bg-animation" id="bgAnimation"></div>
    
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="profile-img">
                <i class="fas fa-user-astronaut"></i>
            </div>
            <h1>Hi, I'm Sai Ram Potlapalli</h1>
            <p class="subtitle">Data Scientist | ML Engineer | Analytics Expert</p>
        </div>

        <!-- Contact Section -->
        <div class="contact-section">
            <div class="contact-card" onclick="window.open('mailto:potlpallisairam@gmail.com')">
                <i class="fas fa-envelope"></i>
                <div>
                    <strong>Email</strong><br>
                    <a href="mailto:potlpallisairam@gmail.com">potlpallisairam@gmail.com</a>
                </div>
            </div>
            <div class="contact-card" onclick="window.open('https://linkedin.com/in/sai-ram-potlapalli', '_blank')">
                <i class="fab fa-linkedin"></i>
                <div>
                    <strong>LinkedIn</strong><br>
                    <a href="https://linkedin.com/in/sai-ram-potlapalli" target="_blank">Connect with me</a>
                </div>
            </div>
            <div class="contact-card" onclick="window.open('https://public.tableau.com/app/profile/sai.ram.potlapalli', '_blank')">
                <i class="fas fa-chart-bar"></i>
                <div>
                    <strong>Tableau</strong><br>
                    <a href="https://public.tableau.com/app/profile/sai.ram.potlapalli" target="_blank">View Visualizations</a>
                </div>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="skills-section">
            <h2><i class="fas fa-tools"></i> Skills & Technologies</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3><i class="fab fa-python"></i> Programming</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">SQL</span>
                        <span class="skill-tag">C++</span>
                        <span class="skill-tag">Shell Scripting</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-brain"></i> Machine Learning</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">NumPy</span>
                        <span class="skill-tag">Pandas</span>
                        <span class="skill-tag">Scikit-learn</span>
                        <span class="skill-tag">Statsmodels</span>
                        <span class="skill-tag">SciPy</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-chart-line"></i> Visualization</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Matplotlib</span>
                        <span class="skill-tag">Seaborn</span>
                        <span class="skill-tag">Tableau</span>
                    </div>
                </div>
                <div class="skill-category">
                    <h3><i class="fas fa-database"></i> Databases & Tools</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">PostgreSQL</span>
                        <span class="skill-tag">Oracle</span>
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">Snowflake</span>
                        <span class="skill-tag">GitHub</span>
                        <span class="skill-tag">JIRA</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Projects Section -->
        <div class="projects-section">
            <h2><i class="fas fa-rocket"></i> Featured Projects</h2>
            
            <div class="project-card">
                <div class="project-header">
                    <i class="fas fa-heart"></i>
                    <h3>DonorsChoose Project Approval Prediction</h3>
                </div>
                <p class="project-description">Used NLP and ML to streamline project proposal approval for DonorsChoose.org</p>
                <div class="project-details">
                    <p>• Built a predictive pipeline to identify classroom project approval likelihood based on metadata and essay content</p>
                    <p>• Performed EDA, hypothesis testing, and trained models on structured and unstructured data</p>
                    <p>• Achieved high accuracy in predicting project approval outcomes</p>
                </div>
                <div class="project-tools">
                    <span class="tool-tag">Python</span>
                    <span class="tool-tag">Scikit-learn</span>
                    <span class="tool-tag">Pandas</span>
                    <span class="tool-tag">Seaborn</span>
                    <span class="tool-tag">NLP</span>
                </div>
                <a href="https://github.com/sai-ram-potlapalli/Data-science-Donor-Choose" target="_blank" class="project-link">
                    <i class="fab fa-github"></i>
                    View on GitHub
                </a>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <i class="fas fa-ticket-alt"></i>
                    <h3>Customer Support Ticket Classification</h3>
                </div>
                <p class="project-description">Optimized ticket handling for retail helpdesk using NLP-based classifiers</p>
                <div class="project-details">
                    <p>• Built an auto-tagging and routing model using issue descriptions</p>
                    <p>• Created KPI dashboards to track performance improvements</p>
                    <p>• Reduced manual ticket routing time by 75%</p>
                </div>
                <div class="project-tools">
                    <span class="tool-tag">Python</span>
                    <span class="tool-tag">TfidfVectorizer</span>
                    <span class="tool-tag">Tableau</span>
                    <span class="tool-tag">Scikit-learn</span>
                    <span class="tool-tag">NLP</span>
                </div>
                <a href="https://github.com/sai-ram-potlapalli/customer-support-nlp" target="_blank" class="project-link">
                    <i class="fab fa-github"></i>
                    View on GitHub
                </a>
            </div>
        </div>

        <!-- Currently Working Section -->
        <div class="current-work">
            <h2><i class="fas fa-code"></i> Currently Working On</h2>
            <ul>
                <li>End-to-end ML pipelines and real-world analytics projects</li>
                <li>Enhancing model deployment skills and contributing to open-source</li>
            </ul>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>Thanks for visiting! ⭐</p>
            <p>Let's build something amazing together!</p>
        </div>
    </div>

    <script>
        // Create floating background shapes
        function createFloatingShapes() {
            const bgAnimation = document.getElementById('bgAnimation');
            
            for (let i = 0; i < 15; i++) {
                const shape = document.createElement('div');
                shape.className = 'floating-shape';
                
                const size = Math.random() * 100 + 50;
                shape.style.width = size + 'px';
                shape.style.height = size + 'px';
                shape.style.left = Math.random() * 100 + '%';
                shape.style.top = Math.random() * 100 + '%';
                shape.style.animationDelay = Math.random() * 6 + 's';
                shape.style.animationDuration = (Math.random() * 3 + 4) + 's';
                
                bgAnimation.appendChild(shape);
            }
        }

        // Smooth scrolling for internal links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Add scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe all project cards and skill categories
        document.querySelectorAll('.project-card, .skill-category').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'all 0.6s ease-out';
            observer.observe(el);
        });

        // Initialize animations
        document.addEventListener('DOMContentLoaded', () => {
            createFloatingShapes();
        });

        // Add typing effect to subtitle
        function typeWriter(element, text, speed = 100) {
            let i = 0;
            element.innerHTML = '';
            
            function type() {
                if (i < text.length) {
                    element.innerHTML += text.charAt(i);
                    i++;
                    setTimeout(type, speed);
                }
            }
            type();
        }

        // Start typing effect after page load
        setTimeout(() => {
            const subtitle = document.querySelector('.subtitle');
            const originalText = subtitle.textContent;
            typeWriter(subtitle, originalText, 100);
        }, 1500);
    </script>
</body>
</html>

