<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="SalesBot AI - Intelligent Audio Sales Assistant powered by ChatGPT. Experience advanced audio interactions, voice commands, and real-time analytics to transform your sales process.">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>SalesBot AI - Intelligent Audio Sales Assistant</title>
  <!-- Open Graph Tags -->
  <meta property="og:title" content="SalesBot AI">
  <meta property="og:description" content="Transform your sales with intelligent audio interactions.">
  <meta property="og:type" content="website">
  <!-- AOS CSS for scroll animations -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <!-- Google Fonts for a futuristic feel -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <!-- Wavesurfer.js for audio waveform visualization -->
  <script src="https://unpkg.com/wavesurfer.js"></script>
  <style>
    :root {
      --primary-color: #4b95dd;
      --secondary-color: #19c37d;
      --background: #121212;
      --surface: #1e1e1e;
      --text-color: #f5f5f5;
      --text-muted: #b0b0b0;
      --footer-bg: #1a1a1a;
      --shadow: rgba(0,0,0,0.2);
    }
    * {
      box-sizing: border-box;
    }
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: var(--background);
      color: var(--text-color);
      line-height: 1.6;
    }
    h1, h2, h3, h4 {
      font-family: 'Orbitron', sans-serif;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    header {
      background-color: var(--footer-bg);
      padding: 20px 0;
      box-shadow: 0 4px 6px var(--shadow);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 24px;
      font-weight: bold;
      color: var(--primary-color);
      display: flex;
      align-items: center;
    }
    .logo-icon {
      width: 32px;
      height: 32px;
      background-color: var(--primary-color);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
    }
    .nav-links {
      display: flex;
      gap: 20px;
    }
    .nav-links a:hover {
      color: var(--text-color);
    }
    /* Hero Section */
    .hero {
      position: relative;
      padding: 80px 0;
      text-align: center;
      background-color: var(--surface);
      border-bottom: 1px solid #333;
      overflow: hidden;
    }
    #particles-js {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
    }
    .hero-content {
      position: relative;
      z-index: 1;
    }
    .typed-cursor {
      font-size: 2.8rem;
      opacity: 1;
      animation: blink 0.7s infinite;
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }
    .hero h1 {
      font-size: 2.8rem;
      margin-bottom: 20px;
    }
    .hero p {
      font-size: 1.2rem;
      max-width: 800px;
      margin: 0 auto 30px;
      color: var(--text-muted);
    }
    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }
    .cta-button, .secondary-button {
      padding: 12px 30px;
      border-radius: 4px;
      font-weight: bold;
      transition: all 0.3s;
    }
    .cta-button {
      background-color: var(--primary-color);
      color: var(--text-color);
    }
    .cta-button:hover {
      background-color: #3a7ab7;
    }
    .secondary-button {
      background-color: transparent;
      color: var(--primary-color);
      border: 1px solid var(--primary-color);
    }
    .secondary-button:hover {
      background-color: rgba(75,149,221,0.1);
    }
    /* Features Section */
    .features {
      padding: 80px 0;
    }
    .section-title {
      text-align: center;
      margin-bottom: 20px;
      font-size: 2.2rem;
    }
    .section-subtitle {
      text-align: center;
      margin-bottom: 50px;
      font-size: 1.2rem;
      color: var(--text-muted);
      max-width: 800px;
      margin: 0 auto;
    }
    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
    }
    .feature-card {
      background-color: #2a2a2a;
      border-radius: 12px;
      padding: 30px;
      box-shadow: 0 4px 6px var(--shadow);
      transition: transform 0.3s, box-shadow 0.3s;
      text-align: center;
    }
    .feature-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px var(--shadow);
    }
    .feature-icon {
      font-size: 2rem;
      margin-bottom: 20px;
      color: var(--primary-color);
    }
    /* Chatbot Demo Section */
    .chatbot-demo {
      padding: 80px 0;
      background-color: var(--surface);
    }
    .chatbot-container {
      display: flex;
      flex-direction: column;
      gap: 40px;
    }
    .chatbot-info {
      text-align: center;
    }
    .chatbot-info h2 {
      font-size: 2rem;
      margin-bottom: 20px;
    }
    .chatbot-info p {
      margin-bottom: 20px;
      color: var(--text-muted);
    }
    /* Embed iframe styling for the ChatGPT Sales Trainer bot */
    .bot-embed {
      width: 100%;
      height: 600px;
      border: none;
      border-radius: 12px;
      box-shadow: 0 4px 15px var(--shadow);
    }
    /* Footer */
    footer {
      background-color: var(--footer-bg);
      padding: 80px 0 40px;
      color: var(--text-muted);
    }
    .footer-content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 40px;
      margin-bottom: 40px;
    }
    .footer-column h3 {
      color: var(--text-color);
      margin-bottom: 20px;
      font-size: 1.2rem;
    }
    .footer-column ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    .footer-column ul li {
      margin-bottom: 12px;
    }
    .footer-column ul li a:hover {
      color: var(--text-color);
    }
    .social-links {
      display: flex;
      gap: 15px;
      justify-content: center;
      margin-top: 20px;
    }
    .social-link {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: #2a2a2a;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text-color);
      transition: background-color 0.3s;
    }
    .social-link:hover {
      background-color: var(--primary-color);
    }
    .copyright {
      text-align: center;
      padding-top: 40px;
      border-top: 1px solid #333;
      font-size: 0.9rem;
      color: #777;
    }
    /* Responsive */
    @media (max-width: 992px) {
      .chatbot-container {
        flex-direction: column;
      }
    }
    @media (max-width: 768px) {
      .nav-links {
        display: none;
      }
      .hero h1 {
        font-size: 2rem;
      }
      .buttons {
        flex-direction: column;
      }
      .cta-button, .secondary-button {
        width: 100%;
        max-width: 300px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container" data-aos="fade-down">
      <nav>
        <div class="logo">
          <div class="logo-icon">S</div>
          SalesBot AI
        </div>
        <div class="nav-links">
          <a href="index.html">Home</a>
          <a href="about.html">About</a>
          <a href="support.html">Support</a>
          <a href="legal.html">Legal</a>
        </div>
      </nav>
    </div>
  </header>
  <main>
    <!-- Hero Section -->
    <section class="hero" id="home">
      <div id="particles-js"></div>
      <div class="container hero-content" data-aos="fade-up">
        <h1><span id="typed"></span></h1>
        <p>Experience the future of sales with our advanced AI-powered chatbot. Leverage state-of-the-art speech-to-text, voice modulation, sentiment analysis, and real-time audio waveform visualization to revolutionize your sales interactions.</p>
        <div class="buttons">
          <a href="#chatbot" class="cta-button">Try the Chatbot Demo</a>
          <a href="support.html" class="secondary-button">Get Support</a>
        </div>
      </div>
    </section>
    <!-- Features Section -->
    <section class="features" id="features">
      <div class="container" data-aos="fade-up">
        <h2 class="section-title">Advanced Audio & Chatbot Capabilities</h2>
        <p class="section-subtitle">Empower your sales team with interactive voice commands, detailed transcripts, recording and playback, and more—all designed to drive revenue growth.</p>
        <div class="features-grid">
          <div class="feature-card" data-aos="zoom-in">
            <div class="feature-icon">🎤</div>
            <h3>Advanced Speech-to-Text</h3>
            <p>Convert spoken words into text in real time with high accuracy, ensuring seamless transcript generation and interaction logging.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="100">
            <div class="feature-icon">🔊</div>
            <h3>Real-Time Voice Modulation</h3>
            <p>Apply dynamic voice modulation to enhance audio clarity and deliver a polished, professional sound during every interaction.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="200">
            <div class="feature-icon">😊</div>
            <h3>Sentiment Analysis</h3>
            <p>Analyze the tone and mood of conversations to tailor responses and improve customer engagement through actionable insights.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="300">
            <div class="feature-icon">📈</div>
            <h3>Audio Waveform Visualization</h3>
            <p>Visualize your audio inputs in real time with detailed waveform graphics, providing deeper insights into conversation dynamics.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="400">
            <div class="feature-icon">🗣️</div>
            <h3>Interactive Voice Commands</h3>
            <p>Control the chatbot interface seamlessly with voice commands to initiate recording, playback, and navigation.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="500">
            <div class="feature-icon">📝</div>
            <h3>Detailed Transcripts</h3>
            <p>Automatically generate and display accurate transcripts of your interactions to ensure nothing is missed.</p>
          </div>
          <div class="feature-card" data-aos="zoom-in" data-aos-delay="600">
            <div class="feature-icon">⏺️</div>
            <h3>Recording & Playback</h3>
            <p>Record your sessions for training and review, with easy playback functionality integrated into the platform.</p>
          </div>
        </div>
      </div>
    </section>
    <!-- Chatbot Demo Section -->
    <section class="chatbot-demo" id="chatbot">
      <div class="container" data-aos="fade-up">
        <div class="chatbot-info">
          <h2>Interactive Chatbot Demo</h2>
          <p>Engage with our Sales Trainer bot—powered by ChatGPT—and experience advanced audio interactions including voice commands, real-time waveform visualization, and live transcript updates. No login is required.</p>
        </div>
        <!-- Seamlessly embed your Sales Trainer bot -->
        <iframe class="bot-embed" src="https://chatgpt.com/g/g-67be87f079888191bfa2e2dcd1e66771-sales-trainer" allow="microphone; autoplay;"></iframe>
      </div>
    </section>
  </main>
  <footer>
    <div class="container" data-aos="fade-up">
      <div class="footer-content">
        <div class="footer-column">
          <h3>Company</h3>
          <ul>
            <li><a href="about.html#our-story">Our Story</a></li>
            <li><a href="about.html#mission-vision">Mission & Vision</a></li>
            <li><a href="about.html#careers">Careers</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>Support</h3>
          <ul>
            <li><a href="support.html#help-center">Help Center</a></li>
            <li><a href="support.html#faqs">FAQs</a></li>
            <li><a href="support.html#contact-support">Contact Support</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>Legal</h3>
          <ul>
            <li><a href="legal.html#privacy-policy">Privacy Policy</a></li>
            <li><a href="legal.html#terms-of-service">Terms of Service</a></li>
          </ul>
        </div>
      </div>
      <div class="social-links">
        <a href="#" class="social-link">F</a>
        <a href="#" class="social-link">T</a>
        <a href="#" class="social-link">I</a>
      </div>
      <div class="copyright">
        &copy; 2025 SalesBot AI. All Rights Reserved.
      </div>
    </div>
  </footer>
  <!-- Scripts -->
  <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
  <script>
    particlesJS("particles-js", {
      "particles": {
        "number": {
          "value": 80,
          "density": { "enable": true, "value_area": 800 }
        },
        "color": { "value": "#4b95dd" },
        "shape": {
          "type": "circle",
          "stroke": { "width": 0, "color": "#000" },
          "polygon": { "nb_sides": 5 }
        },
        "opacity": { "value": 0.5, "random": false },
        "size": { "value": 3, "random": true },
        "line_linked": {
          "enable": true,
          "distance": 150,
          "color": "#4b95dd",
          "opacity": 0.4,
          "width": 1
        },
        "move": {
          "enable": true,
          "speed": 2,
          "direction": "none",
          "random": false,
          "straight": false,
          "out_mode": "out"
        }
      },
      "interactivity": {
        "detect_on": "canvas",
        "events": {
          "onhover": { "enable": true, "mode": "repulse" },
          "onclick": { "enable": true, "mode": "push" }
        },
        "modes": {
          "repulse": { "distance": 100 },
          "push": { "particles_nb": 4 }
        }
      },
      "retina_detect": true
    });
  </script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, easing: 'ease-in-out', once: true });
  </script>
  <script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
  <script>
    var typed = new Typed('#typed', {
      strings: ["Transform Your Sales with Intelligent Audio Interactions", "Experience Advanced Chatbot Capabilities"],
      typeSpeed: 60,
      backSpeed: 30,
      loop: true
    });
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="About SalesBot AI - Our Story, Mission & Vision, Careers. Learn how we are revolutionizing sales with advanced AI and audio technology.">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>About Us - SalesBot AI</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #4b95dd;
      --background: #121212;
      --surface: #1e1e1e;
      --text-color: #f5f5f5;
      --text-muted: #b0b0b0;
      --footer-bg: #1a1a1a;
      --shadow: rgba(0,0,0,0.2);
    }
    * { box-sizing: border-box; }
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--background);
      color: var(--text-color);
      line-height: 1.6;
    }
    h1, h2, h3, h4 { font-family: 'Orbitron', sans-serif; }
    a { text-decoration: none; color: inherit; }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    header {
      background-color: var(--footer-bg);
      padding: 20px 0;
      box-shadow: 0 4px 6px var(--shadow);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 24px;
      font-weight: bold;
      color: var(--primary-color);
      display: flex;
      align-items: center;
    }
    .logo-icon {
      width: 32px;
      height: 32px;
      background-color: var(--primary-color);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
    }
    .nav-links {
      display: flex;
      gap: 20px;
    }
    .nav-links a:hover { color: var(--text-color); }
    main { padding: 60px 0; }
    section { margin-bottom: 60px; }
    .section-title {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 20px;
    }
    .section-content {
      font-size: 1.1rem;
      color: var(--text-muted);
      line-height: 1.8;
      max-width: 800px;
      margin: 0 auto;
      text-align: justify;
    }
    footer {
      background-color: var(--footer-bg);
      padding: 40px 0;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>
    <div class="container" data-aos="fade-down">
      <nav>
        <div class="logo">
          <div class="logo-icon">S</div>
          SalesBot AI
        </div>
        <div class="nav-links">
          <a href="index.html">Home</a>
          <a href="about.html">About</a>
          <a href="support.html">Support</a>
          <a href="legal.html">Legal</a>
        </div>
      </nav>
    </div>
  </header>
  <main class="container">
    <!-- Our Story Section -->
    <section id="our-story" data-aos="fade-up">
      <h2 class="section-title">Our Story</h2>
      <div class="section-content">
        <p>Founded in 2020, SalesBot AI began with a revolutionary vision: to transform the sales landscape using the power of artificial intelligence and advanced audio technologies. Our founders—seasoned sales professionals and innovative technologists—recognized early the potential for AI to streamline processes and create personalized, interactive customer experiences.</p>
        <p>From our humble startup beginnings, we have rapidly grown into a trusted partner for leading sales organizations worldwide. Our relentless commitment to innovation drives us to continually enhance our platform, ensuring that our clients stay ahead in today’s competitive market.</p>
      </div>
    </section>
    <!-- Mission & Vision Section -->
    <section id="mission-vision" data-aos="fade-up">
      <h2 class="section-title">Mission & Vision</h2>
      <div class="section-content">
        <p><strong>Our Mission:</strong> To empower sales professionals with intelligent, audio-driven tools that enhance communication, streamline processes, and boost revenue. We are committed to transforming every sales interaction into an opportunity for success.</p>
        <p><strong>Our Vision:</strong> To be the global leader in AI-powered sales technology, redefining customer engagement and sales performance through innovative automation and human insight.</p>
      </div>
    </section>
    <!-- Careers Section -->
    <section id="careers" data-aos="fade-up">
      <h2 class="section-title">Careers</h2>
      <div class="section-content">
        <p>At SalesBot AI, we believe our people are our greatest asset. We seek passionate, creative, and dedicated individuals eager to push the boundaries of technology and redefine the sales industry.</p>
        <p>Whether you are a software developer, data scientist, sales strategist, or customer support expert, there is a place for you on our team. Join us and help shape the future of sales technology. Explore our current openings and discover the opportunity to grow with us.</p>
      </div>
    </section>
  </main>
  <footer>
    <div class="container">
      &copy; 2025 SalesBot AI. All Rights Reserved.
    </div>
  </footer>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, easing: 'ease-in-out', once: true });
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Support for SalesBot AI - Access our Help Center, FAQs, and contact support for assistance with our advanced AI-powered sales assistant.">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Support - SalesBot AI</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #4b95dd;
      --background: #121212;
      --surface: #1e1e1e;
      --text-color: #f5f5f5;
      --text-muted: #b0b0b0;
      --footer-bg: #1a1a1a;
      --shadow: rgba(0,0,0,0.2);
    }
    * { box-sizing: border-box; }
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--background);
      color: var(--text-color);
      line-height: 1.6;
    }
    h1, h2, h3, h4 { font-family: 'Orbitron', sans-serif; }
    a { text-decoration: none; color: inherit; }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    header {
      background-color: var(--footer-bg);
      padding: 20px 0;
      box-shadow: 0 4px 6px var(--shadow);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 24px;
      font-weight: bold;
      color: var(--primary-color);
      display: flex;
      align-items: center;
    }
    .logo-icon {
      width: 32px;
      height: 32px;
      background-color: var(--primary-color);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
    }
    .nav-links {
      display: flex;
      gap: 20px;
    }
    .nav-links a:hover { color: var(--text-color); }
    main { padding: 60px 0; }
    section { margin-bottom: 60px; }
    .section-title {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 20px;
    }
    .section-content {
      font-size: 1.1rem;
      color: var(--text-muted);
      line-height: 1.8;
      max-width: 800px;
      margin: 0 auto;
      text-align: justify;
    }
    footer {
      background-color: var(--footer-bg);
      padding: 40px 0;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <header>
    <div class="container" data-aos="fade-down">
      <nav>
        <div class="logo">
          <div class="logo-icon">S</div>
          SalesBot AI
        </div>
        <div class="nav-links">
          <a href="index.html">Home</a>
          <a href="about.html">About</a>
          <a href="support.html">Support</a>
          <a href="legal.html">Legal</a>
        </div>
      </nav>
    </div>
  </header>
  <main class="container">
    <!-- Help Center Section -->
    <section id="help-center" data-aos="fade-up">
      <h2 class="section-title">Help Center</h2>
      <div class="section-content">
        <p>Welcome to the SalesBot AI Help Center. Our resource library provides comprehensive guides, tutorials, and troubleshooting tips to help you get the most out of our advanced AI-powered sales assistant. Whether you're a new user or an experienced professional exploring advanced features, our articles and videos have you covered.</p>
      </div>
    </section>
    <!-- FAQs Section -->
    <section id="faqs" data-aos="fade-up">
      <h2 class="section-title">Frequently Asked Questions</h2>
      <div class="section-content">
        <h3>How does the advanced speech-to-text feature work?</h3>
        <p>Our platform leverages cutting-edge AI algorithms to convert spoken language into text in real time, ensuring fast and accurate transcription.</p>
        <h3>Can I customize voice modulation settings?</h3>
        <p>Yes—you can adjust various parameters in our settings panel to match your desired tone and style, enhancing the professionalism of your interactions.</p>
        <h3>What role does sentiment analysis play?</h3>
        <p>Sentiment analysis evaluates the emotional tone of conversations, enabling the chatbot to adapt its responses for more empathetic engagement.</p>
        <h3>How do I record and playback my sessions?</h3>
        <p>Our integrated recording feature allows you to capture live sessions for review and training, with intuitive playback controls built into the platform.</p>
      </div>
    </section>
    <!-- Contact Support Section -->
    <section id="contact-support" data-aos="fade-up">
      <h2 class="section-title">Contact Support</h2>
      <div class="section-content">
        <p>If you need further assistance or have questions about SalesBot AI, our dedicated support team is here to help. Reach out to us at:</p>
        <p>Email: <a href="mailto:support@salesbotai.com" style="color: var(--primary-color);">support@salesbotai.com</a></p>
        <p>Phone: +1 (800) 123-4567</p>
        <p>Support Hours: Monday – Friday, 9 AM – 6 PM (EST)</p>
      </div>
    </section>
  </main>
  <footer>
    <div class="container">
      &copy; 2025 SalesBot AI. All Rights Reserved.
    </div>
  </footer>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, easing: 'ease-in-out', once: true });
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Legal information for SalesBot AI, including our Privacy Policy and Terms of Service.">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Legal - SalesBot AI</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #4b95dd;
      --background: #121212;
      --surface: #1e1e1e;
      --text-color: #f5f5f5;
      --text-muted: #b0b0b0;
      --footer-bg: #1a1a1a;
      --shadow: rgba(0,0,0,0.2);
    }
    * { box-sizing: border-box; }
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--background);
      color: var(--text-color);
      line-height: 1.6;
    }
    h1, h2, h3, h4 { font-family: 'Orbitron', sans-serif; }
    a { text-decoration: none; color: inherit; }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    header {
      background-color: var(--footer-bg);
      padding: 20px 0;
      box-shadow: 0 4px 6px var(--shadow);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-size: 24px;
      font-weight: bold;
      color: var(--primary-color);
      display: flex;
      align-items: center;
    }
    .logo-icon {
      width: 32px;
      height: 32px;
      background-color: var(--primary-color);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
    }
    .nav-links {
      display: flex;
      gap: 20px;
    }
    .nav-links a:hover { color: var(--text-color); }
    main { padding: 60px 0; }
    section { margin-bottom: 60px; }
    .section-title {
      font-size: 2rem;
      text-align: center;
      margin-bottom: 20px;
    }
    .section-content {
      font-size: 1.1rem;
      color: var(--text-muted);
      line-height: 1.8;
      max-width: 800px;
      margin: 0 auto;
      text-align: justify;
    }
    footer {
      background-color: var(--footer-bg);
      padding: 40px 0;
      text-align: center;
      color: var(--text-muted);
      font-size: 0.9rem;
    }
    ul { margin-left: 20px; }
  </style>
