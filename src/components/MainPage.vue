<script setup></script>

<template>
  <div class="main-container">
    <header class="header">
      <div class="logo">
        <img src="../assets/logo.jpg" alt="Quantum Ripple logo" />
        <h1>Quantum Ripple</h1>
      </div>
      <nav class="nav-links">
        <a href="#">Home</a>
        <a href="#about">About</a>
        <a href="#works">Works</a>
        <a href="#softwares">Softwares</a>
      </nav>
    </header>

    <section class="hero">
      <video autoplay muted loop playsinline class="video-bg">
        <source src="../assets/10.mp4" type="video/mp4" />
      </video>
      <div class="overlay"></div>
      <div class="hero-content">
        <h1>Engineering Tomorrow<span>.</span></h1>
        <p>
          Quantum Ripple builds future-proof software powered by AI, data, and human creativity.
        </p>
        <button>Discover More</button>
      </div>
    </section>

    <section id="about" class="about">
      <div class="about-grid">
        <img src="../assets/2.jpeg" alt="Company office" class="office" />
        <div class="text">
          <h2>About Quantum Ripple</h2>
          <p>
            At Quantum Ripple, we don’t just develop software — we engineer digital ecosystems. From
            intelligent web platforms to automation systems that think ahead, our mission is to make
            technology intuitive and impactful.
          </p>
          <p>
            Our offices are powered by a team of creative engineers, designers, and researchers
            building tools that push the boundaries of what’s possible.
          </p>
        </div>
      </div>
    </section>

    <section id="softwares" class="softwares">
      <h2>Core Services</h2>
      <div class="cards">
        <div class="card">
          <img src="../assets/6.jpeg" alt="Code" />
          <h3>Custom Software</h3>
          <p>We develop scalable, adaptive systems that evolve with your business.</p>
        </div>
        <div class="card">
          <img src="../assets/7.jpeg" alt="Coding" />
          <h3>Web Experiences</h3>
          <p>
            From minimal landing pages to enterprise dashboards — crafted for performance and
            beauty.
          </p>
        </div>
        <div class="card">
          <img src="../assets/8.jpeg" alt="AI" />
          <h3>AI & Data Solutions</h3>
          <p>Harness machine intelligence and analytics to unlock insight and automation.</p>
        </div>
      </div>
    </section>

    <section id="works" class="works">
      <h2>Selected Works</h2>
      <div class="gallery work-cards">
        <article class="work-card">
          <h3>Precious School Website</h3>
          <p>A responsive school website built for modern UX and fast performance.</p>
          <a class="work-link" href="https://precioussc.netlify.app" target="_blank">Visit Site</a>
        </article>

        <article class="work-card">
          <h3>CELVE LMS</h3>
          <p>A learning management system designed for scalable classroom experiences.</p>
          <a class="work-link" href="https://celve.netlify.app" target="_blank">View LMS</a>
        </article>

        <article class="work-card">
          <h3>CELVE Website</h3>
          <p>Marketing site and documentation portal for the CELVE platform.</p>
          <a class="work-link" href="https://celve.netlify.app" target="_blank">Visit Site</a>
        </article>
      </div>
    </section>

    <section id="team" class="team">
      <h2>Our Team</h2>
      <p class="intro">
        Quantum Ripple thrives on collaboration — brilliant minds building the digital future
        together.
      </p>

      <div class="team-grid">
        <div class="member">
          <div class="count">3</div>
          <h3>Frontend Engineers</h3>
          <p>
            Craft immersive interfaces and micro-interactions that make our systems feel alive and
            intuitive.
          </p>
        </div>

        <div class="member">
          <div class="count">3</div>
          <h3>Backend Engineers</h3>
          <p>Architect and maintain the unseen logic — secure APIs and scalable systems.</p>
        </div>

        <div class="member">
          <div class="count">2</div>
          <h3>Full Stack Engineers</h3>
          <p>Connect front and back ends for seamless, end-to-end experiences.</p>
        </div>

        <div class="member">
          <div class="count">1</div>
          <h3>AI Engineer</h3>
          <p>Designs adaptive ML systems and intelligent pipelines.</p>
        </div>

        <div class="member">
          <div class="count">1</div>
          <h3>Designer</h3>
          <p>Shapes the visual identity, motion, and UX of our products.</p>
        </div>

        <div class="member">
          <div class="count">10</div>
          <h3>Interns</h3>
          <p>Our future innovators — learning and contributing across all disciplines.</p>
        </div>
      </div>
    </section>

    <footer class="footer">
      <div class="footer-grid">
        <div class="footer-brand">
          <h2>Quantum Ripple</h2>
          <p>
            Building intelligent systems, futuristic software, and digital solutions that power the
            next generation of technology.
          </p>
        </div>

        <div class="footer-links">
          <h3>Quick Links</h3>
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#softwares">Softwares</a></li>
            <li><a href="#works">Our Works</a></li>
            <li><a href="#team">Team</a></li>
          </ul>
        </div>

        <div class="footer-contact">
          <h3>Contact</h3>
          <p>Email: <a href="mailto:quantumrippleltd@gmail.com">info@quantumripple.co.ke</a></p>
          <p>Phone: +254 63 329346</p>
          <div class="socials">
            <a href="#">Twitter</a>
            <a href="#">LinkedIn</a>
            <a href="#">GitHub</a>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <div class="glow-line"></div>
        <p>© 2025 Quantum Ripple. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<style>
