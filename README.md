<!DOCTYPE html> 
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Siva Harish | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet"/>
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    body {
      display: flex;
      background-color: #121821;
      color: white;
    }

    aside {
      width: 280px;
      background-color: #0d1117;
      height: 100vh;
      padding: 1rem 0.5rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      border-right: 1px solid #1f2937;
      position: fixed;
    }

    aside img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      border: 4px solid #2dd4bf;
    }

    aside h2 {
      margin-top: 1rem;
      font-size: 1.5rem;
    }

    .social-icons {
      display: flex;
      gap: 1rem;
      margin: 1rem 0;
    }

    .social-icons a {
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
    }

    nav {
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
      margin-top: 2rem;
      width: 100%;
      padding-left: 0.5rem;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    nav a:hover {
      color: #2dd4bf;
    }

    .content {
      margin-left: 280px;
      flex: 1;
      padding: 1rem;
    }

    .main-content {
      background: url('image.png') no-repeat center center/cover;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
      height: 100vh;
    }

    .main-content h1 {
      font-size: 3rem;
      font-weight: 700;
    }

    .typing-container {
      margin-top: 1rem;
    }

    .typing-text {
      font-size: 1.5rem;
      display: inline-block;
      position: relative;
    }

    .typing-text::after {
      content: '|';
      animation: blink 0.7s infinite;
      position: absolute;
      right: -10px;
    }

    .underline {
      height: 2px;
      background-color: #2dd4bf;
      margin-top: 2px;
      transition: width 0.1s;
    }

    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

    section {
      background-color: #fff;
      color: #000;
      padding: 2rem 1rem;
      margin-bottom: 2rem;
    }

    .about-text h2, .resume-section h2, .services-section h2, .skills-section h2 {
      font-size: 2rem;
      border-bottom: 2px solid #2dd4bf;
      display: inline-block;
      margin-bottom: 1.5rem;
    }

    .about-columns {
      display: flex;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .about-columns img {
      max-width: 280px;
      border-radius: 12px;
    }

    .info-columns {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      flex: 1;
    }

    .details {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
    }

    .details p {
      font-size: 0.95rem;
      margin: 0;
    }

    .columns {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin-top: 1rem;
    }

    .column {
      flex: 1;
      min-width: 300px;
    }

    .entry {
      margin-bottom: 2rem;
      position: relative;
      padding-left: 20px;
    }

    .entry::before {
      content: "";
      position: absolute;
      left: 0;
      top: 8px;
      width: 10px;
      height: 10px;
      background: #0ea5e9;
      border-radius: 50%;
    }

    .entry h3 {
      margin: 0;
      font-size: 1.1rem;
      color: #111827;
    }

    .entry h4 {
      font-size: 0.95rem;
      color: #475569;
      margin: 0.25rem 0;
      font-style: italic;
    }

    .entry p {
      margin: 0.3rem 0;
      font-size: 0.92rem;
      color: #374151;
    }

    .services-section {
    background-color: #f1f5f9;
    color: #0f172a;
    padding: 3rem 1rem;
    animation: fadeInUp 1s ease forwards;
  }

  .services-section h2 {
    font-size: 2rem;
    border-bottom: 2px solid #2dd4bf;
    display: inline-block;
    margin-bottom: 2rem;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 2rem;
  }

  .service-card {
    background: white;
    padding: 1.5rem;
    border-radius: 12px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.05);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    text-align: center;
  }

  .service-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.1);
  }

  .service-card .icon {
    font-size: 2rem;
    color: #0ea5e9;
    margin-bottom: 1rem;
  }

  .service-card h3 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
    color: #1e293b;
  }

  .service-card p {
    font-size: 0.95rem;
    color: #334155;
  }

    /* New Skills Section */
    .skills-section {
      background-color: #f8fafc;
      padding: 2rem;
      animation: fadeInUp 1s ease forwards;
    }

    .skills-section p {
      margin-bottom: 2rem;
      font-size: 1rem;
      color: #1e293b;
    }

    .skills-container .skill {
      margin-bottom: 1.5rem;
    }

    .skills-container .skill span {
      display: block;
      margin-bottom: 0.4rem;
      font-weight: 600;
      color: #111827;
    }

    .progress {
      background-color: #e5e7eb;
      height: 10px;
      border-radius: 5px;
      overflow: hidden;
    }

    .progress-bar {
      height: 10px;
      background-color: #0ea5e9;
      width: 0;
      border-radius: 5px;
      transition: width 1.5s ease-in-out;
    }

    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(40px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>
  <aside>
    <img src="my-profile-img.jpg" alt="Profile Photo">
    <h2>Siva Harish</h2>
    <div class="social-icons">
      <a href="https://github.com/SivaHarish03" target="_blank"><i class="fab fa-github"></i></a>
      <a href="https://www.facebook.com/yourusername" target="_blank"><i class="fab fa-facebook"></i></a>
      <a href="https://www.instagram.com/yourusername" target="_blank"><i class="fab fa-instagram"></i></a>
      <a href="https://www.linkedin.com/in/yourusername" target="_blank"><i class="fab fa-linkedin"></i></a>
    </div>
    <nav>
      <a href="#"><i class="fas fa-home"></i> Home</a>
      <a href="#"><i class="fas fa-user"></i> About</a>
      <a href="#"><i class="fas fa-file"></i> Resume</a>
      <a href="#"><i class="fas fa-briefcase"></i> Services</a>
      <a href="#"><i class="fas fa-layer-group"></i> Dropdown</a>
    </nav>
  </aside>

  <div class="content">
    <section class="main-content">
      <h1>Siva Harish</h1>
      <div class="typing-container">
        <span class="typing-text" id="typing"></span>
        <div class="underline" id="underline"></div>
      </div>
    </section>

    <section class="about-section">
      <div class="about-text">
        <h2>About</h2>
        <p>Hi there! I’m Siva Harish, a passionate web developer and UI/UX designer dedicated to creating beautiful, user-friendly digital experiences. With a blend of technical expertise and a keen eye for design, I strive to bring ideas to life in a way that is both functional and visually appealing.</p>
      </div></br></br>
      <div class="about-columns">
        <img src="my-profile-img.jpg" alt="Profile Details Image">
        <div class="info-columns">
          <h2>UI/UX Designer & Web Developer</h2>
          <p><i>As a UI/UX designer and web developer, I am passionate about crafting intuitive and engaging digital experiences. With a strong foundation in both design and development, I bridge the gap between aesthetics and functionality. My approach is user-centered, ensuring that every project I undertake not only meets the needs of the client but also resonates with the end user. I thrive on collaboration and creativity, constantly seeking innovative solutions to complex problems. Let's transform ideas into reality and create something extraordinary together!.</i></p></br></br>
          <div class="details">
            <p><strong>Birthday:</strong> 03 March 2004</p>
            <p><strong>Specialization:</strong> Information Technology</p>
            <p><strong>Phone:</strong> +91 9080866625</p>
            <p><strong>City:</strong> Tamil Nadu, India</p>
            <p><strong>Age:</strong> 21</p>
            <p><strong>Degree:</strong> Bachelor's</p>
            <p><strong>Email:</strong> sivaharish2k1@gmail.com</p>
            <p><strong>Freelance:</strong> Available</p>
          </div>
          
        </div>
      </div>
    </section>

    <section class="resume-section">
      <h2>Resume</h2>
      <p>With a solid foundation in both UI/UX design and web development, I have cultivated a diverse range of experiences that equip me to tackle complex challenges. My journey includes working with various clients across different industries, where I have successfully delivered projects that enhance user engagement and drive results. I am committed to continuous growth, always seeking opportunities to expand my skill set and stay updated with industry trends. My resume reflects a blend of creativity, technical proficiency, and a passion for creating meaningful digital experiences.</p>
      <div class="columns">
        <div class="column">
          <h3>Education</h3>
          <div class="entry">
            <h3>Bachelor of Technology in Information Technology</h3>
            <h4>2021 - 2025 | Kongunadu College</h4>
            <p>Programming, data structures, algorithms, and network security.</p>
          </div>
          <div class="entry">
            <h3>12th - Bio Maths</h3>
            <h4>2020 - 2021 | Holy Cross School</h4>
            <p>Focused on Chemistry, Biology, and mathematics.</p>
          </div>
          <div class="entry">
            <h3>10th Standard</h3>
            <h4>2018 - 2019 | St. Joseph's School</h4>
            <p>Math, Science, and English foundations with critical thinking.</p>
          </div>
        </div>
        <div class="column">
          <h3>Intern Experience</h3>
          <div class="entry">
            <h3>Web Development Intern</h3>
            <h4>2023 | CodeBind Technologies</h4>
            <p>Built responsive websites and team collaboration.</p>
          </div>
          <div class="entry">
            <h3>Internet of Things Intern</h3>
            <h4>2022 | Training Trains</h4>
            <p>Sensor systems, IoT architecture, and cloud integration.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="services-section">
      <h2>Services</h2>
      <div class="services-grid">
        <div class="service-card">
          <div class="icon"><i class="fas fa-code"></i></div>
          <h3>Website Development</h3>
          <p>Custom website design & development, E-commerce sites, CMS integration with responsive design.</p>
        </div>
        <div class="service-card">
          <div class="icon"><i class="fas fa-search"></i></div>
          <h3>SEO Optimization</h3>
          <p>On-page SEO, site speed optimization, and structured data for better search visibility.</p>
        </div>
        <div class="service-card">
          <div class="icon"><i class="fas fa-server"></i></div>
          <h3>Web Hosting</h3>
          <p>Hosting setup, domain registration, and ongoing domain and server management services.</p>
        </div>
        <div class="service-card">
          <div class="icon"><i class="fas fa-users"></i></div>
          <h3>User Research</h3>
          <p>Conducting interviews, usability testing, and building personas for targeted design strategies.</p>
        </div>
        <div class="service-card">
          <div class="icon"><i class="fas fa-paint-brush"></i></div>
          <h3>Visual Design</h3>
          <p>Crafting UI for web & mobile apps, branding elements, icons, and style guidelines.</p>
        </div>
        <div class="service-card">
          <div class="icon"><i class="fas fa-object-group"></i></div>
          <h3>UX Design</h3>
          <p>Creating wireframes, information architecture, and intuitive interaction flows.</p>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section class="skills-section" id="skills">
      <h2>Skills</h2>
      <p>
        With a diverse skill set that bridges design and development, I excel in creating user-centric solutions...
      </p>
      <div class="skills-container">
        <div class="skill">
          <span>HTML</span>
          <div class="progress"><div class="progress-bar" data-progress="100%"></div></div>
        </div>
        <div class="skill">
          <span>CSS</span>
          <div class="progress"><div class="progress-bar" data-progress="90%"></div></div>
        </div>
        <div class="skill">
          <span>JavaScript</span>
          <div class="progress"><div class="progress-bar" data-progress="75%"></div></div>
        </div>
        <div class="skill">
          <span>PHP</span>
          <div class="progress"><div class="progress-bar" data-progress="80%"></div></div>
        </div>
        <div class="skill">
          <span>WordPress/CMS</span>
          <div class="progress"><div class="progress-bar" data-progress="90%"></div></div>
        </div>
        <div class="skill">
          <span>React JS</span>
          <div class="progress"><div class="progress-bar" data-progress="50%"></div></div>
        </div>
      </div>
    </section>
  </div>

  <script>
    const texts = ["I'm Designer", "I'm Developer"];
    let textIndex = 0;
    let charIndex = 0;
    const typingElement = document.getElementById('typing');
    const underlineElement = document.getElementById('underline');
  
    function typeText() {
      if (charIndex < texts[textIndex].length) {
        typingElement.textContent += texts[textIndex].charAt(charIndex);
        underlineElement.style.width = `${typingElement.offsetWidth}px`;
        charIndex++;
        setTimeout(typeText, 100);
      } else {
        setTimeout(() => {
          charIndex = 0;
          textIndex = (textIndex + 1) % texts.length;
          typingElement.textContent = '';
          underlineElement.style.width = '0px';
          setTimeout(typeText, 500);
        }, 1500);
      }
    }
  
    window.onload = typeText;
  
    // Skills animation on scroll
    window.addEventListener("scroll", function () {
      const skillsSection = document.querySelector("#skills");
      const skillBars = document.querySelectorAll(".progress-bar");
      const sectionTop = skillsSection.getBoundingClientRect().top;
      const windowHeight = window.innerHeight;
  
      if (sectionTop < windowHeight - 100) {
        skillBars.forEach(bar => {
          bar.style.width = bar.getAttribute("data-progress");
        });
      }
    });
  </script>
  
</body>
</html>
