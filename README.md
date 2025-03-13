<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SalesTrainer AI - Powered by ChatGPT</title>
  <style>
    /* Base styling */
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: #f5f5f5;
      background-color: #121212;
    }
    
    /* Layout */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    /* Header */
    header {
      background-color: #1a1a1a;
      padding: 20px 0;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
    }
    
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .logo {
      font-size: 24px;
      font-weight: bold;
      color: #4b95dd;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    
    .logo-icon {
      width: 32px;
      height: 32px;
      background-color: #4b95dd;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-weight: bold;
    }
    
    .nav-links {
      display: flex;
      gap: 20px;
    }
    
    .nav-links a {
      color: #b0b0b0;
      text-decoration: none;
      transition: color 0.3s;
    }
    
    .nav-links a:hover {
      color: #f5f5f5;
    }
    
    /* Hero Section */
    .hero {
      padding: 80px 0;
      text-align: center;
      background-color: #1e1e1e;
      border-bottom: 1px solid #333;
      position: relative;
      overflow: hidden;
    }
    
    .hero-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0.1;
      background-image: url('/api/placeholder/1200/600');
      background-size: cover;
      background-position: center;
      z-index: 0;
    }
    
    .hero-content {
      position: relative;
      z-index: 1;
    }
    
    .hero h1 {
      font-size: 2.8rem;
      margin-bottom: 20px;
      color: #fff;
    }
    
    .hero p {
      font-size: 1.2rem;
      max-width: 800px;
      margin: 0 auto 30px;
      color: #b0b0b0;
    }
    
    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }
    
    .cta-button {
      display: inline-block;
      background-color: #4b95dd;
      color: white;
      padding: 12px 30px;
      border-radius: 4px;
      text-decoration: none;
      font-weight: bold;
      transition: background-color 0.3s;
    }
    
    .cta-button:hover {
      background-color: #3a7ab7;
    }
    
    .secondary-button {
      display: inline-block;
      background-color: transparent;
      color: #4b95dd;
      padding: 12px 30px;
      border-radius: 4px;
      text-decoration: none;
      font-weight: bold;
      border: 1px solid #4b95dd;
      transition: all 0.3s;
    }
    
    .secondary-button:hover {
      background-color: rgba(75, 149, 221, 0.1);
    }
    
    .gpt-badge {
      display: inline-block;
      background-color: #19c37d;
      color: white;
      padding: 6px 12px;
      border-radius: 16px;
      font-size: 0.9rem;
      font-weight: bold;
      margin-bottom: 20px;
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
      color: #b0b0b0;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
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
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
    
    .feature-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    }
    
    .feature-icon {
      width: 60px;
      height: 60px;
      background-color: rgba(75, 149, 221, 0.2);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 20px;
    }
    
    .feature-card h3 {
      font-size: 1.4rem;
      margin-top: 0;
      color: #4b95dd;
      margin-bottom: 15px;
    }
    
    /* Methodology Section */
    .methodology {
      padding: 80px 0;
      background-color: #1e1e1e;
    }
    
    .methodology-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }
    
    .methodology-image {
      background-color: #2a2a2a;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
      height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    
    .methodology-content h2 {
      color: #fff;
      margin-top: 0;
      font-size: 2rem;
      margin-bottom: 20px;
    }
    
    .methodology-content p {
      margin-bottom: 20px;
      color: #b0b0b0;
    }
    
    .methodology-steps {
      margin-top: 30px;
    }
    
    .methodology-step {
      display: flex;
      align-items: flex-start;
      margin-bottom: 20px;
    }
    
    .step-number {
      background-color: #4b95dd;
      color: white;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      margin-right: 15px;
      flex-shrink: 0;
    }
    
    .step-content {
      flex: 1;
    }
    
    .step-content h4 {
      margin-top: 0;
      margin-bottom: 8px;
      color: #fff;
    }
    
    /* Zach Seager Highlights Section */
    .zach-highlights {
      padding: 80px 0;
      background-color: #1e1e1e;
    }
    
    .zach-highlights .audio-player {
      text-align: center;
      margin: 20px 0;
    }
    
    .zach-highlights audio {
      width: 100%;
      max-width: 600px;
    }
    
    .highlights-text ul {
      list-style: none;
      padding: 0;
      color: #b0b0b0;
      font-size: 1.1rem;
    }
    
    .highlights-text li {
      margin-bottom: 10px;
    }
    
    /* Audio Demo Section */
    .audio-demo {
      padding: 80px 0;
    }
    
    .demo-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }
    
    .demo-content {
      display: flex;
      flex-direction: column;
    }
    
    .audio-player {
      background-color: #2a2a2a;
      border-radius: 12px;
      padding: 30px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }
    
    .audio-controls {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 20px;
    }
    
    .audio-progress {
      width: 100%;
      height: 6px;
      background-color: #3a3a3a;
      border-radius: 3px;
      margin-bottom: 20px;
      position: relative;
    }
    
    .progress-bar {
      position: absolute;
      left: 0;
      top: 0;
      height: 100%;
      background-color: #4b95dd;
      border-radius: 3px;
      width: 35%;
    }
    
    .control-button {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background-color: #4b95dd;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      border: none;
      cursor: pointer;
    }
    
    .time-display {
      color: #b0b0b0;
    }
    
    /* Chat Demo Section */
    .chat-demo {
      padding: 80px 0;
      background-color: #1e1e1e;
    }
    
    .chat-interface {
      background-color: #2a2a2a;
      border-radius: 12px;
      padding: 20px;
      height: 500px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    }
    
    .chat-messages {
      flex: 1;
      overflow-y: auto;
      padding: 10px;
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    
    .message {
      padding: 10px 15px;
      border-radius: 18px;
      max-width: 80%;
      word-break: break-word;
    }
    
    .ai-message {
      background-color: #3a3a3a;
      align-self: flex-start;
    }
    
    .user-message {
      background-color: #4b95dd;
      align-self: flex-end;
    }
    
    .chat-input {
      display: flex;
      padding: 10px;
      gap: 10px;
      border-top: 1px solid #444;
      margin-top: 10px;
    }
    
    .chat-input input {
      flex: 1;
      padding: 10px;
      border-radius: 4px;
      border: 1px solid #444;
      background-color: #333;
      color: #fff;
    }
    
    .mic-button {
      background-color: #19c37d;
      color: white;
      border: none;
      border-radius: 4px;
      padding: 10px 15px;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 5px;
    }
    
    .send-button {
      background-color: #4b95dd;
      color: white;
      border: none;
      border-radius: 4px;
      padding: 10px 15px;
      cursor: pointer;
    }
    
    /* Pricing Section */
    .pricing {
      padding: 80px 0;
      background-color: #1e1e1e;
    }
    
    .pricing-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      margin-top: 30px;
    }
    
    .pricing-card {
      background-color: #2a2a2a;
      border-radius: 12px;
      padding: 30px;
      text-align: center;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
      display: flex;
      flex-direction: column;
    }
    
    .pricing-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    }
    
    .pricing-card.popular {
      border: 2px solid #4b95dd;
      position: relative;
    }
    
    .popular-tag {
      position: absolute;
      top: -15px;
      left: 50%;
      transform: translateX(-50%);
      background-color: #4b95dd;
      color: white;
      padding: 5px 15px;
      border-radius: 20px;
      font-size: 0.9rem;
      font-weight: bold;
    }
    
    .pricing-card h3 {
      font-size: 1.6rem;
      margin-top: 0;
      color: #fff;
    }
    
    .price {
      font-size: 2.5rem;
      font-weight: bold;
      margin: 20px 0;
      color: #4b95dd;
    }
    
    .price span {
      font-size: 1rem;
      color: #b0b0b0;
    }
    
    .pricing-features {
      list-style: none;
      padding: 0;
      margin: 0 0 30px;
      text-align: left;
      flex: 1;
    }
    
    .pricing-features li {
      padding: 10px 0;
      border-bottom: 1px solid #3a3a3a;
      display: flex;
      align-items: center;
    }
    
    .pricing-features li::before {
      content: "✓";
      color: #19c37d;
      margin-right: 10px;
      font-weight: bold;
    }
    
    .pricing-features li:last-child {
      border-bottom: none;
    }
    
    /* CTA Section */
    .cta-section {
      padding: 100px 0;
      text-align: center;
      background-color: #2a2a2a;
      position: relative;
      overflow: hidden;
    }
    
    .cta-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0.05;
      background-image: url('/api/placeholder/1200/600');
      background-size: cover;
      background-position: center;
      z-index: 0;
    }
    
    .cta-content {
      position: relative;
      z-index: 1;
    }
    
    .cta-section h2 {
      font-size: 2.5rem;
      margin-bottom: 20px;
      color: #fff;
    }
    
    .cta-section p {
      font-size: 1.2rem;
      margin-bottom: 30px;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
      color: #b0b0b0;
    }
    
    /* Footer */
    footer {
      background-color: #1a1a1a;
      padding: 80px 0 40px;
      color: #b0b0b0;
    }
    
    .footer-content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 40px;
      margin-bottom: 40px;
    }
    
    .footer-column h3 {
      color: #fff;
      margin-top: 0;
      font-size: 1.2rem;
      margin-bottom: 20px;
    }
    
    .footer-column ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    
    .footer-column ul li {
      margin-bottom: 12px;
    }
    
    .footer-column ul li a {
      color: #b0b0b0;
      text-decoration: none;
      transition: color 0.3s;
    }
    
    .footer-column ul li a:hover {
      color: #f5f5f5;
    }
    
    .social-links {
      display: flex;
      gap: 15px;
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
      color: #f5f5f5;
      text-decoration: none;
      transition: background-color 0.3s;
    }
    
    .social-link:hover {
      background-color: #4b95dd;
    }
    
    .copyright {
      text-align: center;
      padding-top: 40px;
      border-top: 1px solid #333;
      color: #777;
      font-size: 0.9rem;
    }
    
    /* Responsive Design */
    @media (max-width: 992px) {
      .methodology-container,
      .demo-container {
        grid-template-columns: 1fr;
      }
      
      .methodology-image {
        order: -1;
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
        align-items: center;
        gap: 10px;
      }
      
      .cta-button, .secondary-button {
        width: 100%;
        max-width: 300px;
        text-align: center;
      }
    }

    /* Simple Popup for Demo */
    .popup {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      justify-content: center;
      align-items: center;
      z-index: 100;
    }
    
    .popup-content {
      background-color: #2a2a2a;
      border-radius: 12px;
      padding: 40px;
      max-width: 500px;
      width: 90%;
      text-align: center;
      position: relative;
    }
    
    .popup-content h2 {
      margin-top: 0;
      color: #fff;
    }
    
    .close-popup {
      position: absolute;
      top: 15px;
      right: 15px;
      background: none;
      border: none;
      color: #b0b0b0;
      font-size: 1.5rem;
      cursor: pointer;
    }
    
    .form-group {
      margin-bottom: 20px;
      text-align: left;
    }
    
    .form-group label {
      display: block;
      margin-bottom: 8px;
      color: #f5f5f5;
    }
    
    .form-group input {
      width: 100%;
      padding: 12px;
      border-radius: 4px;
      border: 1px solid #444;
      background-color: #333;
      color: #fff;
    }
    
    .submit-button {
      background-color: #4b95dd;
      color: white;
      border: none;
      padding: 12px 30px;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
      width: 100%;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="container">
      <nav>
        <div class="logo">
          <div class="logo-icon">S</div>
          SalesTrainer AI
        </div>
        <div class="nav-links">
          <a href="#features">Features</a>
          <a href="#methodology">Methodology</a>
          <a href="#zach-highlights">Highlights</a>
          <a href="#demo">Demo</a>
          <a href="#pricing">Pricing</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>
    </div>
  </header>
  
  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-background"></div>
    <div class="container">
      <div class="hero-content">
        <div class="gpt-badge">Powered by ChatGPT</div>
        <h1>Master the Art of Sales With Our AI-Powered Voice Training</h1>
        <p>Our platform leverages Zach Seager's proven sales methodology and advanced ChatGPT technology to create immersive, audio-based sales simulations that help your team close more deals.</p>
        <div class="buttons">
          <a href="#demo" class="cta-button">Try Interactive Demo</a>
          <a href="https://chatgpt.com/g/g-67be87f079888191bfa2e2dcd1e66771-sales-trainer" class="secondary-button">Use Our ChatGPT Agent</a>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Features Section -->
  <section class="features" id="features">
    <div class="container">
      <h2 class="section-title">Transform Your Sales Team</h2>
      <p class="section-subtitle">Our AI-powered sales training platform combines Zach Seager's expertise with cutting-edge voice technology to deliver personalized, effective training experiences.</p>
      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon">🎙️</div>
          <h3>Voice-Enabled Conversations</h3>
          <p>Practice sales pitches with our AI using your voice for a natural, immersive experience that builds real-world skills.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🧠</div>
          <h3>Powered by ChatGPT</h3>
          <p>Our custom GPT model understands sales psychology and responds naturally with realistic objections and feedback.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">👨‍🏫</div>
          <h3>Zach Seager Methodology</h3>
          <p>Train with proven techniques from sales expert Zach Seager, trusted by top-performing sales professionals.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">📊</div>
          <h3>Performance Analytics</h3>
          <p>Track progress with detailed metrics on win rates, objection handling, and conversation quality.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🎯</div>
          <h3>Industry-Specific Training</h3>
          <p>Customize scenarios to match your specific industry, product, and customer types for targeted development.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">⚡</div>
          <h3>Instant Feedback</h3>
          <p>Receive real-time, actionable suggestions to immediately improve your sales approach.</p>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Methodology Section -->
  <section class="methodology" id="methodology">
    <div class="container">
      <h2 class="section-title">The Zach Seager Sales Methodology</h2>
      <p class="section-subtitle">Built on a framework that has transformed the careers of countless sales professionals, our training is rooted in real-world success.</p>
      <div class="methodology-container">
        <div class="methodology-content">
          <h2>Learn from a Sales Expert</h2>
          <p>Zach Seager's approach blends psychological insights with proven sales techniques. Our AI replicates his authentic coaching to elevate your sales performance.</p>
          <div class="methodology-steps">
            <div class="methodology-step">
              <div class="step-number">1</div>
              <div class="step-content">
                <h4>Discovery Excellence</h4>
                <p>Master the art of asking high-impact questions that reveal customer needs and build rapport.</p>
              </div>
            </div>
            <div class="methodology-step">
              <div class="step-number">2</div>
              <div class="step-content">
                <h4>Objection Navigation</h4>
                <p>Anticipate and address common objections smoothly to keep the conversation moving forward.</p>
              </div>
            </div>
            <div class="methodology-step">
              <div class="step-number">3</div>
              <div class="step-content">
                <h4>Value Articulation</h4>
                <p>Communicate your solution's benefits in clear, compelling terms that resonate with customers.</p>
              </div>
            </div>
            <div class="methodology-step">
              <div class="step-number">4</div>
              <div class="step-content">
                <h4>Strategic Closing</h4>
                <p>Utilize closing techniques that feel natural and boost your conversion rates.</p>
              </div>
            </div>
          </div>
        </div>
        <div class="methodology-image">
          <img src="/api/placeholder/500/400" alt="Zach Seager Sales Methodology" />
        </div>
      </div>
    </div>
  </section>
  
  <!-- Zach Seager Highlights Section -->
  <section class="zach-highlights" id="zach-highlights">
    <div class="container">
      <h2 class="section-title">Zach Seager Highlights</h2>
      <p class="section-subtitle">Listen to key insights from Zach Seager's industry record. Discover proven strategies that have transformed sales teams.</p>
      <div class="audio-player">
        <audio controls>
          <source src="ytapi.org - Ep. 4 Zach Seager Industry Record Pest Control D2D (1).mp3" type="audio/mpeg">
          Your browser does not support the audio element.
        </audio>
      </div>
      <div class="highlights-text">
        <ul>
          <li><strong>Insight 1:</strong> [Insert highlight text here]</li>
          <li><strong>Insight 2:</strong> [Insert highlight text here]</li>
          <li><strong>Insight 3:</strong> [Insert highlight text here]</li>
        </ul>
      </div>
    </div>
  </section>
  
  <!-- Audio Demo Section -->
  <section class="audio-demo" id="demo">
    <div class="container">
      <h2 class="section-title">Experience Voice-Enabled Training</h2>
      <p class="section-subtitle">Try our interactive voice demo to see how our AI responds naturally to your sales pitch and provides real-time feedback.</p>
      <div class="demo-container">
        <div class="demo-content">
          <h3>Sample Training Scenario: Enterprise Software Sale</h3>
          <p>In this simulation, you speak with a potential client considering an upgrade to their CRM system. Practice your pitch and handle objections using your voice or text input.</p>
          <p><strong>Instructions:</strong> Click the microphone button to start speaking, or type your response below.</p>
        </div>
        <div class="audio-player">
          <h3>Voice Interaction Demo</h3>
          <div class="audio-progress">
            <div class="progress-bar"></div>
          </div>
          <div class="audio-controls">
            <button class="control-button">▶️</button>
            <div class="time-display">01:23 / 03:45</div>
          </div>
          <div class="chat-interface" style="height: 300px; margin-top: 20px;">
            <div class="chat-messages">
              <div class="message ai-message">
                Hi there! I'm considering upgrading our CRM system. What can you tell me about your solution?
              </div>
              <div class="message user-message">
                I appreciate your interest. Our platform combines voice-enabled interactions with AI coaching based on proven sales techniques.
              </div>
            </div>
            <div class="chat-input">
              <input type="text" placeholder="Type your message..." id="demo-input">
              <button onclick="simulateResponse()">Send</button>
              <button onclick="startVoiceRecognition()" class="mic-button">🎤</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <!-- Pricing Section -->
  <section class="pricing" id="pricing">
    <div class="container">
      <h2 class="section-title">Pricing Plans</h2>
      <div class="pricing-cards">
        <div class="pricing-card">
          <h3>Starter</h3>
          <div class="price">$199<span>/month</span></div>
          <ul class="pricing-features">
            <li>Up to 5 users</li>
            <li>10 pre-built scenarios</li>
            <li>Basic analytics</li>
            <li>Email support</li>
          </ul>
          <a href="#" class="cta-button" onclick="showSignup(event)">Get Started</a>
        </div>
        <div class="pricing-card popular">
          <div class="popular-tag">Most Popular</div>
          <h3>Professional</h3>
          <div class="price">$399<span>/month</span></div>
          <ul class="pricing-features">
            <li>Up to 20 users</li>
            <li>25 pre-built scenarios</li>
            <li>Custom scenario creation</li>
            <li>Advanced analytics</li>
            <li>Priority support</li>
          </ul>
          <a href="#" class="cta-button" onclick="showSignup(event)">Get Started</a>
        </div>
        <div class="pricing-card">
          <h3>Enterprise</h3>
          <div class="price">Custom</div>
          <ul class="pricing-features">
            <li>Unlimited users</li>
            <li>Unlimited scenarios</li>
            <li>Custom integrations</li>
            <li>White-labeling</li>
            <li>Dedicated support</li>
            <li>On-premise deployment</li>
          </ul>
          <a href="#" class="cta-button" onclick="showSignup(event)">Contact Us</a>
        </div>
      </div>
    </div>
  </section>
  
  <!-- CTA / Contact Section -->
  <section class="cta-section" id="contact">
    <div class="cta-background"></div>
    <div class="container cta-content">
      <h2>Ready to Transform Your Sales Team?</h2>
      <p>Join hundreds of companies already boosting their sales performance with SalesTrainer AI.</p>
      <a href="#" class="cta-button" onclick="showSignup(event)">Get Started Today</a>
    </div>
  </section>
  
  <!-- Footer -->
  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="footer-column">
          <h3>SalesTrainer AI</h3>
          <p>The ultimate AI-powered sales training platform to help your team master the art of selling.</p>
        </div>
        <div class="footer-column">
          <h3>Quick Links</h3>
          <ul>
            <li><a href="#features">Features</a></li>
            <li><a href="#methodology">Methodology</a></li>
            <li><a href="#zach-highlights">Highlights</a></li>
            <li><a href="#demo">Demo</a></li>
            <li><a href="#pricing">Pricing</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>Resources</h3>
          <ul>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Knowledge Base</a></li>
            <li><a href="#">Case Studies</a></li>
            <li><a href="#">Webinars</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>Contact Us</h3>
          <ul>
            <li><a href="mailto:info@salestrainerai.com">info@salestrainerai.com</a></li>
            <li><a href="tel:+15551234567">+1 (555) 123-4567</a></li>
          </ul>
        </div>
      </div>
      <div class="copyright">
        <p>&copy; 2025 SalesTrainer AI. All rights reserved.</p>
      </div>
    </div>
  </footer>
  
  <!-- Popup for Signup (Demo) -->
  <div class="popup" id="signup-popup">
    <div class="popup-content">
      <h2>Coming Soon!</h2>
      <p>This is a demonstration website. In a real implementation, this would connect to a sign-up form or contact system.</p>
      <button class="close-popup" onclick="closePopup()">Close</button>
    </div>
  </div>
  
  <script>
    // Function to simulate chat responses in the demo
    function simulateResponse() {
      const input = document.getElementById('demo-input');
      if (input.value.trim() === '') return;
      
      const chatMessages = document.querySelector('.chat-messages');
      const userMessage = document.createElement('div');
      userMessage.className = 'message user-message';
      userMessage.textContent = input.value;
      chatMessages.appendChild(userMessage);
      
      input.value = '';
      chatMessages.scrollTop = chatMessages.scrollHeight;
      
      setTimeout(() => {
        const aiResponses = [
          "That's an interesting point. Can you elaborate?",
          "I see, but what about your pricing?",
          "I appreciate your explanation. Can we schedule a demo?",
          "I'm not sure; could you tell me more about the benefits?",
          "Let me think about that and get back to you."
        ];
        const randomResponse = aiResponses[Math.floor(Math.random() * aiResponses.length)];
        const aiMessage = document.createElement('div');
        aiMessage.className = 'message ai-message';
        aiMessage.textContent = randomResponse;
        chatMessages.appendChild(aiMessage);
        chatMessages.scrollTop = chatMessages.scrollHeight;
      }, 1000);
    }
    
    // Voice recognition using the Web Speech API
    function startVoiceRecognition() {
      if (!('webkitSpeechRecognition' in window) && !('SpeechRecognition' in window)) {
        alert("Your browser does not support voice recognition.");
        return;
      }
      const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
      const recognition = new SpeechRecognition();
      recognition.lang = 'en-US';
      recognition.interimResults = false;
      recognition.maxAlternatives = 1;
      recognition.start();
      
      recognition.onresult = function(event) {
        const transcript = event.results[0][0].transcript;
        document.getElementById('demo-input').value = transcript;
      };
      
      recognition.onerror = function(event) {
        console.error("Speech recognition error", event.error);
      };
    }
    
    // Show signup popup (demo only)
    function showSignup(event) {
      event.preventDefault();
      document.getElementById('signup-popup').style.display = 'flex';
    }
    
    function closePopup() {
      document.getElementById('signup-popup').style.display = 'none';
    }
    
    // Allow Enter key to send chat messages
    document.getElementById('demo-input').addEventListener('keypress', function(e) {
      if (e.key === 'Enter') {
        simulateResponse();
      }
    });
  </script>
</body>
</html>