:root {
  --header-height: 72px;
  --bg: #060a1f;
  --accent1: #00ffe1;
  --accent2: #007bff;
  --text: #e5e8ff;
  --glass: rgba(255, 255, 255, 0.06);
  --card: rgba(255, 255, 255, 0.08);
}

body {
  margin: 0;
  background: var(--bg);
  font-family: 'Poppins', sans-serif;
  color: var(--text);
  overflow-x: hidden;
}

.header {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(12px);
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
  padding: 1rem 2rem;
  z-index: 10;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  height: var(--header-height);
}

.logo {
  display: flex;
  align-items: center;
  gap: 6px;
  justify-self: start;
}
.logo img {
  width: 45px;
  border-radius: 8px;
}
.logo h1 {
  font-size: 1.4rem;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 600;
}
.nav-links {
  grid-column: 2;
  justify-self: center;
  display: flex;
  gap: 22px;
  align-items: center;
}

.nav-links a {
  color: var(--text);
  text-decoration: none;
  font-weight: 500;
  transition: 0.3s;
}
.nav-links a:hover {
  color: var(--accent1);
}

.hero {
  /* start below the fixed header */
  margin-top: var(--header-height);
  height: calc(100vh - var(--header-height));
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #fff;
  /* cover image fallback / hero cover */
  background-image: url('../assets/1.jpeg');
  background-size: cover;
  background-position: center center;
}
.video-bg {
  position: absolute;
  width: 100%;
  height: 100%;
  object-fit: cover;
  top: 0;
  left: 0;
  filter: brightness(0.35);
}
.overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.4), transparent 60%, rgba(0, 0, 0, 0.7));
}
.hero-content {
  z-index: 2;
  max-width: 800px;
}
.hero h1 {
  font-size: 3.2rem;
  letter-spacing: 1px;
}
.hero h1 span {
  color: var(--accent1);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.hero p {
  font-size: 1.1rem;
  margin: 1rem auto;
  max-width: 600px;
}
.hero button {
  margin-top: 1.5rem;
  padding: 0.9rem 2.2rem;
  border: none;
  border-radius: 30px;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  color: #000;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.3s ease;
}
.hero button:hover {
  transform: scale(1.07);
}

.about {
  padding: 6rem 2rem;
}
.about-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
  gap: 2rem;
  align-items: center;
  max-width: 1100px;
  margin: auto;
}
.office {
  width: 100%;
  border-radius: 20px;
  box-shadow: 0 0 30px rgba(0, 255, 255, 0.05);
}
.text h2 {
  color: var(--accent1);
  font-size: 2rem;
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.text p {
  color: #cfd3f7;
  line-height: 1.7;
  margin-bottom: 1rem;
}

.softwares {
  padding: 6rem 2rem;
  text-align: center;
}
.softwares h2 {
  color: var(--accent2);
}
.cards {
  margin-top: 3rem;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
  max-width: 1100px;
  margin-inline: auto;
}
.card {
  background: var(--card);
  border-radius: 18px;
  padding: 1.5rem;
  backdrop-filter: blur(6px);
  transition: transform 0.4s;
}
.card:hover {
  transform: translateY(-8px);
}
.card img {
  width: 100%;
  border-radius: 12px;
  margin-bottom: 1rem;
}

.works {
  padding: 6rem 2rem;
  text-align: center;
}
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
  max-width: 1100px;
  margin-inline: auto;
}

