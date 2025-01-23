<script setup lang="ts">
import { ref } from 'vue'

const testimonials = ref([
  {
    name: 'John Doe',
    role: 'CEO, Tech Corp',
    content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero.',
    image: 'https://i.pravatar.cc/150?img=1'
  },
  {
    name: 'Jane Smith',
    role: 'Designer, Creative Co',
    content: 'Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.',
    image: 'https://i.pravatar.cc/150?img=2'
  },
  {
    name: 'Mike Johnson',
    role: 'Developer, Innovation Labs',
    content: 'Duis sagittis ipsum. Praesent mauris. Fusce nec tellus sed augue semper porta.',
    image: 'https://i.pravatar.cc/150?img=3'
  }
])

const stats = ref([
  { label: 'Happy Clients', value: '500+' },
  { label: 'Projects Completed', value: '1000+' },
  { label: 'Team Members', value: '50+' },
  { label: 'Awards Won', value: '25+' }
])
</script>

<template>
  <div class="app-container">
    <header class="header">
      <nav class="nav">
        <div class="logo">InnovateTech</div>
        <div class="nav-links">
          <a href="#home">Home</a>
          <a href="#about">About</a>
          <a href="#services">Services</a>
          <a href="#portfolio">Portfolio</a>
          <a href="#testimonials">Testimonials</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>
    </header>

    <main class="main">
      <section id="home" class="hero">
        <div class="hero-content">
          <h1>Transform Your Digital Presence</h1>
          <p class="subtitle">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.</p>
          <div class="hero-buttons">
            <button class="cta-button primary">Get Started</button>
            <button class="cta-button secondary">Learn More</button>
          </div>
        </div>
        <div class="hero-image">
          <img src="https://placehold.co/600x400" alt="Hero Image" />
        </div>
      </section>

      <section id="about" class="about">
        <h2>About Us</h2>
        <div class="about-content">
          <div class="about-text">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident.</p>
          </div>
          <div class="stats-grid">
            <div v-for="stat in stats" :key="stat.label" class="stat-card">
              <h3>{{ stat.value }}</h3>
              <p>{{ stat.label }}</p>
            </div>
          </div>
        </div>
      </section>

      <section id="services" class="services">
        <h2>Our Services</h2>
        <div class="services-grid">
          <div class="service-card">
            <div class="service-icon">🚀</div>
            <h3>Innovation</h3>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam scelerisque justo in felis elementum.</p>
            <a href="#" class="learn-more">Learn More →</a>
          </div>
          <div class="service-card">
            <div class="service-icon">💡</div>
            <h3>Strategy</h3>
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo.</p>
            <a href="#" class="learn-more">Learn More →</a>
          </div>
          <div class="service-card">
            <div class="service-icon">⚡</div>
            <h3>Development</h3>
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla.</p>
            <a href="#" class="learn-more">Learn More →</a>
          </div>
          <div class="service-card">
            <div class="service-icon">📱</div>
            <h3>Mobile Apps</h3>
            <p>Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit.</p>
            <a href="#" class="learn-more">Learn More →</a>
          </div>
        </div>
      </section>

      <section id="portfolio" class="portfolio">
        <h2>Our Work</h2>
        <div class="portfolio-grid">
          <div class="portfolio-item" v-for="n in 6" :key="n">
            <img :src="`https://placehold.co/400x300?text=Project+${n}`" :alt="`Project ${n}`" />
            <div class="portfolio-overlay">
              <h3>Project {{ n }}</h3>
              <p>Lorem ipsum dolor sit amet</p>
              <a href="#" class="view-project">View Project</a>
            </div>
          </div>
        </div>
      </section>

      <section id="testimonials" class="testimonials">
        <h2>What Our Clients Say</h2>
        <div class="testimonials-grid">
          <div v-for="testimonial in testimonials" :key="testimonial.name" class="testimonial-card">
            <img :src="testimonial.image" :alt="testimonial.name" class="testimonial-image" />
            <div class="testimonial-content">
              <p>"{{ testimonial.content }}"</p>
              <h4>{{ testimonial.name }}</h4>
              <p class="role">{{ testimonial.role }}</p>
            </div>
          </div>
        </div>
      </section>

      <section id="contact" class="contact">
        <h2>Get in Touch</h2>
        <div class="contact-container">
          <div class="contact-info">
            <h3>Contact Information</h3>
            <p>📍 123 Innovation Street, Tech City, TC 12345</p>
            <p>📞 (555) 123-4567</p>
            <p>✉️ info@innovatetech.com</p>
          </div>
          <form class="contact-form">
            <div class="form-group">
              <input type="text" placeholder="Your Name" />
            </div>
            <div class="form-group">
              <input type="email" placeholder="Your Email" />
            </div>
            <div class="form-group">
              <textarea placeholder="Your Message" rows="5"></textarea>
            </div>
            <button type="submit" class="cta-button primary">Send Message</button>
          </form>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div class="footer-content">
        <div class="footer-section">
          <h3>InnovateTech</h3>
          <p>Transforming ideas into digital reality.</p>
        </div>
        <div class="footer-section">
          <h4>Quick Links</h4>
          <a href="#home">Home</a>
          <a href="#about">About</a>
          <a href="#services">Services</a>
          <a href="#portfolio">Portfolio</a>
        </div>
        <div class="footer-section">
          <h4>Connect</h4>
          <a href="#">Twitter</a>
          <a href="#">LinkedIn</a>
          <a href="#">Facebook</a>
          <a href="#">Instagram</a>
        </div>
        <div class="footer-section">
          <h4>Newsletter</h4>
          <div class="newsletter-form">
            <input type="email" placeholder="Enter your email" />
            <button class="cta-button secondary">Subscribe</button>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 InnovateTech. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.app-container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.header {
  background-color: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
}

