<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Unlocking Your Full Potential | Fadi Albitar</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
  <style>
    /* Basic Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #00F0FF;
      --secondary: #C300FF;
      --accent: #FF00B8;
      --dark: #0A0A23;
      --light: #FFFFFF;
      --gray: #7A7A9D;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      background: var(--dark);
      color: var(--light);
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    .container {
      width: 90%;
      margin: 0 auto;
      max-width: 1200px;
      padding: 2rem 0;
      position: relative;
      z-index: 2;
    }

    /* Navigation */
    nav {
      display: flex;
      justify-content: center;
      padding: 1.5rem 0;
      background: rgba(10, 10, 35, 0.9);
      position: sticky;
      top: 0;
      z-index: 1000;
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(0, 240, 255, 0.1);
    }

    nav a {
      margin: 0 1.5rem;
      color: var(--light);
      font-weight: 500;
      transition: all 0.3s ease;
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
      background: var(--primary);
      transition: width 0.3s ease;
    }

    nav a:hover::after {
      width: 100%;
    }

    /* Hero Section */
    .hero {
      text-align: center;
      padding: 8rem 0 5rem;
      background: linear-gradient(135deg, #0A0A23 0%, #1A1A4A 100%);
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(0, 240, 255, 0.1) 0%, transparent 70%);
      animation: pulse 15s infinite alternate;
      z-index: 0;
    }

    .hero::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, 
                  rgba(195, 0, 255, 0.03) 0%, 
                  rgba(255, 0, 184, 0.03) 50%, 
                  rgba(0, 240, 255, 0.03) 100%);
      z-index: 0;
      animation: gradientShift 20s ease infinite;
      background-size: 200% 200%;
    }

    @keyframes pulse {
      0% { transform: translate(0, 0); }
      50% { transform: translate(50px, 50px); }
      100% { transform: translate(-30px, -30px); }
    }

    @keyframes gradientShift {
      0% { background-position: 0% 0%; }
      50% { background-position: 100% 100%; }
      100% { background-position: 0% 0%; }
    }

    .hero-content {
      position: relative;
      z-index: 1;
    }

    .hero h1 {
      font-size: 4rem;
      margin-bottom: 1rem;
      color: var(--light);
      text-shadow: 0 0 20px rgba(0, 240, 255, 0.5);
      animation: fadeInDown 1s ease;
    }

    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 1.5rem;
      color: var(--primary);
      animation: fadeInDown 1s ease 0.2s both;
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 800px;
      margin: 0 auto 2rem;
      color: var(--gray);
      animation: fadeIn 1s ease 0.4s both;
    }

    .book-cover {
      max-width: 300px;
      margin: 2rem auto;
      border-radius: 8px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 
                  0 0 30px rgba(0, 240, 255, 0.3),
                  0 0 60px rgba(195, 0, 255, 0.2);
      border: 2px solid rgba(255, 255, 255, 0.1);
      transform: perspective(1000px) rotateY(0deg);
      transition: transform 0.5s ease, box-shadow 0.5s ease;
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0) rotateY(0deg); }
      50% { transform: translateY(-20px) rotateY(5deg); }
    }

    .book-cover:hover {
      transform: perspective(1000px) rotateY(15deg) scale(1.05);
      box-shadow: 0 15px 40px rgba(0, 0, 0, 0.6), 
                  0 0 40px rgba(0, 240, 255, 0.4),
                  0 0 80px rgba(195, 0, 255, 0.3);
    }

    .btn {
      display: inline-block;
      background: var(--primary);
      color: var(--dark);
      padding: 1rem 2rem;
      border-radius: 50px;
      font-weight: bold;
      margin-top: 1rem;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
      border: none;
      box-shadow: 0 0 15px rgba(0, 240, 255, 0.5);
      animation: fadeInUp 1s ease 0.6s both;
    }

    .btn:hover {
      background: var(--secondary);
      color: white;
      box-shadow: 0 0 20px rgba(195, 0, 255, 0.7);
      transform: translateY(-3px) scale(1.05);
    }

    .btn::after {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.2) 0%, transparent 70%);
      transform: scale(0);
      transition: transform 0.5s ease;
    }

    .btn:hover::after {
      transform: scale(1);
    }

    /* Sections */
    .section {
      margin: 6rem 0;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.6s ease, transform 0.6s ease;
      position: relative;
    }

    .section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .section h2 {
      font-size: 2.5rem;
      margin-bottom: 1.5rem;
      color: var(--primary);
      position: relative;
      display: inline-block;
    }

    .section h2::after {
      content: '';
      position: absolute;
      bottom: -10px;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.5s ease;
    }

    .section.visible h2::after {
      transform: scaleX(1);
    }

    .section h3 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
      color: var(--secondary);
    }

    .section p {
      margin-bottom: 1.5rem;
      color: var(--gray);
    }

    /* Features */
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
    }

    .feature-card {
      background: rgba(20, 20, 50, 0.6);
      padding: 2rem;
      border-radius: 10px;
      border: 1px solid rgba(0, 240, 255, 0.2);
      transform: translateY(20px);
      opacity: 0;
      transition: all 0.5s ease;
      position: relative;
      overflow: hidden;
      backdrop-filter: blur(5px);
    }

    .section.visible .feature-card {
      transform: translateY(0);
      opacity: 1;
    }

    .feature-card:nth-child(1) { transition-delay: 0.1s; }
    .feature-card:nth-child(2) { transition-delay: 0.2s; }
    .feature-card:nth-child(3) { transition-delay: 0.3s; }
    .feature-card:nth-child(4) { transition-delay: 0.4s; }

    .feature-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(135deg, rgba(0, 240, 255, 0.05), rgba(195, 0, 255, 0.05));
      z-index: -1;
      border-radius: inherit;
    }

    .feature-card:hover {
      transform: translateY(-5px) scale(1.02);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3),
                  0 0 20px rgba(0, 240, 255, 0.2);
      border-color: var(--accent);
    }

    .feature-card h3 {
      color: var(--accent);
      margin-bottom: 1rem;
      font-size: 1.5rem;
      transition: color 0.3s ease;
    }

    .feature-card:hover h3 {
      color: var(--primary);
    }

    /* Testimonials */
    .testimonials {
      margin: 6rem 0;
    }

    .testimonial-card {
      background: rgba(20, 20, 50, 0.6);
      padding: 2rem;
      border-radius: 10px;
      margin-bottom: 2rem;
      border: 1px solid rgba(0, 240, 255, 0.2);
      transform: perspective(1000px) rotateX(0deg);
      transition: all 0.5s ease;
      backdrop-filter: blur(5px);
    }

    .testimonial-card:hover {
      transform: perspective(1000px) rotateX(5deg);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4),
                  0 0 30px rgba(195, 0, 255, 0.2);
    }

    .testimonial-text {
      font-style: italic;
      margin-bottom: 1rem;
      position: relative;
      padding-left: 2rem;
    }

    .testimonial-text::before {
      content: '"';
      font-size: 4rem;
      color: rgba(0, 240, 255, 0.3);
      position: absolute;
      left: -1rem;
      top: -1.5rem;
      line-height: 1;
    }

    .testimonial-author {
      font-weight: bold;
      color: var(--primary);
      display: flex;
      align-items: center;
    }

    .testimonial-author::before {
      content: '—';
      margin-right: 0.5rem;
      color: var(--accent);
    }

    /* Stats */
    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
      text-align: center;
    }

    .stat-item {
      padding: 2rem;
      border-radius: 10px;
      background: rgba(20, 20, 50, 0.4);
      border: 1px solid rgba(0, 240, 255, 0.1);
      transition: all 0.5s ease;
      backdrop-filter: blur(5px);
    }

    .stat-item:hover {
      background: rgba(20, 20, 50, 0.6);
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    }

    .stat-item h3 {
      font-size: 3rem;
      color: var(--primary);
      margin-bottom: 0.5rem;
      background: linear-gradient(90deg, var(--primary), var(--accent));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      transition: all 0.5s ease;
    }

    .stat-item:hover h3 {
      background: linear-gradient(90deg, var(--accent), var(--primary));
    }

    .stat-item p {
      color: var(--gray);
      font-size: 0.9rem;
      letter-spacing: 1px;
    }

    /* Floating Particles */
    .particles {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: 1;
      pointer-events: none;
    }

    .particle {
      position: absolute;
      border-radius: 50%;
      animation: float-particle linear infinite;
      pointer-events: none;
    }

    /* Different particle types */
    .particle.type1 {
      background: rgba(0, 240, 255, 0.5);
      box-shadow: 0 0 10px rgba(0, 240, 255, 0.7);
    }
    
    .particle.type2 {
      background: rgba(195, 0, 255, 0.4);
      box-shadow: 0 0 10px rgba(195, 0, 255, 0.6);
    }
    
    .particle.type3 {
      background: rgba(255, 0, 184, 0.3);
      box-shadow: 0 0 10px rgba(255, 0, 184, 0.5);
    }
    
    .particle.type4 {
      background: rgba(255, 255, 255, 0.2);
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.4);
    }

    @keyframes float-particle {
      0% {
        transform: translateY(0) translateX(0);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      90% {
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) translateX(calc(var(--random-x) * 100px));
        opacity: 0;
      }
    }
    
    /* Floating shapes */
    .floating-shape {
      position: absolute;
      opacity: 0.1;
      z-index: 0;
      animation: float-shape linear infinite;
    }
    
    .shape-circle {
      border-radius: 50%;
      background: radial-gradient(circle, var(--primary), transparent 70%);
    }
    
    .shape-triangle {
      width: 0;
      height: 0;
      border-left: 50px solid transparent;
      border-right: 50px solid transparent;
      border-bottom: 100px solid var(--secondary);
      background: transparent;
    }
    
    .shape-square {
      background: linear-gradient(45deg, var(--accent), transparent);
    }
    
    @keyframes float-shape {
      0% {
        transform: translate(0, 0) rotate(0deg);
      }
      100% {
        transform: translate(100px, -100px) rotate(360deg);
      }
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 4rem 0 2rem;
      background: linear-gradient(to bottom, rgba(10, 10, 35, 0), rgba(10, 10, 35, 1));
      color: var(--gray);
      margin-top: 3rem;
      position: relative;
    }

    footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--primary), var(--secondary), var(--accent), transparent);
    }

    footer p {
      margin-bottom: 1rem;
    }
    
    /* Social Section */
    .social-section {
      padding: 4rem 0;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    
    .social-section h2 {
      color: var(--primary);
      margin-bottom: 1rem;
    }
    
    .social-section p {
      color: var(--gray);
      margin-bottom: 2rem;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
    }
    
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 2rem;
    }
    
    .social-link {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
      color: white;
      font-size: 1.5rem;
    }
    
    .social-link:hover {
      background: var(--primary);
      color: var(--dark);
      transform: translateY(-5px) scale(1.1);
    }

    /* Responsive */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.5rem;
      }
      
      .hero h2 {
        font-size: 1.8rem;
      }
      
      nav {
        flex-wrap: wrap;
      }
      
      nav a {
        margin: 0.5rem;
      }
      
      .book-cover {
        max-width: 250px;
      }
      
      .section {
        margin: 4rem 0;
      }
      
      .features {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <!-- Floating Particles Background -->
  <div class="particles" id="particles"></div>
  
  <!-- Floating Shapes Background -->
  <div id="floating-shapes"></div>

  <nav>
    <a href="#home">HOME</a>
    <a href="#about">ABOUT</a>
    <a href="#features">FEATURES</a>
    <a href="#testimonials">TESTIMONIALS</a>
    <a href="#buy">BUY NOW</a>
  </nav>

  <div class="container">
    <section id="home" class="hero">
      <div class="hero-content">
        <h1 class="animate__animated animate__fadeInDown">UNLOCKING YOUR FULL POTENTIAL</h1>
        <h2 class="animate__animated animate__fadeInDown animate__delay-1s">By Fadi Albitar</h2>
        <p class="animate__animated animate__fadeIn animate__delay-2s">A transformative self-improvement guide tailored for college students. Packed with actionable strategies, this book helps you build unstoppable confidence, conquer self-doubt, and craft a life filled with purpose and joy.</p>
        <img src="/images/book.png" alt="Unlocking Your Full Potential Book Cover" class="book-cover animate__animated animate__fadeInUp animate__delay-3s">
        <a href="#buy" class="btn animate__animated animate__fadeInUp animate__delay-4s">GET YOUR COPY NOW</a>
      </div>
    </section>

    <section id="about" class="section">
      <h2>ABOUT THE BOOK</h2>
      <p><strong>Unlocking Your Full Potential</strong> is more than just a book - it's a roadmap to personal transformation. Designed specifically for college students navigating the challenges of higher education and young adulthood, this guide provides practical, actionable strategies to help you:</p>
      
      <div class="features">
        <div class="feature-card">
          <h3>Build Confidence</h3>
          <p>Overcome self-doubt and imposter syndrome with proven techniques that help you recognize and embrace your true worth.</p>
        </div>
        <div class="feature-card">
          <h3>Develop Resilience</h3>
          <p>Learn how to bounce back from setbacks stronger than before and turn challenges into opportunities for growth.</p>
        </div>
        <div class="feature-card">
          <h3>Find Purpose</h3>
          <p>Discover how to align your daily actions with your deepest values and create a life of meaning and fulfillment.</p>
        </div>
      </div>
    </section>

    <section id="features" class="section">
      <h2>WHAT YOU'LL LEARN</h2>
      
      <div class="features">
        <div class="feature-card">
          <h3>Mindset Mastery</h3>
          <p>Transform limiting beliefs into empowering perspectives that propel you forward in academics and life.</p>
        </div>
        <div class="feature-card">
          <h3>Productivity Systems</h3>
          <p>Study smarter, not harder with time-tested techniques for academic success without burnout.</p>
        </div>
        <div class="feature-card">
          <h3>Social Confidence</h3>
          <p>Build meaningful relationships and network effectively to create opportunities during and after college.</p>
        </div>
        <div class="feature-card">
          <h3>Emotional Intelligence</h3>
          <p>Develop self-awareness and interpersonal skills that give you an edge in both personal and professional settings.</p>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="stats">
        <div class="stat-item">
          <h3>300+</h3>
          <p>STUDENTS IMPACTED</p>
        </div>
        <div class="stat-item">
          <h3>5.0</h3>
          <p>AVERAGE RATING</p>
        </div>
        <div class="stat-item">
          <h3>10</h3>
          <p>TRANSFORMATIVE CHAPTERS</p>
        </div>
        <div class="stat-item">
          <h3>50+</h3>
          <p>PRACTICAL EXERCISES</p>
        </div>
      </div>
    </section>

    <section id="testimonials" class="section">
      <h2>WHAT READERS SAY</h2>
      
      <div class="testimonial-card">
        <p class="testimonial-text">Unlock your full potential, di Fadi Albitar: conosco l'autore personalmente, il libro è una guida pratica dedicata ai giovani studenti, godibile anche 'da grande'.</p>
        <p class="testimonial-author">Enrica</p>
      </div>
      
      <div class="testimonial-card">
        <p class="testimonial-text">This book changed my college experience completely. The confidence-building exercises helped me land my dream internship!</p>
        <p class="testimonial-author">Sarah</p>
      </div>
      
      <div class="testimonial-card">
        <p class="testimonial-text">As a first-generation student, I felt lost until I found this book. The practical advice on time management and networking was exactly what I needed.</p>
        <p class="testimonial-author">Michael</p>
      </div>
    </section>
    
    <section id="social" class="section social-section">
      <h2>Connect With Me</h2>
      <p>Follow my journey and get more tips for personal growth and success.</p>
      
      <div style="margin: 2rem auto; text-align: center;">
        <iframe src="https://www.facebook.com/plugins/video.php?height=476&href=https%3A%2F%2Fwww.facebook.com%2F100093891904979%2Fvideos%2F881703710757781%2F&show_text=false&width=476&t=0" width="476" height="476" style="border:none;overflow:hidden; max-width: 100%;" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>
      </div>
      
      <div class="social-links">
        <a href="https://www.facebook.com/profile.php?id=100093891904979" target="_blank" class="social-link">f</a>
        <a href="#" target="_blank" class="social-link">in</a>
        <a href="#" target="_blank" class="social-link">t</a>
        <a href="#" target="_blank" class="social-link">yt</a>
      </div>
    </section>

    <section id="buy" class="section" style="text-align: center;">
      <h2>READY TO UNLOCK YOUR POTENTIAL?</h2>
      <p>Available in paperback, ebook, and audiobook formats</p>
      <a href="https://amzn.eu/d/2ebJ00C" class="btn">BUY NOW</a>
    </section>
  </div>

  <footer>
    <p>&copy; 2023 Fadi Albitar. All rights reserved.</p>
    <p>DESIGN BY HYKROX</p>
  </footer>

  <script>
    // Create floating particles with different types
    function createParticles() {
      const particlesContainer = document.getElementById('particles');
      const particleCount = 50;
      
      for (let i = 0; i < particleCount; i++) {
        const particle = document.createElement('div');
        const particleType = Math.floor(Math.random() * 4) + 1;
        particle.classList.add('particle', `type${particleType}`);
        
        // Random size between 1px and 5px
        const size = Math.random() * 4 + 1;
        particle.style.width = `${size}px`;
        particle.style.height = `${size}px`;
        
        // Random position
        particle.style.left = `${Math.random() * 100}%`;
        particle.style.bottom = `-10px`;
        
        // Random animation duration between 10s and 30s
        const duration = Math.random() * 20 + 10;
        particle.style.animationDuration = `${duration}s`;
        
        // Random delay
        particle.style.animationDelay = `${Math.random() * 10}s`;
        
        // Random horizontal movement
        particle.style.setProperty('--random-x', Math.random() * 2 - 1);
        
        particlesContainer.appendChild(particle);
      }
    }
    
    // Create floating shapes
    function createFloatingShapes() {
      const container = document.getElementById('floating-shapes');
      const shapeCount = 8;
      
      for (let i = 0; i < shapeCount; i++) {
        const shape = document.createElement('div');
        const shapeType = Math.floor(Math.random() * 3);
        const size = Math.random() * 150 + 50;
        const opacity = Math.random() * 0.1 + 0.05;
        
        if (shapeType === 0) {
          shape.classList.add('floating-shape', 'shape-circle');
          shape.style.width = `${size}px`;
          shape.style.height = `${size}px`;
        } else if (shapeType === 1) {
          shape.classList.add('floating-shape', 'shape-triangle');
          shape.style.borderLeftWidth = `${size/2}px`;
          shape.style.borderRightWidth = `${size/2}px`;
          shape.style.borderBottomWidth = `${size}px`;
        } else {
          shape.classList.add('floating-shape', 'shape-square');
          shape.style.width = `${size}px`;
          shape.style.height = `${size}px`;
        }
        
        shape.style.opacity = opacity;
        shape.style.left = `${Math.random() * 100}%`;
        shape.style.top = `${Math.random() * 100}%`;
        
        // Random animation duration between 30s and 60s
        const duration = Math.random() * 30 + 30;
        shape.style.animationDuration = `${duration}s`;
        
        container.appendChild(shape);
      }
    }
    
    // Intersection Observer for scroll animations
    function setupIntersectionObserver() {
      const sections = document.querySelectorAll('.section');
      
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
          }
        });
      }, { threshold: 0.1 });
      
      sections.forEach(section => {
        observer.observe(section);
      });
    }
    
    // Smooth scrolling for anchor links
    function setupSmoothScrolling() {
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          e.preventDefault();
          
          const targetId = this.getAttribute('href');
          if (targetId === '#') return;
          
          const targetElement = document.querySelector(targetId);
          if (targetElement) {
            window.scrollTo({
              top: targetElement.offsetTop - 80,
              behavior: 'smooth'
            });
          }
        });
      });
    }
    
    // Mouse move parallax effect
    function setupParallaxEffect() {
      document.addEventListener('mousemove', (e) => {
        const x = e.clientX / window.innerWidth;
        const y = e.clientY / window.innerHeight;
        
        const particles = document.querySelector('.particles');
        particles.style.transform = `translate(${x * 20}px, ${y * 20}px)`;
        
        const shapes = document.querySelector('#floating-shapes');
        shapes.style.transform = `translate(${x * -10}px, ${y * -10}px)`;
      });
    }
    
    // Initialize everything when DOM is loaded
    document.addEventListener('DOMContentLoaded', () => {
      createParticles();
      createFloatingShapes();
      setupIntersectionObserver();
      setupSmoothScrolling();
      setupParallaxEffect();
      
      // Add hover effect to feature cards
      const featureCards = document.querySelectorAll('.feature-card');
      featureCards.forEach(card => {
        card.addEventListener('mouseenter', () => {
          card.style.transform = 'translateY(-5px) scale(1.02)';
          card.style.boxShadow = '0 10px 25px rgba(0, 0, 0, 0.3), 0 0 20px rgba(0, 240, 255, 0.2)';
          card.style.borderColor = 'var(--accent)';
        });
        
        card.addEventListener('mouseleave', () => {
          card.style.transform = 'translateY(0) scale(1)';
          card.style.boxShadow = 'none';
          card.style.borderColor = 'rgba(0, 240, 255, 0.2)';
        });
      });
    });
  </script>
</body>
</html>