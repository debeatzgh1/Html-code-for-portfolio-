
<!-- ✅ Carousel Wrapper -->
<div class="carousel-container" id="carousel">
  <!-- ✅ Slides -->
  <div class="slide active">
    <h2>👋 Welcome to My AI Project Portfolio</h2>
    <p>Explore AI-powered tools and innovations built to empower creators, solopreneurs, and startups. Swipe or tap arrows to begin.</p>
  </div>

  <div class="slide">
    <h2>📱 Android AI Explorer</h2>
    <p>Smart mobile app with built-in AI voice recognition, task automation, and intelligent suggestions for digital growth.</p>
    <p><a href="https://github.com/debeatzgh1/Explore-my-Android-project-" target="_blank">🔗 View Android AI Explorer</a></p>
  </div>

  <div class="slide">
    <h2>🌐 AI Productivity Web App</h2>
    <p>A modern web platform offering carefully curated AI tools, automated workflows, and prompt generators for maximum productivity.</p>
    <p><a href="https://github.com/debeatzgh1/Improve-productivity-with-AI-Web-App-project-" target="_blank">🔗 View Web App</a></p>
  </div>

  <div class="slide">
    <h2>🧠 TechAdapt Toolkit</h2>
    <p>Comprehensive resource hub: startup automation templates, prompt libraries, AI courses, and monetization guides.</p>
    <p><a href="https://github.com/debeatzgh1/TechAdapt-Solutions-Strategies-for-Modern-Startups-and-Individuals" target="_blank">🔗 View TechAdapt Toolkit</a></p>
  </div>

  <div class="slide">
    <h2>💼 AI Side Hustle Assistant</h2>
    <p>Turn ideas into income with our prompt-based assistant that helps you launch, test, and automate side hustles online.</p>
    <p><a href="https://github.com/debeatzgh1/AI-side-hustle-Assistant-" target="_blank">🔗 View AI Hustle Assistant</a></p>
  </div>

  <div class="slide">
    <h2>📋 Prompt Sample Showcase</h2>
    <p>Discover prompt examples and resources powering these tools.</p>
    <p><a href="https://gist.github.com/98cf571e21881f4a39560503988861d3" target="_blank">🔗 Explore Prompt Gist</a></p>
  </div>

  <div class="slide">
    <h2>📬 Contact Me</h2>
    <p>Want to collaborate or ask a question? Fill out the form below. I’ll get back to you soon!</p>
    <div class="form-frame">
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSfBDlR6TcU9sWjbeVOp6dtb4GMKdL6SP_i0KB08IrtbLT9wwA/viewform?embedded=true" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
    </div>
  </div>

  <!-- ✅ Arrows -->
  <div class="carousel-nav">
    <button class="arrow left" onclick="prevSlide()">&#10094;</button>
    <button class="arrow right" onclick="nextSlide()">&#10095;</button>
  </div>
</div>

<!-- ✅ Styles -->
<style>
  .carousel-container {
    position: relative;
    max-width: 800px;
    margin: 30px auto;
    background: #fff;
    border-radius: 16px;
    box-shadow: 0 8px 30px rgba(0,0,0,0.1);
    overflow: hidden;
    padding: 30px 20px;
    font-family: 'Segoe UI', sans-serif;
  }

  .slide {
    display: none;
    opacity: 0;
    transition: opacity 0.6s ease;
  }

  .slide.active {
    display: block;
    opacity: 1;
  }

  .slide h2 {
    font-size: 1.5rem;
    color: #333;
    margin-bottom: 10px;
  }

  .slide p {
    font-size: 1rem;
    color: #555;
    line-height: 1.6;
  }

  .slide a {
    color: #1a73e8;
    text-decoration: none;
    font-weight: bold;
  }

  .slide a:hover {
    text-decoration: underline;
  }

  .carousel-nav {
    position: absolute;
    top: 50%;
    width: 100%;
    display: flex;
    justify-content: space-between;
    transform: translateY(-50%);
    pointer-events: none;
  }

  .arrow {
    pointer-events: auto;
    background: #222;
    color: #fff;
    border: none;
    font-size: 22px;
    padding: 10px 16px;
    border-radius: 50%;
    cursor: pointer;
    transition: background 0.3s ease;
  }

  .arrow:hover {
    background: #000;
  }

  .form-frame {
    margin-top: 15px;
    width: 100%;
    max-width: 100%;
    height: 520px;
  }

  .form-frame iframe {
    width: 100%;
    height: 100%;
    border: none;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  }

  @media (max-width: 768px) {
    .carousel-container {
      padding: 20px 15px;
    }

    .arrow {
      padding: 8px 12px;
      font-size: 20px;
    }

    .slide h2 {
      font-size: 1.3rem;
    }

    .slide p {
      font-size: 0.95rem;
    }
  }