</head>
<body>
  <header>
    <div class="container" data-aos="fade-down">
      <nav>
        <div class="logo">
          <div class="logo-icon">S</div>
          SalesBot AI
        </div>
        <div class="nav-links">
          <a href="index.html">Home</a>
          <a href="about.html">About</a>
          <a href="support.html">Support</a>
          <a href="legal.html">Legal</a>
        </div>
      </nav>
    </div>
  </header>
  <main class="container">
    <!-- Privacy Policy Section -->
    <section id="privacy-policy" data-aos="fade-up">
      <h2 class="section-title">Privacy Policy</h2>
      <div class="section-content">
        <p>Your privacy is critically important to us at SalesBot AI. We adhere to strict policies designed to protect your personal information and ensure a secure experience. Key principles include:</p>
        <ul>
          <li>Collecting only the information necessary to provide our services.</li>
          <li>Storing your data securely and not sharing it with third parties without consent, except as required by law.</li>
          <li>Implementing industry-standard security measures to safeguard your data.</li>
        </ul>
        <p><strong>Information Collection:</strong> We gather data provided during account registration and service use, as well as automatically collected usage data and cookies, to improve your experience.</p>
        <p><strong>Use of Information:</strong> Your data is used to personalize our services, enhance functionality, and communicate important updates. We do not sell your personal information.</p>
        <p><strong>Data Security:</strong> Our systems employ robust encryption and security protocols to ensure your data remains confidential and protected.</p>
      </div>
    </section>
    <!-- Terms of Service Section -->
    <section id="terms-of-service" data-aos="fade-up">
      <h2 class="section-title">Terms of Service</h2>
      <div class="section-content">
        <p>Welcome to SalesBot AI. By accessing or using our services, you agree to the following terms and conditions. Please read them carefully:</p>
        <p><strong>1. Acceptance of Terms:</strong> Your use of our services constitutes acceptance of these terms. If you do not agree, please refrain from using our platform.</p>
        <p><strong>2. License:</strong> We grant you a limited, non-exclusive, non-transferable license to use our services for your internal business purposes only.</p>
        <p><strong>3. Modifications:</strong> SalesBot AI reserves the right to modify or suspend any aspect of our services at any time without prior notice. Continued use signifies acceptance of any changes.</p>
        <p><strong>4. Disclaimer:</strong> Our services are provided "as is" without warranties. SalesBot AI is not liable for any damages arising from use or inability to use our services.</p>
        <p><strong>5. Governing Law:</strong> These terms are governed by the laws of the jurisdiction in which SalesBot AI operates. Disputes will be resolved in the appropriate courts.</p>
      </div>
    </section>
  </main>
  <footer>
    <div class="container">
      &copy; 2025 SalesBot AI. All Rights Reserved.
    </div>
  </footer>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    AOS.init({ duration: 1000, easing: 'ease-in-out', once: true });
  </script>
</body>
</html>
