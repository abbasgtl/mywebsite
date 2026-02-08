<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IGCSE/As/A Levels | Math Tutoring Classes</title>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- CSS Variables & Reset --- */
        :root {
            --primary-color: #0f172a; /* Deep Navy */
            --accent-color: #ca8a04; /* Gold/Amber for excellence */
            --secondary-color: #334155; /* Slate */
            --bg-light: #f8fafc;
            --text-dark: #1e293b;
            --text-light: #f1f5f9;
            --white: #ffffff;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --radius: 8px;
            --font-main: system-ui, -apple-system, sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-main);
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--bg-light);
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: 0.3s;
        }

        ul {
            list-style: none;
        }

        /* --- Typography --- */
        h1, h2, h3, h4 {
            color: var(--primary-color);
            font-weight: 700;
            line-height: 1.2;
        }

        h1 { font-size: 2.5rem; margin-bottom: 1rem; }
        h2 { font-size: 2rem; margin-bottom: 1rem; position: relative; display: inline-block; }
        h3 { font-size: 1.5rem; margin-bottom: 0.5rem; }
        p { margin-bottom: 1rem; }

        /* --- Layout Utilities --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section {
            padding: 5rem 0;
        }

        .bg-white { background-color: var(--white); }
        .bg-dark { background-color: var(--primary-color); color: var(--text-light); }
        .text-center { text-align: center; }
        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; }
        .grid-3 { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
        .grid-4 { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.5rem; }

        @media (max-width: 768px) {
            .grid-2 { grid-template-columns: 1fr; }
            h1 { font-size: 2rem; }
            h2 { font-size: 1.75rem; }
        }

        /* --- Components --- */
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--accent-color);
            color: var(--white);
            border-radius: var(--radius);
            font-weight: 600;
            border: none;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #a16207;
            transform: translateY(-2px);
        }
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--accent-color);
            color: var(--accent-color);
        }
        .btn-outline:hover {
            background-color: var(--accent-color);
            color: var(--white);
        }

        .card {
            background: var(--white);
            padding: 2rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            height: 100%;
            transition: transform 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
        }

        .section-title-wrapper {
            text-align: center;
            margin-bottom: 3rem;
        }
        .section-title-wrapper h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--accent-color);
            margin: 10px auto 0;
        }

        /* --- Header --- */
        header {
            background: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .logo i { color: var(--accent-color); }
        .nav-links {
            display: flex;
            gap: 20px;
        }
        .nav-links a {
            font-weight: 500;
            color: var(--secondary-color);
        }
        .nav-links a:hover { color: var(--accent-color); }
        .mobile-menu-btn { display: none; font-size: 1.5rem; cursor: pointer; }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .mobile-menu-btn { display: block; }
        }

        /* --- Hero Section --- */
        .hero {
            background: linear-gradient(rgba(15, 23, 42, 0.9), rgba(15, 23, 42, 0.8)), url('https://picsum.photos/seed/mathclass/1920/1080') no-repeat center center/cover;
            color: var(--white);
            padding: 8rem 0 6rem;
            text-align: center;
        }
        .hero h1 { color: var(--white); margin-bottom: 1.5rem; }
        .hero p { font-size: 1.2rem; max-width: 700px; margin: 0 auto 2rem; color: #cbd5e1; }
        .hero-badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }
        .badge {
            background: rgba(255,255,255,0.1);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            border: 1px solid rgba(255,255,255,0.2);
        }

        /* --- Teacher Profile --- */
        .teacher-profile {
            align-items: center;
        }
        .teacher-img {
            width: 100%;
            max-width: 400px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            object-fit: cover;
        }
        .qualification-list li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
        }
        .qualification-list li::before {
            content: '\f00c';
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            color: var(--accent-color);
            position: absolute;
            left: 0;
            top: 2px;
        }

        /* --- Objectives & Standards --- */
        .feature-box {
            text-align: center;
            padding: 2rem;
            border: 1px solid #e2e8f0;
            border-radius: var(--radius);
            transition: 0.3s;
        }
        .feature-box:hover {
            border-color: var(--accent-color);
        }
        .feature-icon {
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        /* --- Syllabus --- */
        .syllabus-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }
        .syllabus-item {
            background: var(--white);
            border-left: 4px solid var(--accent-color);
            padding: 1.5rem;
            box-shadow: var(--shadow);
            border-radius: 0 var(--radius) var(--radius) 0;
        }
        .syllabus-item h4 {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: var(--primary-color);
        }
        .syllabus-list li {
            font-size: 0.95rem;
            margin-bottom: 0.5rem;
            padding-left: 1.2rem;
            position: relative;
        }
        .syllabus-list li::before {
            content: '•';
            color: var(--accent-color);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        /* --- Methodology --- */
        .methodology-steps {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }
        .step {
            text-align: center;
            flex: 1;
            min-width: 150px;
        }
        .step-num {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background: var(--primary-color);
            color: var(--white);
            border-radius: 50%;
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 10px;
        }

        /* --- Prerequisites & Footer --- */
        .prereq-box {
            background: var(--primary-color);
            color: var(--white);
            padding: 3rem;
            border-radius: var(--radius);
            text-align: center;
        }
        footer {
            background: var(--primary-color);
            color: #94a3b8;
            padding: 3rem 0;
            margin-top: 4rem;
        }
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        .footer-col h4 { color: var(--white); margin-bottom: 1.5rem; }
        .footer-col a { display: block; margin-bottom: 0.8rem; }
        .footer-col a:hover { color: var(--accent-color); }
        .contact-highlight {
            color: var(--accent-color);
            font-size: 1.2rem;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="container nav-container">
            <div class="logo">
                <i class="fas fa-square-root-variable"></i> IGCSE(O)/As/A Levels
            </div>
            <nav class="nav-links">
                <a href="#about">About Teacher</a>
                <a href="#overview">Overview</a>
                <a href="#syllabus">Syllabus</a>
                <a href="#methodology">Methodology</a>
                <a href="#contact" class="btn" style="padding: 8px 20px;">Contact Us</a>
            </nav>
            <div class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-badges">
                <span class="badge">8 Month Course</span>
                <span class="badge">Basics to 10th Grade</span>
                <span class="badge">Cambridge & IGCSE</span>
            </div>
            <h1>Revolutionize Your Math Learning Experience</h1>
            <p>Interactive conceptual classes designed to cover the entire spectrum from basic addition to 10th-grade math. Join engaging sessions 5 days a week and build a strong foundation for global success.</p>
            <a href="https://wa.me/918124185476" class="btn">
                <i class="fab fa-whatsapp"></i> Start Learning Now
            </a>
        </div>
    </section>

    <!-- About Teacher -->
    <section id="about" class="section bg-white">
        <div class="container">
            <div class="grid-2 teacher-profile">
                <div>
                    <img src="https://picsum.photos/seed/abbassyed/600/600" alt="Dr. Abbas Ahmed Syed Khaja" class="teacher-img">
                </div>
                <div>
                    <h2>Meet Your Teacher</h2>
                    <h3>Dr. Abbas Ahmed Syed Khaja</h3>
                    <p style="font-size: 1.1rem; color: var(--secondary-color); margin-bottom: 2rem;">18+ Years of Teaching Experience</p>
                    
                    <ul class="qualification-list">
                        <li><strong>B.E</strong> (India)</li>
                        <li><strong>M.E</strong> (India)</li>
                        <li><strong>M.S</strong> (Germany)</li>
                        <li><strong>Ph.D</strong> (IIT Madras, India)</li>
                        <li>Expert in Cambridge, IGCSE, CBSE, ICSE curriculums</li>
                        <li>On-demand classes for 11th & 12th Grade available</li>
                    </ul>
                    
                    <div style="margin-top: 2rem;">
                        <a href="https://wa.me/918124185476" class="contact-highlight">
                            <i class="fab fa-whatsapp"></i> (+91) 81241 85476
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Overview & Objectives -->
    <section id="overview" class="section">
        <div class="container">
            <div class="section-title-wrapper">
                <h2>Overview & Objectives</h2>
                <p>Excelling in IGCSE/AS/A levels for admission in top universities.</p>
            </div>
            
            <div class="grid-3">
                <div class="card">
                    <div class="feature-icon"><i class="fas fa-globe"></i></div>
                    <h4>Global Exam Readiness</h4>
                    <p>Students will be equipped to excel in 10th-grade examinations globally including Cambridge Board (UK), IGCSE, AQA, OCR, ICSE, CBSE, and German Boards.</p>
                </div>
                <div class="card">
                    <div class="feature-icon"><i class="fas fa-university"></i></div>
                    <h4>USA Standardized Tests</h4>
                    <p>Curriculum aligns with SAT and ACT requirements. Additional preparation is provided to enhance performance and achieve high scores in these assessments.</p>
                </div>
                <div class="card">
                    <div class="feature-icon"><i class="fas fa-bullseye"></i></div>
                    <h4>University Pathways</h4>
                    <p>A direct path to top universities like MIT, Oxford, Cambridge, or Stanford by excelling in IGCSE/AS/A levels at the bachelor level.</p>
                </div>
            </div>

            <div class="section-title-wrapper" style="margin-top: 4rem;">
                <h2>Why This Approach?</h2>
            </div>
            <div class="grid-2">
                <div>
                    <h3><i class="fas fa-brain" style="color: var(--accent-color);"></i> Psychological Aspect</h3>
                    <p>Our primary objective is to alleviate the academic burden. The knowledge usually accumulated over 10 years can be condensed effectively, allowing students ample free time in their formative years to enjoy life and promote healthy mental growth.</p>
                    <p>We streamline the curriculum, provide effective concept explanations, and adopt teaching strategies that accommodate diverse learning styles, enhancing engagement and nurturing interest.</p>
                </div>
                <div>
                    <h3><i class="fas fa-book-open" style="color: var(--accent-color);"></i> Why Cambridge Board?</h3>
                    <p>The textbooks are meticulously crafted with daily practical examples. They go beyond rote memorization, elucidating underlying concepts and practical applications to engineering problems.</p>
                    <p>Achieving an 'A*/A+/A' grade opens doors to prestigious universities worldwide including MIT, Stanford, NUS, and Cambridge.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Methodology -->
    <section id="methodology" class="section bg-white">
        <div class="container">
            <div class="section-title-wrapper">
                <h2>Methodology & Assessment</h2>
                <p>Following Integrated Quality Education Standards (IAEA)</p>
            </div>

            <div class="text-center" style="margin-bottom: 3rem;">
                <h3>The Lean Six Sigma Principle</h3>
                <div class="methodology-steps">
                    <div class="step">
                        <div class="step-num">1</div>
                        <p>Teach</p>
                    </div>
                    <div class="step">
                        <div class="step-num">2</div>
                        <p>Continuous Assessment</p>
                    </div>
                    <div class="step">
                        <div class="step-num">3</div>
                        <p>Adapt to Intellect</p>
                    </div>
                    <div class="step">
                        <div class="step-num">4</div>
                        <p>Test</p>
                    </div>
                    <div class="step">
                        <div class="step-num">5</div>
                        <p>Improve</p>
                    </div>
                </div>
            </div>

            <div class="grid-2">
                <div class="card">
                    <h3><i class="fas fa-clipboard-check"></i> Assessment Strategy</h3>
                    <ul style="padding-left: 20px; list-style: disc;">
                        <li>Homework evaluated after each class.</li>
                        <li>Timely performance updates to parents.</li>
                        <li>Examinations after completion of each chapter.</li>
                        <li>Parents encouraged to assess independently.</li>
                    </ul>
                </div>
                <div class="card">
                    <h3><i class="fas fa-calendar-alt"></i> Recommended Study Plan</h3>
                    <p>Commence with Mathematics to complete the course in 8 months. Chemistry follows once Math foundation is set. Physics is advised only after Math completion.</p>
                    <p><strong>Optimal Starting Age:</strong> 12-13 years (7th, 8th, or 9th grade).</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Syllabus -->
    <section id="syllabus" class="section">
        <div class="container">
            <div class="section-title-wrapper">
                <h2>Comprehensive Syllabus</h2>
                <p>Covering the spectrum from Basics to 10th Grade</p>
            </div>

            <div class="syllabus-grid">
                <!-- Topic 1 -->
                <div class="syllabus-item">
                    <h4>1. Number</h4>
                    <ul class="syllabus-list">
                        <li>Number manipulation, Prime numbers, Factors</li>
                        <li>Indices, Powers, Roots, Surds</li>
                        <li>Rationalising the denominator</li>
                        <li>Weights, Measures, Money</li>
                        <li>Fractions, Ratios, Proportions, Decimals, Percentages</li>
                        <li>Standard form, Upper and lower bounds</li>
                    </ul>
                </div>

                <!-- Topic 2 -->
                <div class="syllabus-item">
                    <h4>2. Sets</h4>
                    <ul class="syllabus-list">
                        <li>Idea of a set, language, and notation</li>
                        <li>Union and Intersection of sets</li>
                        <li>Complementary set, Subsets</li>
                        <li>Venn diagrams and logic problems</li>
                    </ul>
                </div>

                <!-- Topic 3 -->
                <div class="syllabus-item">
                    <h4>3. Algebra</h4>
                    <ul class="syllabus-list">
                        <li>Construction and manipulation of formulae</li>
                        <li>Factorization, Factor theorem, Algebraic division</li>
                        <li>Manipulation of algebraic fractions</li>
                        <li>Solutions to linear, quadratic, and simultaneous equations</li>
                        <li>Linear inequalities and representation on number line</li>
                    </ul>
                </div>

                <!-- Topic 4 -->
                <div class="syllabus-item">
                    <h4>4. Functions</h4>
                    <ul class="syllabus-list">
                        <li>Mapping, Notations, Domain, Range</li>
                        <li>Composite and Inverse functions</li>
                        <li>Direct and Indirect proportion</li>
                        <li>Differentiation of integer powers</li>
                        <li>Gradients, rate of change, maxima, minima</li>
                        <li>Plotting cubic and trigonometric graphs</li>
                    </ul>
                </div>

                <!-- Topic 5 -->
                <div class="syllabus-item">
                    <h4>5. Matrices</h4>
                    <ul class="syllabus-list">
                        <li>Representation of data, Addition, Multiplication</li>
                        <li>Unit matrix and Null matrix</li>
                        <li>Determinants and inverse of 2x2 matrices</li>
                        <li>Transformation of the plane associated with 2x2 matrices</li>
                    </ul>
                </div>

                <!-- Topic 6 -->
                <div class="syllabus-item">
                    <h4>6. Geometry</h4>
                    <ul class="syllabus-list">
                        <li>Angle properties of polygons and parallel lines</li>
                        <li>Properties of quadrilaterals (parallelogram, kite, etc.)</li>
                        <li>Pythagoras theorem in 2D and 3D</li>
                        <li>Similarity, Congruence (SSS, SAS, ASA)</li>
                        <li>Circle properties (Chord, angle, tangent)</li>
                        <li>Loci and Constructions</li>
                    </ul>
                </div>

                <!-- Topic 7 -->
                <div class="syllabus-item">
                    <h4>7. Mensuration</h4>
                    <ul class="syllabus-list">
                        <li>Length, Area, and Volume</li>
                        <li>2D Shapes: Rectangle, parallelogram, trapezium, triangle, circle</li>
                        <li>3D Shapes: Cylinder, cone, sphere, cuboid, pyramid, prism</li>
                        <li>Arc length and sector area</li>
                    </ul>
                </div>

                <!-- Topic 8 -->
                <div class="syllabus-item">
                    <h4>8. Vectors & Transformation</h4>
                    <ul class="syllabus-list">
                        <li>Scalar vs Vector quantities, Notation</li>
                        <li>Parallel, Unit, and Position vectors</li>
                        <li>Sum, Difference, and Modulus of vectors</li>
                        <li>Transformation of plane, Combination of transformations</li>
                    </ul>
                </div>

                <!-- Topic 9 -->
                <div class="syllabus-item">
                    <h4>9. Trigonometry</h4>
                    <ul class="syllabus-list">
                        <li>Sine, Cosine, Tangent of angles up to 180 degrees</li>
                        <li>Problems in 2D and 3D</li>
                        <li>Angle of elevation and depression</li>
                        <li>Bearings</li>
                    </ul>
                </div>

                <!-- Topic 10 -->
                <div class="syllabus-item">
                    <h4>10. Statistics & Probability</h4>
                    <ul class="syllabus-list">
                        <li>Graphical representation of data</li>
                        <li>Mean, Median, Mode (discrete & grouped)</li>
                        <li>Probability concepts and language</li>
                        <li>Addition and Product rules for events</li>
                        <li>Conditional probability and expected probability</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Other Subjects & Prerequisites -->
    <section class="section bg-white">
        <div class="container">
            <div class="grid-2">
                <div class="card" style="border-left: 5px solid var(--primary-color);">
                    <h3><i class="fas fa-atom"></i> Other Subjects</h3>
                    <p style="font-size: 1.1rem; margin-top: 1rem;">Apart from Math, we also provide specialized tutoring for:</p>
                    <ul class="qualification-list" style="margin-top: 1rem;">
                        <li><strong>Physics</strong> - Conceptual understanding and problem solving.</li>
                        <li><strong>Chemistry</strong> - Building foundations after Math mastery.</li>
                    </ul>
                </div>
                <div class="card" style="border-left: 5px solid var(--accent-color);">
                    <h3><i class="fas fa-list-check"></i> Prerequisites</h3>
                    <ul class="qualification-list">
                        <li>Students must know how to read, write, and understand English.</li>
                        <li>Students should be good at tables.</li>
                        <li>Eagerness to learn!</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA / Contact -->
    <section id="contact" class="section">
        <div class="container">
            <div class="prereq-box">
                <h2>Ready to Excel in Math?</h2>
                <p style="margin-bottom: 2rem; color: #cbd5e1;">Join Dr. Abbas Ahmed Syed Khaja for a transformative learning journey. Whether you are aiming for IIT, Cambridge, or Ivy League universities, we build the foundation for your success.</p>
                
                <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
                    <a href="https://wa.me/918124185476" class="btn" style="background: #25D366;">
                        <i class="fab fa-whatsapp"></i> WhatsApp Now
                    </a>
                    <a href="tel:+918124185476" class="btn" style="background: var(--white); color: var(--primary-color);">
                        <i class="fas fa-phone"></i> Call Us
                    </a>
                </div>
                <p style="margin-top: 1.5rem; font-size: 0.9rem; color: #94a3b8;">(+91) 81241 85476</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h4>Tutor Syed</h4>
                    <p>Revolutionizing math education with interactive conceptual classes designed to take students from basics to 10th grade mastery in 8 months.</p>
                </div>
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <a href="#about">About Teacher</a>
                    <a href="#overview">Objectives</a>
                    <a href="#syllabus">Syllabus</a>
                    <a href="#methodology">Methodology</a>
                </div>
                <div class="footer-col">
                    <h4>Contact Info</h4>
                    <p><i class="fas fa-user-graduate"></i> Dr. Abbas Ahmed Syed Khaja</p>
                    <p><i class="fab fa-whatsapp"></i> (+91) 81241 85476</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 3rem; border-top: 1px solid #334155; padding-top: 1rem;">
                <p>&copy; 2023 Tutor Syed Math Classes. All rights reserved.</p>
            </div>
        </div>
    </footer>

</body>
</html>
