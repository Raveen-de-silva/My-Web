# My-Web
My Personal web site
!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raveen De Silva | Data Analyst & Systems Thinker</title>
    <link href="https://fonts.googleapis.com/css2?family=Crimson+Pro:wght@400;600;700&family=Work+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a4d2e;
            --secondary: #2d6a4f;
            --accent: #d4a574;
            --dark: #0d1b2a;
            --light: #faf9f6;
            --gray: #4a5759;
            --border: #e0ddd4;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Work Sans', sans-serif;
            color: var(--dark);
            background: var(--light);
            line-height: 1.7;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(250, 249, 246, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav.scrolled {
            box-shadow: 0 2px 20px rgba(0,0,0,0.08);
        }

        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav .logo {
            font-family: 'Crimson Pro', serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        nav ul {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        nav a {
            color: var(--gray);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.3s ease;
            position: relative;
        }

        nav a:hover {
            color: var(--primary);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 8rem 2rem 4rem;
            background: linear-gradient(135deg, #faf9f6 0%, #f0ece3 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 50%;
            height: 100%;
            background: radial-gradient(circle at top right, rgba(212, 165, 116, 0.1), transparent 70%);
            pointer-events: none;
        }

        .hero .container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1.2fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-content h1 {
            font-family: 'Crimson Pro', serif;
            font-size: 4rem;
            font-weight: 700;
            color: var(--primary);
            line-height: 1.1;
            margin-bottom: 1rem;
            animation: fadeInUp 0.8s ease forwards;
            opacity: 0;
        }

        .hero-content .headline {
            font-size: 1.3rem;
            color: var(--secondary);
            font-weight: 600;
            margin-bottom: 1.5rem;
            animation: fadeInUp 0.8s ease 0.2s forwards;
            opacity: 0;
        }

        .hero-content .summary {
            font-size: 1.15rem;
            color: var(--gray);
            line-height: 1.8;
            margin-bottom: 2.5rem;
            animation: fadeInUp 0.8s ease 0.4s forwards;
            opacity: 0;
        }

        .hero-links {
            display: flex;
            gap: 1.5rem;
            flex-wrap: wrap;
            animation: fadeInUp 0.8s ease 0.6s forwards;
            opacity: 0;
        }

        .hero-links a {
            padding: 0.9rem 2rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            box-shadow: 0 4px 15px rgba(26, 77, 46, 0.2);
        }

        .btn-primary:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(26, 77, 46, 0.3);
        }

        .btn-secondary {
            background: transparent;
            color: var(--primary);
            border: 2px solid var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: white;
        }

        .hero-photo {
            position: relative;
            animation: fadeIn 1s ease 0.3s forwards;
            opacity: 0;
        }

        .photo-wrapper {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
        }

        .photo-wrapper::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            width: 120px;
            height: 120px;
            background: var(--accent);
            border-radius: 12px;
            z-index: -1;
        }

        .hero-photo img {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 12px;
        }

        /* Section Styles */
        section {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        section h2 {
            font-family: 'Crimson Pro', serif;
            font-size: 3rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
        }

        section h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--accent);
        }

        /* About Section */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 2rem;
        }

        .about-card {
            background: white;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
            border-left: 4px solid var(--accent);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .about-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 30px rgba(0,0,0,0.1);
        }

        .about-card h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.6rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .about-card p {
            color: var(--gray);
            line-height: 1.8;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 2.5rem;
            margin-top: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(0,0,0,0.12);
        }

        .project-header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem;
        }

        .project-type {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            opacity: 0.9;
            margin-bottom: 0.5rem;
        }

        .project-header h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .project-content {
            padding: 2rem;
        }

        .project-section {
            margin-bottom: 1.5rem;
        }

        .project-section h4 {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: var(--accent);
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .project-section p {
            color: var(--gray);
            line-height: 1.7;
        }

        .project-tools {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1.5rem;
            padding-top: 1.5rem;
            border-top: 1px solid var(--border);
        }

        .tool-tag {
            background: var(--light);
            color: var(--primary);
            padding: 0.4rem 1rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
            border: 1px solid var(--border);
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 2rem;
        }

        .skill-category {
            background: white;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
        }

        .skill-category h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.6rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .skill-category h3::before {
            content: '';
            width: 40px;
            height: 3px;
            background: var(--accent);
        }

        .skill-list {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 0.8rem;
        }

        .skill-item {
            color: var(--gray);
            padding: 0.6rem 0;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .skill-item::before {
            content: '▪';
            color: var(--accent);
            font-size: 1.2rem;
        }

        /* Experience Section */
        .experience-timeline {
            margin-top: 2rem;
            position: relative;
            padding-left: 3rem;
        }

        .experience-timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            bottom: 0;
            width: 3px;
            background: var(--border);
        }

        .experience-item {
            position: relative;
            margin-bottom: 3rem;
            background: white;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
        }

        .experience-item::before {
            content: '';
            position: absolute;
            left: -3.6rem;
            top: 2rem;
            width: 15px;
            height: 15px;
            background: var(--accent);
            border-radius: 50%;
            border: 3px solid var(--light);
        }

        .experience-item h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.6rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .experience-meta {
            color: var(--accent);
            font-size: 0.95rem;
            margin-bottom: 1.5rem;
            font-weight: 500;
        }

        .experience-impact {
            background: var(--light);
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 3px solid var(--accent);
            margin-top: 1rem;
        }

        .experience-impact h4 {
            color: var(--primary);
            margin-bottom: 0.8rem;
            font-size: 1.1rem;
        }

        /* Blog Section */
        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .blog-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .blog-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 30px rgba(0,0,0,0.12);
        }

        .blog-category {
            background: var(--accent);
            color: white;
            padding: 0.5rem 1.5rem;
            font-size: 0.85rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .blog-content {
            padding: 2rem;
        }

        .blog-content h3 {
            font-family: 'Crimson Pro', serif;
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .blog-excerpt {
            color: var(--gray);
            line-height: 1.7;
            margin-bottom: 1rem;
        }

        .read-more {
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }

        .read-more:hover {
            color: var(--primary);
        }

        /* Contact Section */
        .contact-content {
            background: white;
            padding: 3rem;
            border-radius: 12px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.06);
            max-width: 800px;
            margin: 2rem auto;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .contact-method {
            text-align: center;
            padding: 2rem;
            background: var(--light);
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .contact-method:hover {
            transform: translateY(-5px);
        }

        .contact-method h3 {
            font-size: 1.2rem;
            color: var(--primary);
            margin-bottom: 0.8rem;
        }

        .contact-method a {
            color: var(--secondary);
            text-decoration: none;
            font-weight: 500;
        }

        .contact-method a:hover {
            color: var(--accent);
        }

        .contact-form {
            display: grid;
            gap: 1.5rem;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .form-group input,
        .form-group textarea {
            padding: 1rem;
            border: 2px solid var(--border);
            border-radius: 6px;
            font-family: 'Work Sans', sans-serif;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 150px;
        }

        .submit-btn {
            background: var(--primary);
            color: white;
            padding: 1rem 3rem;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            justify-self: start;
        }

        .submit-btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(26, 77, 46, 0.3);
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 4rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        /* Responsive */
        @media (max-width: 968px) {
            .hero .container {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-content h1 {
                font-size: 3rem;
            }

            .hero-links {
                justify-content: center;
            }

            .about-grid,
            .skills-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            nav ul {
                gap: 1.5rem;
            }

            section h2 {
                font-size: 2.5rem;
            }
        }

        @media (max-width: 640px) {
            nav .container {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .contact-grid {
                grid-template-columns: 1fr;
            }

            .skill-list {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="container">
            <a href="#home" class="logo">RDS</a>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#blog">Insights</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Raveen De Silva</h1>
                <p class="headline">Data Analyst | Supply Chain & Healthcare Systems | Future AI Consultant</p>
                <p class="summary">I analyze operational processes and transform them into measurable improvements using data, statistics, and systems thinking.</p>
                <div class="hero-links">
                    <a href="#contact" class="btn-primary">Get in Touch</a>
                    <a href="#" class="btn-secondary" onclick="downloadCV(event)">Download CV</a>
                    <a href="https://linkedin.com/in/raveendesilva" class="btn-secondary" target="_blank">LinkedIn</a>
                </div>
            </div>
            <div class="hero-photo">
                <div class="photo-wrapper">
                    <!-- Placeholder for professional photo -->
                    <img src="https://via.placeholder.com/500x600/2d6a4f/ffffff?text=Your+Photo+Here" alt="Raveen De Silva">
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <div class="about-grid">
            <div class="about-card">
                <h3>My Journey</h3>
                <p>From a foundation in science to navigating complex supply chain operations, my career has been driven by curiosity about systems and their inefficiencies. Working in industry exposed me to the gap between data availability and actionable insights. This led me to analytics—not just as a technical skill, but as a lens for understanding and improving operational reality.</p>
            </div>
            <div class="about-card">
                <h3>Analytical Mindset</h3>
                <p>I approach problems systematically: define the question, examine the data, test hypotheses, and measure impact. I'm fascinated by the intersection of statistics and business logic—where numbers tell stories about processes, behaviors, and opportunities. My strength lies in translating complex analysis into clear, decision-ready insights.</p>
            </div>
            <div class="about-card">
                <h3>Why Healthcare & AI</h3>
                <p>Healthcare systems represent one of the most data-rich yet operationally complex domains. The potential for AI to optimize patient flow, resource allocation, and clinical outcomes is immense but underutilized. I'm drawn to this challenge—applying analytical rigor to improve systems that directly impact human wellbeing.</p>
            </div>
            <div class="about-card">
                <h3>Long-term Vision</h3>
                <p>My goal is to become a consultant specializing in operational analytics and AI implementation for healthcare and industrial systems. I'm pursuing advanced studies to deepen my technical expertise while building a portfolio that demonstrates real-world problem-solving. I want to be the bridge between data science capability and organizational transformation.</p>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>Projects Portfolio</h2>
        <div class="projects-grid">
            <!-- Data Analysis Project -->
            <div class="project-card">
                <div class="project-header">
                    <div class="project-type">Data Analysis</div>
                    <h3>Demand Forecasting & Inventory Optimization</h3>
                </div>
                <div class="project-content">
                    <div class="project-section">
                        <h4>Problem</h4>
                        <p>A small manufacturing company faced recurring stock-outs and overstock situations, leading to lost sales and tied-up capital. Historical ordering was based on intuition rather than data.</p>
                    </div>
                    <div class="project-section">
                        <h4>Data & Method</h4>
                        <p>Analyzed 2 years of sales transactions (15,000+ records), seasonal patterns, and supplier lead times. Applied ARIMA time series modeling and safety stock calculations based on demand variability.</p>
                    </div>
                    <div class="project-section">
                        <h4>Insight</h4>
                        <p>Discovered that 80% of stockouts occurred in just 12 SKUs driven by seasonal spikes. Demand variability was 3x higher than management estimated, requiring different safety stock strategies per product category.</p>
                    </div>
                    <div class="project-section">
                        <h4>Business Impact</h4>
                        <p>Recommended reorder points reduced stockouts by 65% while decreasing average inventory holding by 23%. Projected annual savings: $180,000 in carrying costs and lost sales.</p>
                    </div>
                    <div class="project-tools">
                        <span class="tool-tag">Python</span>
                        <span class="tool-tag">Pandas</span>
                        <span class="tool-tag">Statsmodels</span>
                        <span class="tool-tag">Time Series Analysis</span>
                    </div>
                </div>
            </div>

            <!-- Business/Systems Analysis Project -->
            <div class="project-card">
                <div class="project-header">
                    <div class="project-type">Systems Analysis</div>
                    <h3>ERP Workflow Optimization Study</h3>
                </div>
                <div class="project-content">
                    <div class="project-section">
                        <h4>Problem</h4>
                        <p>Purchase requisition approval process in ERP system took average 8 days, delaying procurement and frustrating users. Management wanted to understand bottlenecks without blaming individuals.</p>
                    </div>
                    <div class="project-section">
                        <h4>Data & Method</h4>
                        <p>Extracted workflow logs from ERP database (3,200 requisitions over 6 months). Created process mining analysis using UML activity diagrams and mapped approval paths with bottleneck identification.</p>
                    </div>
                    <div class="project-section">
                        <h4>Insight</h4>
                        <p>72% of delays occurred at a single approval stage where managers were CCed but not required approvers—they thought action was needed. Parallel approval paths were possible but not configured.</p>
                    </div>
                    <div class="project-section">
                        <h4>Business Impact</h4>
                        <p>Redesigned workflow reduced approval time to 2.3 days on average. Recommended system configuration changes and user training. Improved procurement cycle time by 58%.</p>
                    </div>
                    <div class="project-tools">
                        <span class="tool-tag">SQL</span>
                        <span class="tool-tag">Process Mining</span>
                        <span class="tool-tag">UML</span>
                        <span class="tool-tag">ERD Modeling</span>
                    </div>
                </div>
            </div>

            <!-- Visualization Project -->
            <div class="project-card">
                <div class="project-header">
                    <div class="project-type">Data Visualization</div>
                    <h3>Supply Chain KPI Dashboard</h3>
                </div>
                <div class="project-content">
                    <div class="project-section">
                        <h4>Problem</h4>
                        <p>Operations team tracked 40+ metrics in Excel but couldn't quickly identify performance trends or correlations. Monthly reporting took 3 days to compile manually.</p>
                    </div>
                    <div class="project-section">
                        <h4>Data & Method</h4>
                        <p>Connected Power BI to ERP database, inventory system, and logistics provider APIs. Designed star schema data model with dimension tables for products, suppliers, and time periods.</p>
                    </div>
                    <div class="project-section">
                        <h4>Insight</h4>
                        <p>Interactive dashboard revealed supplier performance correlation with lead time variability. Late deliveries from 3 suppliers caused 89% of production delays. Real-time visibility highlighted issues within 24 hours instead of monthly.</p>
                    </div>
                    <div class="project-section">
                        <h4>Business Impact</h4>
                        <p>Enabled data-driven supplier negotiations. Reporting time reduced from 3 days to 15 minutes. Management could now make weekly operational adjustments instead of monthly reactions.</p>
                    </div>
                    <div class="project-tools">
                        <span class="tool-tag">Power BI</span>
                        <span class="tool-tag">DAX</span>
                        <span class="tool-tag">SQL</span>
                        <span class="tool-tag">Data Modeling</span>
                    </div>
                </div>
            </div>

            <!-- Research-style Project -->
            <div class="project-card">
                <div class="project-header">
                    <div class="project-type">Research Analysis</div>
                    <h3>Hospital Patient Flow Optimization Case Study</h3>
                </div>
                <div class="project-content">
                    <div class="project-section">
                        <h4>Problem</h4>
                        <p>Emergency department experiencing patient overcrowding with average wait times exceeding 4 hours. Hospital wanted evidence-based recommendations for process improvement.</p>
                    </div>
                    <div class="project-section">
                        <h4>Data & Method</h4>
                        <p>Mixed-method analysis: quantitative analysis of 8,000 patient visit records plus qualitative interviews with 12 staff members. Applied queuing theory and simulation modeling to test scenarios.</p>
                    </div>
                    <div class="project-section">
                        <h4>Insight</h4>
                        <p>Bottleneck wasn't staffing levels but resource allocation timing. Peak arrivals (10am-2pm) coincided with scheduled procedures blocking rooms. 35% of "urgent" cases could be redirected to fast-track protocol.</p>
                    </div>
                    <div class="project-section">
                        <h4>Business Impact</h4>
                        <p>Recommended staggered procedure scheduling and fast-track pathway implementation. Simulation predicted 40% reduction in average wait time and 25% improvement in bed utilization without additional staff.</p>
                    </div>
                    <div class="project-tools">
                        <span class="tool-tag">R</span>
                        <span class="tool-tag">Queuing Theory</span>
                        <span class="tool-tag">Simulation</span>
                        <span class="tool-tag">Statistical Analysis</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2>Skills & Expertise</h2>
        <div class="skills-grid">
            <div class="skill-category">
                <h3>Analytical</h3>
                <div class="skill-list">
                    <div class="skill-item">Statistics & Probability</div>
                    <div class="skill-item">Forecasting</div>
                    <div class="skill-item">Hypothesis Testing</div>
                    <div class="skill-item">Regression Analysis</div>
                    <div class="skill-item">Process Modeling</div>
                    <div class="skill-item">Root Cause Analysis</div>
                    <div class="skill-item">Time Series Analysis</div>
                    <div class="skill-item">Optimization</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Technical</h3>
                <div class="skill-list">
                    <div class="skill-item">SQL (Advanced)</div>
                    <div class="skill-item">Python (Pandas, NumPy)</div>
                    <div class="skill-item">R (Statistical Analysis)</div>
                    <div class="skill-item">Power BI</div>
                    <div class="skill-item">Tableau</div>
                    <div class="skill-item">Excel (VBA, Power Query)</div>
                    <div class="skill-item">Git & Version Control</div>
                    <div class="skill-item">Data Warehousing</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Systems</h3>
                <div class="skill-list">
                    <div class="skill-item">ERP Systems</div>
                    <div class="skill-item">Database Design</div>
                    <div class="skill-item">UML Modeling</div>
                    <div class="skill-item">Requirements Analysis</div>
                    <div class="skill-item">Process Mapping</div>
                    <div class="skill-item">Data Architecture</div>
                    <div class="skill-item">Business Intelligence</div>
                    <div class="skill-item">API Integration</div>
                </div>
            </div>

            <div class="skill-category">
                <h3>Domain Knowledge</h3>
                <div class="skill-list">
                    <div class="skill-item">Supply Chain Operations</div>
                    <div class="skill-item">Inventory Management</div>
                    <div class="skill-item">Procurement Processes</div>
                    <div class="skill-item">Healthcare Systems</div>
                    <div class="skill-item">Workflow Analysis</div>
                    <div class="skill-item">Performance Metrics</div>
                    <div class="skill-item">Change Management</div>
                    <div class="skill-item">Stakeholder Engagement</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <h2>Professional Experience</h2>
        <div class="experience-timeline">
            <div class="experience-item">
                <h3>Supply Chain Analyst</h3>
                <div class="experience-meta">ABC Manufacturing Ltd | 2021 - 2023</div>
                <p><strong>Situation:</strong> Company struggled with inventory accuracy below 75% and frequent stockouts causing production delays.</p>
                <div class="experience-impact">
                    <h4>What I Analyzed</h4>
                    <p>Conducted root cause analysis of 2,000+ inventory discrepancies, mapped material flow patterns, and identified systemic data entry gaps in receiving process.</p>
                </div>
                <div class="experience-impact">
                    <h4>Decision Impact</h4>
                    <p>Implemented automated validation checks and redesigned receiving workflow. Inventory accuracy improved to 94% within 4 months. Reduced stockout incidents by 58%, enabling on-time production increase from 82% to 96%.</p>
                </div>
            </div>

            <div class="experience-item">
                <h3>Data Analyst Intern</h3>
                <div class="experience-meta">HealthTech Solutions | 2020 - 2021</div>
                <p><strong>Situation:</strong> Healthcare analytics startup needed to demonstrate ROI of their patient flow optimization software to prospective clients.</p>
                <div class="experience-impact">
                    <h4>What I Analyzed</h4>
                    <p>Analyzed before/after implementation data from 5 pilot hospitals. Built comparative dashboard showing patient wait times, bed utilization, and staff productivity metrics.</p>
                </div>
                <div class="experience-impact">
                    <h4>Decision Impact</h4>
                    <p>Created evidence-based sales materials demonstrating average 32% reduction in patient wait times. Contributed to securing 3 new enterprise contracts worth $850K total annual value.</p>
                </div>
            </div>

            <div class="experience-item">
                <h3>Supply Planning Coordinator</h3>
                <div class="experience-meta">XYZ Distribution | 2018 - 2020</div>
                <p><strong>Situation:</strong> Growing order volumes (40% YoY) overwhelmed manual planning process causing delivery delays and customer complaints.</p>
                <div class="experience-impact">
                    <h4>What I Analyzed</h4>
                    <p>Examined order patterns, supplier lead times, and demand variability across 300+ SKUs. Identified products suitable for automated reordering vs. those requiring manual review.</p>
                </div>
                <div class="experience-impact">
                    <h4>Decision Impact</h4>
                    <p>Implemented ABC analysis-based planning approach with automated reorder points for 70% of SKUs. Reduced planning time by 12 hours/week while improving on-time delivery from 78% to 91%.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Blog Section -->
    <section id="blog">
        <h2>Insights & Writing</h2>
        <div class="blog-grid">
            <div class="blog-card">
                <div class="blog-category">Operations</div>
                <div class="blog-content">
                    <h3>Why Small Businesses Fail at Inventory Planning</h3>
                    <p class="blog-excerpt">Most small manufacturers treat inventory as a necessary evil rather than a strategic asset. The root cause isn't lack of sophistication—it's the absence of basic data discipline. Here's what I've learned from analyzing dozens of struggling supply chains...</p>
                    <a href="#" class="read-more">Read more →</a>
                </div>
            </div>

            <div class="blog-card">
                <div class="blog-category">Healthcare</div>
                <div class="blog-content">
                    <h3>How Data Can Actually Improve Hospital Workflow</h3>
                    <p class="blog-excerpt">Healthcare generates massive amounts of data, yet most hospitals still make operational decisions based on anecdote and intuition. The problem isn't technology—it's translating clinical reality into analyzable structures. My case study on ED patient flow...</p>
                    <a href="#" class="read-more">Read more →</a>
                </div>
            </div>

            <div class="blog-card">
                <div class="blog-category">Analytics</div>
                <div class="blog-content">
                    <h3>Cultural Behavior Hidden in Consumer Demand Data</h3>
                    <p class="blog-excerpt">While analyzing sales patterns for a retail client, I noticed something unexpected: demand spikes weren't just seasonal—they correlated with cultural events barely mentioned in marketing calendars. This revealed a deeper truth about forecasting...</p>
                    <a href="#" class="read-more">Read more →</a>
                </div>
            </div>

            <div class="blog-card">
                <div class="blog-category">AI & Future</div>
                <div class="blog-content">
                    <h3>AI in Operational Decision Making: Promise vs. Reality</h3>
                    <p class="blog-excerpt">Every software vendor promises AI-powered optimization, but most "AI" in operations is just rule-based automation with better marketing. Real AI transformation requires rethinking processes, not just installing tools. Here's what actually works...</p>
                    <a href="#" class="read-more">Read more →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get in Touch</h2>
        <div class="contact-content">
            <div class="contact-grid">
                <div class="contact-method">
                    <h3>Email</h3>
                    <a href="mailto:raveen.desilva@email.com">raveen.desilva@email.com</a>
                </div>
                <div class="contact-method">
                    <h3>LinkedIn</h3>
                    <a href="https://linkedin.com/in/raveendesilva" target="_blank">Connect with me</a>
                </div>
                <div class="contact-method">
                    <h3>CV</h3>
                    <a href="#" onclick="downloadCV(event)">Download PDF</a>
                </div>
            </div>

            <form class="contact-form" onsubmit="handleSubmit(event)">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" name="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" name="message" required></textarea>
                </div>
                <button type="submit" class="submit-btn">Send Message</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 Raveen De Silva. All rights reserved. | Built with purpose, designed with intention.</p>
    </footer>

    <script>
        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                const href = this.getAttribute('href');
                if (href !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(href);
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                }
            });
        });

        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Form submission handler
        function handleSubmit(e) {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            e.target.reset();
        }

        // CV download handler
        function downloadCV(e) {
            e.preventDefault();
            alert('CV download functionality - Connect this to your actual CV file URL');
            // In production, replace with: window.location.href = 'path/to/your/cv.pdf';
        }

        // Intersection Observer for fade-in animations
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

        // Observe project cards and skill categories
        document.querySelectorAll('.project-card, .skill-category, .about-card, .blog-card, .experience-item').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