.work-cards .work-card {
  background: var(--card);
  border-radius: 14px;
  padding: 1.6rem;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
  min-height: 180px;
}

.work-card h3 {
  margin: 0;
  color: var(--accent1);
}

.work-card p {
  color: #d7d9ef;
  flex: 1 1 auto;
}

.work-link {
  align-self: start;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  color: #000;
  padding: 0.5rem 0.9rem;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 600;
}
.project {
  position: relative;
  overflow: hidden;
  border-radius: 15px;
}
.project img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: 0.4s;
}
.project:hover img {
  transform: scale(1.05);
}
.overlay-text {
  position: absolute;
  inset: 0;
  background: linear-gradient(180deg, transparent, rgba(0, 0, 0, 0.7));
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  opacity: 0;
  transition: 0.4s;
}
.project:hover .overlay-text {
  opacity: 1;
}
.overlay-text h3 {
  color: var(--accent1);
  margin-bottom: 0.5rem;
}
.overlay-text a {
  color: #fff;
  text-decoration: underline;
}
.team {
  padding: 6rem 2rem;
  text-align: center;
  background: linear-gradient(180deg, rgba(0, 255, 255, 0.05), rgba(0, 0, 0, 0.8));
  color: var(--text);
}

.team h2 {
  font-size: 2.2rem;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 1rem;
}

.team-grid .member {
  opacity: 0;
  transform: translateY(10px) rotateX(6deg);
  animation: memberIn 520ms cubic-bezier(0.2, 0.9, 0.2, 1) forwards;
  transition:
    transform 0.35s ease,
    box-shadow 0.35s ease;
}
.team-grid .member:nth-child(1) {
  animation-delay: 80ms;
}
.team-grid .member:nth-child(2) {
  animation-delay: 160ms;
}
.team-grid .member:nth-child(3) {
  animation-delay: 240ms;
}
.team-grid .member:nth-child(4) {
  animation-delay: 320ms;
}
.team-grid .member:nth-child(5) {
  animation-delay: 400ms;
}

@keyframes memberIn {
  to {
    opacity: 1;
    transform: translateY(0) rotateX(0);
  }
}

.member:hover {
  transform: translateY(-6px) rotateX(0);
  box-shadow: 0 18px 40px rgba(0, 255, 204, 0.06);
}

.member .avatar {
  width: 76px;
  height: 76px;
  border-radius: 12px;
  overflow: hidden;
  margin-bottom: 0.8rem;
}
.member .avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}
.member h3 {
  margin: 0 0 0.25rem 0;
  color: var(--accent1);
}
.member .role {
  color: var(--accent2);
  font-weight: 600;
  margin-bottom: 0.6rem;
}
.member .bio {
  color: #cfd3f7;
  font-size: 0.95rem;
}

.team .intro {
  max-width: 700px;
  margin: 0 auto 3rem;
  color: #cfd3f7;
  font-size: 1rem;
  line-height: 1.7;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
  max-width: 1100px;
  margin: 0 auto;
}