</style>

<!-- ✅ Script -->
<script>
  let currentSlide = 0;
  let slides;

  document.addEventListener("DOMContentLoaded", function () {
    slides = document.querySelectorAll(".slide");
    showSlide(currentSlide);

    const carousel = document.getElementById("carousel");
    let startX = 0;

    carousel.addEventListener("touchstart", function (e) {
      startX = e.touches[0].clientX;
    });

    carousel.addEventListener("touchend", function (e) {
      let diff = e.changedTouches[0].clientX - startX;
      if (diff > 50) prevSlide();
      else if (diff < -50) nextSlide();
    });

    setInterval(nextSlide, 5000); // Auto-slide every 5s
  });

  function showSlide(index) {
    slides.forEach((slide, i) => {
      slide.classList.toggle("active", i === index);
    });
  }

  function nextSlide() {
    currentSlide = (currentSlide + 1) % slides.length;
    showSlide(currentSlide);
  }

  function prevSlide() {
    currentSlide = (currentSlide - 1 + slides.length) % slides.length;
    showSlide(currentSlide);
  }
</script>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Projects</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Font Awesome for GitHub icon -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      margin: 0;
      padding: 0;
    }

    .view-projects-container {
      text-align: center;
      margin: 40px 0;
    }

    .view-projects-btn {
      display: inline-block;
      padding: 14px 32px;
      font-size: 1.1rem;
      font-weight: bold;
      color: #ffffff;
      background-color: #007bff;
      border-radius: 8px;
      text-decoration: none;
      box-shadow: 0 4px 12px rgba(0, 123, 255, 0.2);
      transition: background-color 0.3s ease, transform 0.2s ease;
    }

    .view-projects-btn i {
      margin-right: 10px;
    }

    .view-projects-btn:hover {
      background-color: #0056b3;
      transform: translateY(-2px);
    }

    /* Modal Styling */
    .modal {
      display: none;
      position: fixed;
      z-index: 9999;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow-y: auto;
      background-color: rgba(0, 0, 0, 0.8);
      animation: fadeIn 0.3s ease-in-out;
    }

    .modal-content {
      background-color: #fff;
      margin: 60px auto;
      padding: 30px;
      max-width: 900px;
      border-radius: 12px;
      position: relative;
    }

    .close-btn {
      position: absolute;
      top: 16px;
      right: 20px;
      font-size: 24px;
      color: #333;
      cursor: pointer;
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .project-card {
      background: #fff;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
      animation: slideUp 0.6s ease-in-out forwards;
      opacity: 0;
    }

    .project-card img {
      width: 100%;
      height: 140px;
      object-fit: cover;
    }

    .project-card h3 {
      padding: 10px;
      margin: 0;
      font-size: 1rem;
    }

    .card-buttons {
      display: flex;
      justify-content: center;
      gap: 10px;
      padding: 10px;
    }

    .card-btn {
      padding: 8px 14px;
      border-radius: 6px;
      background-color: #007bff;
      color: #fff;
      font-weight: 500;
      text-decoration: none;
      transition: background-color 0.3s;
      font-size: 0.85rem;
    }

    .card-btn.live {
      background-color: #28a745;
    }

    .card-btn:hover {
      opacity: 0.85;
    }

    @keyframes slideUp {
      0% { opacity: 0; transform: translateY(40px); }
      100% { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
  </style>
</head>
<body>

  <!-- View Button -->
  <div class="view-projects-container">
    <a href="#" class="view-projects-btn" onclick="openModal()">
      <i class="fab fa-github"></i> View All Projects
    </a>
  </div>

  <!-- Modal -->
  <div id="projectModal" class="modal">
    <div class="modal-content">
      <span class="close-btn" onclick="closeModal()">&times;</span>
      <h2>My Featured Projects</h2>
      <div class="project-grid">

        <!-- Project 1 -->
        <div class="project-card">
          <img src="https://raw.githubusercontent.com/debeatzgh1/TechAdapt-Solutions-Strategies-for-Modern-Startups-and-Individuals/main/preview.jpg" alt="TechAdapt" />
          <h3>TechAdapt Solutions</h3>
          <div class="card-buttons">
            <a href="https://github.com/debeatzgh1/TechAdapt-Solutions-Strategies-for-Modern-Startups-and-Individuals" target="_blank" class="card-btn">GitHub</a>
            <a href="https://debeatzgh1.github.io/TechAdapt-Solutions-Strategies-for-Modern-Startups-and-Individuals/" target="_blank" class="card-btn live">Live Preview</a>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
          <img src="https://raw.githubusercontent.com/debeatzgh1/Improve-productivity-with-AI-Web-App-project-/main/preview.jpg" alt="AI Productivity" />
          <h3>AI Productivity App</h3>
          <div class="card-buttons">
            <a href="https://github.com/debeatzgh1/Improve-productivity-with-AI-Web-App-project-" target="_blank" class="card-btn">GitHub</a>
            <a href="https://debeatzgh1.github.io/Improve-productivity-with-AI-Web-App-project-/" target="_blank" class="card-btn live">Live Preview</a>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
          <img src="https://raw.githubusercontent.com/debeatzgh1/Explore-my-Android-project-/main/preview.jpg" alt="Android Project" />
          <h3>Android AI Explorer</h3>
          <div class="card-buttons">
            <a href="https://github.com/debeatzgh1/Explore-my-Android-project-" target="_blank" class="card-btn">GitHub</a>
            <a href="https://debeatzgh1.github.io/Explore-my-Android-project-/" target="_blank" class="card-btn live">Live Preview</a>
          </div>
        </div>

        <!-- Project 4 -->
        <div class="project-card">
          <img src="https://raw.githubusercontent.com/debeatzgh1/AI-side-hustle-Assistant-/main/preview.jpg" alt="AI Assistant" />
          <h3>AI Side Hustle Assistant</h3>
          <div class="card-buttons">
            <a href="https://github.com/debeatzgh1/AI-side-hustle-Assistant-" target="_blank" class="card-btn">GitHub</a>
            <a href="https://debeatzgh1.github.io/AI-side-hustle-Assistant-/" target="_blank" class="card-btn live">Live Preview</a>
          </div>
        </div>

        <!-- Project 5 -->
        <div class="project-card">
          <img src="https://via.placeholder.com/400x200?text=Gist+Preview" alt="Business Gist" />
          <h3>Business Strategy Gist</h3>
          <div class="card-buttons">
            <a href="https://gist.github.com/98cf571e21881f4a39560503988861d3" target="_blank" class="card-btn">GitHub</a>
            <a href="https://gist.github.com/98cf571e21881f4a39560503988861d3" target="_blank" class="card-btn live">Live Gist</a>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- JavaScript to toggle modal -->
  <script>
    function openModal() {
      document.getElementById('projectModal').style.display = 'block';
    }

    function closeModal() {
      document.getElementById('projectModal').style.display = 'none';
    }

    // Animate each project card after modal opens
    document.getElementById('projectModal').addEventListener('transitionend', () => {
      const cards = document.querySelectorAll('.project-card');
      cards.forEach((card, i) => {
        setTimeout(() => card.style.opacity = 1, i * 100);
      });
    });
  </script>
</body>
</html>
<!-- ✅ Simple Catalog Card for Blogger -->
<div style="max-width: 600px; margin: 20px auto; font-family: Arial, sans-serif; border-radius: 12px; overflow: hidden; box-shadow: 0 4px 10px rgba(0,0,0,0.1); background: #fff;">
  
  <!-- Thumbnail Image -->
  <img src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/07/amoderncleanworkspaceshowcasingfront-endcodesnippetsonasleeklaptopscreensurroundedbytailwindcsslogoshtml5andfirebaseicons5315964892159237038.jpg" alt="HTML Template Thumbnail" style="width: 100%; display: block;">

  <!-- Content -->
  <div style="padding: 20px;">
    <h2 style="font-size: 20px; color: #1f2937; margin-bottom: 10px;">Firebase Curated Front-End Components with HTML, Tailwind CSS & Firebase for Modern Creators</h2>
    <p style="font-size: 14px; color: #4b5563; margin-bottom: 20px;">Discover a collection of responsive, production-ready UI components built with HTML5, Tailwind CSS, and Firebase. Designed for bloggers, developers, and solopreneurs seeking sleek, minimal design with maximum efficiency.  </p>

    <!-- GitHub Action Button -->
    <a href="https://github.com/debeatzgh1/Blogger-sign-up-button-" target="_blank" style="display: inline-block; text-decoration: none; background: #3b82f6; color: #fff; padding: 10px 18px; border-radius: 8px; font-weight: bold; font-size: 14px;">
      🔧 View & Edit on GitHub
    </a>
  </div>
</div>

<!-- Floating Menu Button with Modals: Place in HTML/JavaScript widget on Blogger for site-wide use -->
<style>
  #floatingMenu {
    position: fixed;
    top: 50%;
    right: 20px;
    transform: translateY(-50%);
    z-index: 9999;
  }
  .menu-btn {
    background: #0057ff;
    color: white;
    border: none;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    font-size: 28px;
    cursor: pointer;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    transition: background 0.3s ease;
  }
  .menu-btn:hover {
    background: #003db3;
  }
  .icon-menu {
    display: none;
    flex-direction: column;
    align-items: flex-end;
    margin-bottom: 10px;
  }
  .icon-menu a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: #333;
    background: white;
    padding: 10px 14px;
    margin: 5px 0;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: background 0.3s;
    width: 240px;
    cursor: pointer;
  }
  .icon-menu a:hover {
    background: #e0e0ff;
  }
  .icon-menu i {
    font-size: 20px;
    margin-right: 10px;
  }
  .custom-modal {
    display: none;
    position: fixed;
    z-index: 10000;
    left: 0;
    top: 0;
    width: 100vw;
    height: 100vh;
    overflow: auto;
    background: rgba(0,0,0,0.4);
    justify-content: center;
    align-items: center;
  }
  .custom-modal .modal-content {
    background: #fff;
    margin: 60px auto;
    padding: 30px 20px;
    border-radius: 12px;
    max-width: 600px;
    box-shadow: 0 2px 10px #bbb;
    position: relative;
    animation: fadeIn 0.4s;
    font-size: 1.07em;
  }
  @keyframes fadeIn {
    from {transform:translateY(30px); opacity:0;}
    to {transform:translateY(0); opacity:1;}
  }
  .custom-modal .close {
    position: absolute;
    top: 12px;
    right: 18px;
    font-size: 28px;
    color: #333;
    cursor: pointer;
  }
  .custom-modal h2 {
    color: #1976d2;
    text-align: center;
    margin-bottom: 22px;
  }
  .custom-modal a { color: #1976d2; word-break: break-all;}
  @media (max-width: 700px) {
    .custom-modal .modal-content { max-width: 97vw; }
    .icon-menu a { width: 90vw; }
  }
</style>
<!-- Font Awesome (for icons) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>
<div id="floatingMenu">
  <div class="icon-menu" id="iconLinks">
    <a onclick="openModal('aboutModal')"><i class="fas fa-user"></i> About Us</a>
    <a onclick="openModal('contactModal')"><i class="fas fa-envelope"></i> Contact</a>
    <a onclick="openModal('toolsModal')"><i class="fas fa-toolbox"></i> Tools & Widgets</a>
    <a onclick="openModal('privacyModal')"><i class="fas fa-shield-alt"></i> Privacy Policy</a>
    <a onclick="openModal('termsModal')"><i class="fas fa-file-contract"></i> Terms of Use</a>
    <a onclick="openModal('resourcesModal')"><i class="fas fa-book-open"></i> Resources</a>
    <a onclick="openModal('faqModal')"><i class="fas fa-question-circle"></i> FAQs</a>
    <a onclick="openModal('aiModal')"><i class="fas fa-robot"></i> AI Articles</a>
    <a onclick="openModal('galleryModal')"><i class="fas fa-images"></i> Gallery</a>
  </div>
  <button class="menu-btn" onclick="toggleMenu()">
    <i class="fas fa-bars"></i>
  </button>
</div>
<!-- About Modal -->
<div id="aboutModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('aboutModal')">&times;</span>
    <h2>About Us</h2>
    <p><strong>debeatzgh1</strong> is a passionate developer, designer, and content creator dedicated to empowering creators and entrepreneurs through open-source tools, digital products, and educational content. Across multiple platforms (GitHub and Blogger), debeatzgh1 shares curated front-end components, productivity resources, and guides for web development, AI, and digital business growth.</p>
  </div>
</div>
<!-- Contact Modal -->
<div id="contactModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('contactModal')">&times;</span>
    <h2>Contact</h2>
    <p>You can connect via:</p>
    <ul>
      <li><a href="https://github.com/debeatzgh1" target="_blank">GitHub Profile</a></li>
      <li><a href="https://beatzde4.blogspot.com/p/contact.html" target="_blank">Beatzde4 Blog Contact</a></li>
      <li>Email: <a href="mailto:your@email.com">Use blog contact form</a></li>
    </ul>
  </div>
</div>
<!-- Tools & Widgets Modal -->
<div id="toolsModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('toolsModal')">&times;</span>
    <h2>Tools & Widgets</h2>
    <ul>
      <li><a href="https://github.com/debeatzgh1/firebase-front-end-components" target="_blank">Firebase Front-End Components</a>: Reusable UI components, HTML/CSS/JS, and Python resources.</li>
      <li><a href="https://beatzde4.blogspot.com/p/tools.html" target="_blank">Beatzde4 Blog Tools</a>: Widgets, templates, and utilities for bloggers and creators.</li>
    </ul>
  </div>
</div>
<!-- Privacy Policy Modal -->
<div id="privacyModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('privacyModal')">&times;</span>
    <h2>Privacy Policy</h2>
    <p>Your privacy matters! We use cookies and analytics to enhance your experience. No personal data is shared or sold. For details, visit:</p>
    <ul>
      <li><a href="https://beatzde4.blogspot.com/p/privacy-policy.html" target="_blank">Beatzde4 Blog Privacy Policy</a></li>
      <li><a href="https://appdategh1.blogspot.com/p/privacy-policy.html" target="_blank">AppdateGH Privacy Policy</a></li>
    </ul>
  </div>
</div>
<!-- Terms of Use Modal -->
<div id="termsModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('termsModal')">&times;</span>
    <h2>Terms of Use</h2>
    <p>By using our tools, templates, and content, you agree to use them for lawful and ethical purposes. Please credit the author when using open-source code. See the full terms:</p>
    <ul>
      <li><a href="https://beatzde4.blogspot.com/p/terms.html" target="_blank">Beatzde4 Blog Terms</a></li>
    </ul>
  </div>
</div>
<!-- Resources Modal -->
<div id="resourcesModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('resourcesModal')">&times;</span>
    <h2>Resources</h2>
    <ul>
      <li><a href="https://beatzde4.blogspot.com/p/firebase-curated-front-end-components.html" target="_blank">Firebase Curated Front-End Components</a></li>
      <li><a href="https://mybrandsonline.blogspot.com/" target="_blank">MyBrandsOnline Blog</a>: Branding advice and online business tips.</li>
      <li><a href="http://digimartgh.blogspot.com/" target="_blank">DigimartGH</a>: Digital marketing, business tools, and guides.</li>
    </ul>
  </div>
</div>
<!-- FAQs Modal -->
<div id="faqModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('faqModal')">&times;</span>
    <h2>Frequently Asked Questions</h2>
    <details>
      <summary>Who is debeatzgh1?</summary>
      <div>
        <p>debeatzgh1 is a developer, designer, and content creator focused on building modern web apps, sharing productivity tools, and providing digital solutions. Find my projects on <a href="https://github.com/debeatzgh1" target="_blank">GitHub</a> and insights on my <a href="https://beatzde4.blogspot.com/" target="_blank">blog</a>.</p>
      </div>
    </details>
    <details>
      <summary>What is the firebase-front repository?</summary>
      <div>
        <p>The <a href="https://github.com/debeatzgh1/firebase-front-end-components" target="_blank">firebase-front-end-components</a> repository is an open-source front-end template or starter kit for integrating Firebase services into web projects. It provides modern UI components and ready-to-use code for developers.</p>
      </div>
    </details>
    <details>
      <summary>How can I use your templates or code?</summary>
      <div>
        <p>Browse my <a href="https://github.com/debeatzgh1?tab=repositories" target="_blank">GitHub repositories</a> and follow the README instructions to clone or download templates and starter projects. Most projects are open source and free to use with attribution.</p>
      </div>
    </details>
    <details>
      <summary>Do you provide guides and tutorials?</summary>
      <div>
        <p>Yes! I share detailed guides, tech tips, and tutorials on my <a href="https://beatzde4.blogspot.com/" target="_blank">blog</a> covering Firebase, web development, productivity tools, and AI-powered solutions.</p>
      </div>
    </details>
    <details>
      <summary>How do I contact you for custom services?</summary>
      <div>
        <p>You can reach out via my blog's contact form, or through my email and social links provided on my <a href="https://github.com/debeatzgh1" target="_blank">GitHub profile</a>.</p>
      </div>
    </details>
    <details>
      <summary>Can I request a new feature or report a bug?</summary>
      <div>
        <p>Absolutely! Please open an issue on the relevant GitHub repository, or leave a comment on my blog post related to your request.</p>
      </div>
    </details>
    <details>
      <summary>Are your projects free to use?</summary>
      <div>
        <p>Most projects are open source and free for personal or educational use. Please check the license in each repository for details.</p>
      </div>
    </details>
    <details>
      <summary>What topics do you cover on your blog?</summary>
      <div>
        <p>I cover digital design, productivity tools, web development (especially Firebase), AI, and online business tips.</p>
      </div>
    </details>
    <details>
      <summary>Where can I follow your updates?</summary>
      <div>
        <p>Follow me on <a href="https://github.com/debeatzgh1" target="_blank">GitHub</a> for code/project updates and on <a href="https://beatzde4.blogspot.com/" target="_blank">Blogger</a> for articles and announcements.</p>
      </div>
    </details>
  </div>
</div>
<!-- AI Articles Modal -->
<div id="aiModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('aiModal')">&times;</span>
    <h2>AI Articles</h2>
    <ul>
      <li><a href="https://beatzde4.blogspot.com/search/label/AI" target="_blank">AI Articles on Beatzde4</a></li>
      <li><a href="https://appdategh1.blogspot.com/search/label/AI" target="_blank">AppdateGH AI Section</a></li>
    </ul>
    <p>Stay updated with the latest in AI, automation, and tech trends!</p>
  </div>
</div>
<!-- Gallery Modal -->
<div id="galleryModal" class="custom-modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('galleryModal')">&times;</span>
    <h2>Gallery</h2>
    <p>View creative inspiration, UI/UX samples, and project showcases:</p>
    <ul>
      <li><a href="https://pin.it/7iRoE2LKj" target="_blank">Pinterest Gallery</a></li>
    </ul>
  </div>
</div>
<script>
  function toggleMenu() {
    const menu = document.getElementById('iconLinks');
    menu.style.display = menu.style.display === 'flex' ? 'none' : 'flex';
  }
  function openModal(id) {
    document.getElementById(id).style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }
  function closeModal(id) {
    document.getElementById(id).style.display = 'none';
    document.body.style.overflow = '';
  }
  window.onclick = function(event) {
    const modals = document.querySelectorAll('.custom-modal');
    modals.forEach(function(modal) {
      if (event.target === modal) {
        modal.style.display = 'none';
        document.body.style.overflow = '';
      }
    });
  }
  document.addEventListener('keydown', function(event) {
    if (event.key === 'Escape') {
      document.querySelectorAll('.custom-modal').forEach(function(modal){
        modal.style.display = 'none';
      });
      document.body.style.overflow = '';
    }
  });
</script>




# My Project Portfolio

A responsive HTML modal portfolio featuring projects with GitHub and Live Preview buttons. Built using plain HTML, CSS, and JavaScript.

## 📌 Projects Included
- TechAdapt Solutions
- AI Productivity App
- Android AI Explorer
- AI Side Hustle Assistant
- Business Strategy Gist

## 🔗 Live Demo
Hosted at: [https://debeatzgh1.github.io/my-project-portfolio](https://debeatzgh1.github.io/my-project-portfolio)

## 🚀 How to Use
Clone the repo or upload the `index.html` directly to GitHub Pages to showcase your work.

---


# 🚀 DeBeatzGH – AI Tools & Side Hustle Hub  

![DeBeatzGH Thumbnail](https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designamodernminimalisticdesignfeaturinganai-themedicon28likeabraincircuitorrobot29overlaidwithdebeatzghoraitoolshustles6089986211026037047.jpg)  

## 🌟 About  
Welcome to **[DeBeatzGH](https://debeatzgh.wordpress.com/)** — your go-to hub for **AI tools, side hustle strategies, blogging resources, and digital growth guides**.  

Our platform is built to help **students, creators, startups, and professionals** unlock the power of AI, monetize their skills, and thrive in today’s digital economy.  

### ✨ What You’ll Find  
- 💡 Explore **AI prompts, tools, and hacks**  
- 📈 Discover **side hustle strategies & online income ideas**  
- ✍️ Access **blogging & digital business guides**  
- 🚀 Stay ahead with **regular updates and fresh insights**  

---

## 👉 Get Started  
🔥 **Start your journey today → [Visit DeBeatzGH](https://debeatzgh.wordpress.com/)**  

---

<!-- README: DebeatzGH Digital Store (HTML-friendly for GitHub) -->
<div align="center">
  <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener">
    <img
      src="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designadigitalproductse-commerceonlinedeals3545265155247625100.jpg"
      alt="DebeatzGH Digital Store"
      style="max-width:100%; border-radius:16px;"
    />
  </a>

  <h1 style="margin-top: 14px;">DebeatzGH Digital Store</h1>
  <p style="max-width:780px;">
    Your hub for AI insights, tech tutorials, side-hustle playbooks, and productivity tools.
    Learn, build, and launch digital projects faster.
  </p>

  <!-- CTAs -->
  <p>
    <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin:4px; border-radius:999px; text-decoration:none; font-weight:600; border:1px solid #2563eb;">
      🚀 View Live App
    </a>
    <a href="https://github.com/debeatzgh1/Personal-Portfolio-site-" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin:4px; border-radius:999px; text-decoration:none; font-weight:600; border:1px solid #111827;">
      ⭐ Star this Repo
    </a>
  </p>
</div>

<hr/>

<h2>Overview</h2>
<p>
  <strong>DebeatzGH</strong> helps beginners and creators build profitable digital assets:
  blogs, affiliate funnels, AI-assisted content, and more. Explore tutorials, tools, and
  ready-to-use components to speed up your workflow.
</p>

<h2>Features</h2>
<ul>
  <li><strong>AI & Tech Learning:</strong> Bite-sized guides for modern tools and workflows.</li>
  <li><strong>Side-Hustle Playbooks:</strong> Practical steps to validate and launch ideas.</li>
  <li><strong>Productivity Toolkit:</strong> Reusable widgets, templates, and scripts.</li>
  <li><strong>Beginner-Friendly:</strong> Clear explanations, curated resources, and examples.</li>
</ul>

<h2>Quick Start</h2>
<ol>
  <li>Clone:
    <pre><code>git clone https://github.com/debeatzgh1/Personal-Portfolio-site-</code></pre>
  </li>
  <li>Enter folder:
    <pre><code>cd debeatzgh</code></pre>
  </li>
  <li>Install deps (adjust to your stack):
    <pre><code># Node
npm install
npm run dev

# or Python
pip install -r requirements.txt
python app.py</code></pre>
  </li>
  <li>Open in browser:
    <pre><code>http://localhost:3000</code></pre>
  </li>
</ol>

<h2>Project Links</h2>
<ul>
  <li>🌐 Live App: <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener">socialcreator.com/debeatzgh</a></li>
  <li>🖼️ Thumbnail: <a href="https://debeatzgh.wordpress.com/wp-content/uploads/2025/08/designadigitalproductse-commerceonlinedeals3545265155247625100.jpg" target="_blank" rel="noopener">View image</a></li>
</ul>

<h2>Contributing</h2>
<p>
  Contributions are welcome! Open an issue for bugs or ideas. For changes, fork the repo,
  create a feature branch, and submit a pull request.
</p>

<h2>License</h2>
<p>
  Released under the <a href="./LICENSE">MIT License</a>.
</p>

<hr/>

<div align="center">
  <p><em>If this project helps you, consider giving it a star. It really helps! ⭐</em></p>
  <p>
    <a href="https://www.socialcreator.com/debeatzgh" target="_blank" rel="noopener"
       style="display:inline-block; padding:10px 16px; margin-top:6px; border-radius:10px; text-decoration:none; font-weight:600; border:1px solid #2563eb;">
      Open DebeatzGH Now →
    </a>
  </p>
</div>
