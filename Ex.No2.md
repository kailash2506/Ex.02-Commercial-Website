# Ex02 Commercial Website
## Date: 29-08-2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multiplex Signs | Chennai Signboard Experts</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    /* ===== General Reset ===== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      background-color: #f8f9fa;
    }

    /* ===== Header ===== */
    header {
      background: #222;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px 20px;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    header .logo-title {
      display: flex;
      align-items: center;
    }
    header .logo-img {
      height: 50px;
      margin-right: 10px;
    }
    header nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      transition: color 0.3s;
    }
    header nav a:hover {
      color: #FFD700;
    }
    .site-title {
      color: #FFF7B2;
      font-family: 'Poppins', Arial, sans-serif;
      font-size: 1.8rem;
      font-weight: 600;
    }

    /* ===== Hero Section ===== */
    .hero {
      background: #facc15; /* Bright yellow background */
      color: #1f2937; /* Dark text for contrast */
      text-align: center;
      padding: 80px 20px;
    }
    .hero h1 {
      font-size: 2.5em;
      font-family: 'Poppins', sans-serif;
      font-weight: 600;
    }
    .hero p {
      max-width: 700px;
      margin: 10px auto 20px;
    }
    .btn {
      background: #1f2937; /* Dark button */
      color: white;
      padding: 12px 24px;
      text-decoration: none;
      font-weight: bold;
      border-radius: 5px;
      transition: background 0.3s;
    }
    .btn:hover {
      background: #374151;
    }

    section {
      padding: 60px 20px;
      text-align: center;
    }
    
    section:nth-of-type(odd) {
        background-color: #fff;
    }

    section h2 {
      font-size: 2.2rem;
      font-family: 'Poppins', sans-serif;
      color: #2b3a4a;
      margin-bottom: 40px;
    }

    .card-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 25px;
    }

    /* Service Cards */
    .service-card {
      background-color: #ffffff;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.08);
      width: 220px;
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      overflow: hidden;
    }
    .service-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 25px rgba(0,0,0,0.12);
    }
    .service-card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
    }
    .service-card-content {
        padding: 20px;
    }
    .service-card h3 {
        margin-bottom: 8px;
        color: #333;
    }
    .service-card p {
        font-size: 0.9rem;
        color: #666;
    }

    /* Client Cards */
    .client-card {
        background-color: #ffffff;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0,0,0,0.05);
        padding: 15px;
        width: 200px;
        height: 120px;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: transform 0.2s ease;
    }
    .client-card:hover {
        transform: translateY(-5px);
    }
    .client-card img {
        max-width: 100%;
        max-height: 100%;
        object-fit: contain;
    }

    /* ===== About Us ===== */
    #about {
      padding: 60px 20px;
      background: #fffde9; /* softer yellow */
    }
    #about p {
      font-size: 1.1rem;
      color: #333;
      margin-bottom: 18px;
      max-width: 650px;
      margin-left: auto;
      margin-right: auto;
      line-height: 1.7;
    }
    #about ul {
      display: inline-block;
      text-align: left;
      margin-top: 10px;
      padding-left: 24px;
      list-style-type: '✓  ';
    }
    #about li {
      margin-bottom: 8px;
      font-size: 1.05rem;
      color: #222;
    }

    /* ===== Contact Section ===== */
    #contact {
      background: #f8f6ec;
      padding-bottom: 40px;
    }
    .branches {
      display: flex;
      gap: 20px;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 30px;
    }
    .branch {
      background: #fff9d7;
      border-radius: 10px;
      padding: 20px;
      width: 350px;
      box-shadow: 0 2px 5px rgba(255, 225, 134, 0.32);
    }
    .branch h3 {
      color: #a68900;
      margin-bottom: 8px;
    }
    .contact-details {
      display: flex;
      gap: 15px;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 8px;
    }
    .contact-details div {
      background: #fff8e1;
      padding: 12px 20px;
      border-radius: 8px;
      font-size: 1.01em;
    }
    .contact-details a {
      color: #36415a;
      text-decoration: none;
    }
     .contact-details a:hover {
      text-decoration: underline;
    }

    /* ===== Footer ===== */
    footer {
      background-color: #36415a;
      color: white;
      text-align: center;
      padding: 30px 10px;
      line-height: 1.7;
      font-family: 'Poppins', Arial, sans-serif;
    }
    footer p {
      margin: 6px 0;
    }
    .social-links a {
      color: #FFD700;
      text-decoration: none;
      font-weight: 500;
      margin: 0 8px;
    }
    .social-links a:hover {
      color: #fff;
      text-decoration: underline;
    }

    /* ===== Media Queries for Responsiveness ===== */
    @media (max-width: 820px) {
        header {
            flex-direction: column;
            gap: 10px;
        }
        .branches, .contact-details {
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }
        .branch {
            width: 80%;
        }
    }
    @media (max-width: 510px) {
        .hero h1 { font-size: 1.8rem; }
        .site-title { font-size: 1.5rem; }
        header nav { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; }
        header nav a { margin-left: 10px; }
        .service-card { width: 80vw; }
        .client-card { width: 60vw; }
        .branch { width: 90vw; }
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <header>
    <div class="logo-title">
      <img src="https://placehold.co/150x50/222222/FFF7B2?text=Multiplex" alt="Multiplex Signs Logo" class="logo-img">
      <span class="site-title">Multiplex Signs</span>
    </div>
    <nav>
      <a href="#home">Home</a>
      <a href="#services">Our Services</a>
      <a href="#about">About Us</a>
      <a href="#clients">Clients</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- HERO / HOME SECTION -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Creating Eye-Catching Signboards for Every Business</h1>
      <p>Multiplex established in 2000. Chennai's trusted experts for all kinds of signage—quality, creativity, competitive rates, own designing and fabrication units.</p>
      <a href="#contact" class="btn">Get A Free Quote</a>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services">
    <h2>Our Services</h2>
    <div class="card-container">
      <div class="service-card">
        <img src="https://placehold.co/400x300/eab308/ffffff?text=LED+Boards" alt="LED Boards">
        <div class="service-card-content">
          <h3>LED Boards</h3>
          <p>Bright and durable boards for high visibility.</p>
        </div>
      </div>
      <div class="service-card">
        <img src="https://placehold.co/400x300/475569/ffffff?text=ACP+Boards" alt="ACP Boards">
        <div class="service-card-content">
            <h3>ACP Boards</h3>
            <p>Modern Aluminum Composite Panels for signage.</p>
        </div>
      </div>
      <div class="service-card">
        <img src="https://placehold.co/400x300/f97316/ffffff?text=Letters" alt="Letters">
        <div class="service-card-content">
            <h3>Letters</h3>
            <p>Custom cut acrylic and metal letters for branding.</p>
        </div>
      </div>
      <div class="service-card">
        <img src="https://placehold.co/400x300/0ea5e9/ffffff?text=Glow+Sign" alt="Glow Signage">
        <div class="service-card-content">
            <h3>Glow Signage</h3>
            <p>Illuminated boards that shine night and day!</p>
        </div>
      </div>
      <div class="service-card">
        <img src="https://placehold.co/400x300/84cc16/ffffff?text=Non-Lit" alt="Non Lit Signage">
        <div class="service-card-content">
            <h3>Non Lit Signage</h3>
            <p>Elegant boards for indoor & outdoor use.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Clients Section -->
  <section id="clients" class="clients">
    <h2>Our Clients</h2>
    <div class="card-container">
        <div class="client-card">
            <img src="https://placehold.co/200x100/f3f4f6/6b7280?text=Client+A" alt="Client A">
        </div>
        <div class="client-card">
            <img src="https://placehold.co/200x100/f3f4f6/6b7280?text=Client+B" alt="Client B">
        </div>
        <div class="client-card">
            <img src="https://placehold.co/200x100/f3f4f6/6b7280?text=Client+C" alt="Client C">
        </div>
        <div class="client-card">
            <img src="https://placehold.co/200x100/f3f4f6/6b7280?text=Client+D" alt="Client D">
        </div>
    </div>
  </section>
  
  <!-- About Us Section -->
  <section id="about" class="order">
    <h2>About Us</h2>
    <p>
      Multiplex was established in 2000 and we specialize in all kinds of signage.<br>
      We have our own Designing Unit, Fabrication Unit, and state-of-the-art Machineries.<br>
      We are committed to delivering the best quality at competitive rates.
    </p>
    <ul>
      <li>Own designing & fabrication units</li>
      <li>Expert team & advanced equipment</li>
      <li>Trusted by Chennai's leading brands</li>
    </ul>
  </section>
  
  <!-- Contact Section -->
  <section id="contact" class="menu">
    <h2>Contact Us</h2>
    <div class="branches">
      <div class="branch">
        <h3>Mount Road</h3>
        <p>New No.27, Old No.14, Thayar Sahib Street,<br>
        Chennai – 600 002.<br>
        (1st Left of G.P. Road) (Near Ellis Road)</p>
      </div>
      <div class="branch">
        <h3>Iyyappanthangal</h3>
        <p>No. 81, Mount Poonamallee Road,<br>
        Iyyappanthangal, Chennai – 600 056.<br>
        (Opp To Porur Sri Ramachandra Hospital)</p>
      </div>
    </div>
    <div class="contact-details">
      <div>
        <strong>📞 Phone:</strong> <a href="tel:9840084893">9840084893</a>, <a href="tel:9841684803">9841684803</a>
      </div>
      <div>
        <strong>📧 Email:</strong> <a href="mailto:multiplexsignage@yahoo.com">multiplexsignage@yahoo.com</a>
      </div>
      <div>
        <strong>💳 GPay:</strong> MULTIPLEX (8838392510@okbizaxis)
      </div>
    </div>
  </section>
  
  <!-- Footer -->
  <footer>
    <p>© 2025 Multiplex Signs | All Rights Reserved</p>
    <p>Designed by Kailash Kumar S</p>
    <div class="social-links">
      <a href="#">Facebook</a> | 
      <a href="#">Instagram</a> | 
      <a href="https://api.whatsapp.com/send?phone=919840084893" target="_blank">WhatsApp</a>
    </div>
  </footer>
</body>
</html>


```

## OUTPUT
![alt text](<Screenshot 2025-09-10 151654.png>)
![alt text](<Screenshot 2025-09-10 151712.png>)
![alt text](<Screenshot 2025-09-10 151728.png>)

## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