.member {
  background: var(--card);
  border-radius: 15px;
  padding: 1.8rem;
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.05);
  transition: 0.3s ease;
  box-shadow: 0 0 10px rgba(0, 255, 255, 0.05);
}

.member:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 25px rgba(0, 255, 255, 0.2);
}

.member h3 {
  color: var(--accent1);
  font-size: 1.2rem;
  margin-bottom: 0.6rem;
}

.member p {
  color: #cfd3f7;
  font-size: 0.95rem;
  line-height: 1.6;
}

.member .count {
  font-size: 2.6rem;
  font-weight: 800;
  color: #000;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  padding: 0.45rem 0.8rem;
  border-radius: 12px;
  display: inline-block;
  margin-bottom: 0.6rem;
  box-shadow:
    0 8px 30px rgba(0, 0, 0, 0.45),
    0 0 18px rgba(0, 255, 204, 0.06);
}

.team-grid .member {
  opacity: 0;
  transform: translateY(8px);
  animation: memberCountIn 520ms cubic-bezier(0.2, 0.9, 0.2, 1) forwards;
}
.team-grid .member:nth-child(1) {
  animation-delay: 80ms;
}
.team-grid .member:nth-child(2) {
  animation-delay: 160ms;
}
.team-grid .member:nth-child(3) {
  animation-delay: 240ms;
}
.team-grid .member:nth-child(4) {
  animation-delay: 320ms;
}
.team-grid .member:nth-child(5) {
  animation-delay: 400ms;
}
.team-grid .member:nth-child(6) {
  animation-delay: 480ms;
}

@keyframes memberCountIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.prefooter {
  position: relative;
  text-align: center;
}
.prefooter img {
  width: 100%;
  height: 60vh;
  object-fit: cover;
  filter: brightness(0.4);
}
.caption {
  position: absolute;
  inset: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: #fff;
}
.caption h2 {
  color: var(--accent1);
  font-size: 2rem;
}
.caption p {
  font-size: 1rem;
}

.footer {
  background: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(10px);
  padding: 4rem 2rem 2rem;
  color: var(--text);
  position: relative;
  overflow: hidden;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

/* Glowing lines animation */
.footer::before,
.footer::after {
  content: '';
  position: absolute;
  width: 200%;
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--accent1), var(--accent2), transparent);
  top: 0;
  left: -50%;
  opacity: 0.4;
  animation: moveGlow 8s linear infinite;
}

@keyframes moveGlow {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(50%);
  }
}

/* Footer Grid Layout */
.footer-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 2rem;
  max-width: 1100px;
  margin: auto;
}

.footer-brand h2 {
  font-size: 1.5rem;
  background: linear-gradient(90deg, var(--accent1), var(--accent2));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.footer-brand p {
  color: #bfc7e0;
  line-height: 1.6;
  font-size: 0.95rem;
  margin-top: 0.5rem;
}

.footer-links h3,
.footer-contact h3 {
  color: var(--accent1);
  font-size: 1.1rem;
  margin-bottom: 0.8rem;
}

.footer-links ul {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin: 0.4rem 0;
}

.footer-links a {
  color: #bfc7e0;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--accent2);
}

.footer-contact a {
  color: var(--accent2);
  text-decoration: none;
}

.footer-contact a:hover {
  text-decoration: underline;
}

.socials {
  margin-top: 1rem;
  display: flex;
  gap: 1rem;
}

.socials a {
  color: var(--accent1);
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.3s;
}

.socials a:hover {
  color: var(--accent2);
}

/* Footer Bottom */
.footer-bottom {
  margin-top: 3rem;
  text-align: center;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  padding-top: 1rem;
}

.footer-bottom p {
  font-size: 0.85rem;
  color: #9ea4c2;
}

.glow-line {
  width: 100%;
  height: 2px;
  margin-bottom: 0.8rem;
  background: linear-gradient(90deg, transparent, var(--accent1), var(--accent2), transparent);
  opacity: 0.5;
}

.copy {
  color: #888;
  margin-top: 1rem;
}
</style>