.nav {
  max-width: 1400px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.8rem;
  font-weight: bold;
  background: linear-gradient(135deg, #646cff 0%, #42b883 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.nav-links {
  display: flex;
  gap: 2rem;
}

.nav-links a {
  color: #333;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
  padding: 0.5rem 1rem;
  border-radius: 20px;
}

.nav-links a:hover {
  color: #646cff;
  background-color: rgba(100, 108, 255, 0.1);
}

.main {
  margin-top: 4rem;
  flex: 1;
}

.hero {
  background: linear-gradient(135deg, #646cff 0%, #42b883 100%);
  color: white;
  padding: 8rem 2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 4rem;
  min-height: 90vh;
}

.hero-content {
  flex: 1;
  max-width: 600px;
}

.hero h1 {
  font-size: 4rem;
  margin-bottom: 1.5rem;
  line-height: 1.2;
}

.subtitle {
  font-size: 1.3rem;
  margin-bottom: 2.5rem;
  opacity: 0.9;
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.cta-button {
  padding: 1rem 2rem;
  font-size: 1.1rem;
  border-radius: 30px;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 600;
}

.cta-button.primary {
  background-color: white;
  color: #646cff;
  border: none;
}

.cta-button.secondary {
  background-color: transparent;
  color: white;
  border: 2px solid white;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.hero-image {
  flex: 1;
  max-width: 600px;
}

.hero-image img {
  width: 100%;
  height: auto;
  border-radius: 20px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);
}

.about, .services, .portfolio, .testimonials, .contact {
  padding: 6rem 2rem;
  max-width: 1400px;
  margin: 0 auto;
}

h2 {
  font-size: 2.5rem;
  text-align: center;
  margin-bottom: 3rem;
  color: #333;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.about-text p {
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
  line-height: 1.8;
  color: #666;
}

.stats-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}

.stat-card {
  background: white;
  padding: 2rem;
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-5px);
}

.stat-card h3 {
  font-size: 2.5rem;
  color: #646cff;
  margin-bottom: 0.5rem;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
}

.service-card {
  background: white;
  padding: 2.5rem;
  border-radius: 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-align: center;
}

.service-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.service-card h3 {
  color: #333;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.service-card p {
  color: #666;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.learn-more {
  color: #646cff;
  text-decoration: none;
  font-weight: 600;
  transition: color 0.3s ease;
}

.learn-more:hover {
  color: #42b883;
}

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.portfolio-item {
  position: relative;
  border-radius: 15px;
  overflow: hidden;
}

.portfolio-item img {
  width: 100%;
  height: 300px;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.portfolio-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(100, 108, 255, 0.9);
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: opacity 0.3s ease;
  padding: 2rem;
  text-align: center;
}

.portfolio-item:hover .portfolio-overlay {
  opacity: 1;
}

.portfolio-item:hover img {
  transform: scale(1.1);
}

.view-project {
  color: white;
  text-decoration: none;
  padding: 0.8rem 1.5rem;
  border: 2px solid white;
  border-radius: 25px;
  margin-top: 1rem;
  transition: all 0.3s ease;
}

.view-project:hover {
  background: white;
  color: #646cff;
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.testimonial-card {
  background: white;
  padding: 2rem;
  border-radius: 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.testimonial-image {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 1.5rem;
}

.testimonial-content p {
  font-style: italic;
  color: #666;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.testimonial-content h4 {
  color: #333;
  margin-bottom: 0.5rem;
}

.role {
  color: #646cff;
  font-size: 0.9rem;
}

.contact-container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 4rem;
  background: white;
  padding: 3rem;
  border-radius: 20px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.contact-info h3 {
  color: #333;
  margin-bottom: 2rem;
  font-size: 1.5rem;
}

.contact-info p {
  margin-bottom: 1rem;
  color: #666;
}

.contact-form {
  display: grid;
  gap: 1.5rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 1rem;
  border: 1px solid #ddd;
  border-radius: 10px;
  font-size: 1rem;
}

.form-group textarea {
  resize: vertical;
}

.footer {
  background-color: #1a1a1a;
  color: white;
  padding: 4rem 2rem 2rem;
  margin-top: 4rem;
}

.footer-content {
  max-width: 1400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-section h3,
.footer-section h4 {
  margin-bottom: 1.5rem;
  color: white;
}

.footer-section a {
  color: #999;
  text-decoration: none;
  display: block;
  margin-bottom: 0.8rem;
  transition: color 0.3s ease;
}

.footer-section a:hover {
  color: white;
}

.newsletter-form {
  display: flex;
  gap: 1rem;
}

.newsletter-form input {
  flex: 1;
  padding: 0.8rem;
  border: none;
  border-radius: 5px;
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

@media (max-width: 1024px) {
  .hero {
    flex-direction: column;
    text-align: center;
    padding: 6rem 2rem;
  }

  .hero-content {
    max-width: 100%;
  }

  .hero-buttons {
    justify-content: center;
  }

  .about-content {
    grid-template-columns: 1fr;
  }

  .contact-container {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .nav {
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
  }

  .nav-links {
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
  }

  .hero h1 {
    font-size: 2.5rem;
  }

  .stats-grid {
    grid-template-columns: 1fr;
  }

  .newsletter-form {
    flex-direction: column;
  }
}
</style>