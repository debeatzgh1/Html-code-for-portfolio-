<style>
/* 1. RESET & VARIABLES */
:root {
  --dd-bg: #1a1c1e; /* Deep Dark */
  --dd-text: #f0f6fc;
  --dd-accent: #1877F2; /* Facebook Blue */
  --dd-border: rgba(240, 246, 252, 0.1);
  --dd-font: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
}

/* 2. MAIN CONTAINER (SLIM-FIT & FLOATING) */
.dd-banner-container {
  position: fixed;
  top: 10px; /* Slight offset for modern float */
  right: 50%;
  transform: translateX(-50%);
  width: 92%;
  max-width: 900px;
  height: 40px; /* Slim height */
  background-color: var(--dd-bg);
  background-image: radial-gradient(at 10% 10%, rgba(24, 119, 242, 0.15) 0px, transparent 50%),
                    radial-gradient(at 90% 90%, rgba(240, 246, 252, 0.05) 0px, transparent 50%);
  border: 1px solid var(--dd-border);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 10px 0 15px;
  z-index: 999999; /* Ensure topmost */
  box-shadow: 0 10px 25px rgba(0,0,0,0.4);
  overflow: hidden;
  transition: all 0.3s ease;
  font-family: var(--dd-font);
}

.dd-banner-container:hover {
  border-color: var(--dd-accent);
  box-shadow: 0 10px 30px rgba(24, 119, 242, 0.2);
  transform: translateX(-50%) translateY(-2px);
}

/* 3. LEFT SECTION (BRAND & SLIDER) */
.dd-left {
  display: flex;
  align-items: center;
  gap: 12px;
  flex: 1;
  overflow: hidden;
}

.dd-brand {
  color: var(--dd-accent);
  font-size: 16px;
  display: flex;
  align-items: center;
}

/* AUTO-SLIDE TEXT LOGIC */
.dd-slider-box {
  flex: 1;
  height: 20px;
  overflow: hidden;
  position: relative;
}

.dd-slider-content {
  display: flex;
  flex-direction: column;
  animation: ddTextSlide 12s cubic-bezier(0.645, 0.045, 0.355, 1) infinite;
}

.dd-slider-content span {
  height: 20px;
  font-size: 11px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: var(--dd-text);
  display: flex;
  align-items: center;
  white-space: nowrap;
}

.dd-highlight { color: var(--dd-accent); font-weight: 800; }

@keyframes ddTextSlide {
  0%, 20% { transform: translateY(0); }             /* Intro */
  25%, 45% { transform: translateY(-20px); }        /* Recommend 1 */
  50%, 70% { transform: translateY(-40px); }        /* Recommend 2 */
  75%, 95% { transform: translateY(-60px); }        /* Action */
  100% { transform: translateY(0); }                /* Reset loop */
}

/* 4. RIGHT SECTION (ACTION BUTTON) */
.dd-right {
  display: flex;
  align-items: center;
}

.dd-join-btn {
  background-color: var(--dd-accent);
  color: #ffffff;
  border: none;
  padding: 5px 12px;
  border-radius: 6px;
  font-size: 10px;
  font-weight: 800;
  text-transform: uppercase;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.2s ease;
  display: flex;
  align-items: center;
  gap: 6px;
  text-decoration: none;
}

.dd-join-btn:hover {
  background-color: #ffffff;
  color: #1877F2;
  transform: scale(1.05);
}

/* 5. MOBILE OPTIMIZATION */
@media (max-width: 600px) {
  .dd-banner-container { width: 96%; top: 5px; height: 36px; padding: 0 8px; }
  .dd-brand { font-size: 14px; }
  .dd-slider-content span { font-size: 9px; }
  .dd-join-btn { padding: 4px 8px; font-size: 9px; }
  .dd-btn-text { display: none; } /* Show only icon on mobile */
  .dd-join-btn i { font-size: 12px; margin: 0; }
}
</style>

<div class='dd-banner-container'>
  <div class='dd-left'>
    <div class='dd-brand'>
      <i class='fab fa-facebook-square'></i>
    </div>
    <div class='dd-slider-box'>
      <div class='dd-slider-content'>
        <span>Official Community: <strong class='dd-highlight'>&quot;Digital Dynamo&quot;</strong></span>
        <span>Recommended: Amplify our tech insights in the group.</span>
        <span>Deepen the discussion: Join the <strong class='dd-highlight'>Dynamo</strong> network.</span>
        <span>Action Required: Tap &#39;Chat with AI Bot &#39; to deepen Research.</span>
      </div>
    </div>
  </div>
  <div class='dd-right'>
    <a class='dd-join-btn' href='https://debeatzgh1.github.io/ai-chat/' target='_blank'>
      <i class='fas fa-users'></i> <span class='dd-btn-text'>Contact support</span>
    </a>
  </div>
</div>

<script src='https://kit.fontawesome.com/0f6c123a31.js' crossorigin='anonymous'></script>






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
    width: 40px;
    height: 40px;
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
    <p><strong>debeatzgh</strong> is a freelance platform by a passionate developer, designer, and content creator dedicated to empowering creators and entrepreneurs through open-source tools, digital products, and educational content. Across multiple platforms (GitHub and Blogger), debeatzgh(1 shares curated front-end components, productivity resources, and guides for web development, AI, and digital business growth.</p>
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
      <li><a href="https://debeatzgh1.github.io/Home-/" target="_blank">Beatzde4 Blog Contact</a></li>
      <li>Email: <a href="debeatz4@gmail.com">Use blog contact form</a></li>
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
      <li><a href="https://debeatzgh1.github.io/Home-/" target="_blank">Beatzde4 Blog Tools</a>: Widgets, templates, and utilities for bloggers and creators.</li>
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
      <li><a href="http://digimartgh.blogspot.com/" target="_blank">debeatzgh</a>: Digital marketing, business tools, and guides.</li>
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
        <p>debeatzgh is a freelance developer, designer, and content creator focused on building modern web apps, sharing productivity tools, and providing digital solutions. Find my projects on <a href="https://github.com/debeatzgh1" target="_blank">GitHub</a> and insights on my <a href="https://beatzde4.blogspot.com/" target="_blank">blog</a>.</p>
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
        <p>Follow me on <a href="https://github.com/debeatzgh1" target="_blank">GitHub</a> for code/project updates and on <a href="https://debeatzgh1.github.io/debeatzgh/" target="_blank">Blogger</a> for articles and announcements.</p>
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

<!-- Elfsight Announcement Bar | Ads -->
<script src="https://elfsightcdn.com/platform.js" async></script>
<div class="elfsight-app-da4c4e26-f1fe-4865-98e5-07ab2384d659" data-elfsight-app-lazy></div>
