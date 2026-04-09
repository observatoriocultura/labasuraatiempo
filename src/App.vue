<script setup>
const baseUrl = import.meta.env.BASE_URL

const trackChaticoClick = () => {
  if (window.gtag) {
    window.gtag('event', 'click_chatico', {
      'event_category': 'engagement',
      'event_label': 'WhatsApp Chatico'
    });
  }
}
</script>

<template>
  <main class="app-view">
    <!-- Image Reference Hero Section -->
    <header class="hero-reference">
      <div class="hero-overlay"></div>
      <div class="hero-branding">
        <a href="https://www.bogota.gov.co/" target="_blank">
          <img :src="`${baseUrl}images/bogota-sobre-rojo.png`" alt="Bogotá" class="hero-logo" />
        </a>
      </div>
      <div class="hero-container">
        <div class="hero-text-content">
          <h2 class="hero-question">¿Sabes qué <span class="white-text">días hay</span></h2>
          <h1 class="hero-main-title">RECOLECCIÓN<br>DE BASURAS</h1>
          <h2 class="hero-subtitle">en tu zona?</h2>
        </div>
      </div>
    </header>

    <!-- Intro Section -->
    <section class="intro-section">
      <div class="card content-narrow">
        <p class="intro-text">
          <strong class="highlight">Sabemos que te importa Bogotá.</strong><br>
          Si quieres que la ciudad esté limpia y agradable, saca la basura en el momento en que inicia la franja de recolección y en el día correcto.
        </p>
      </div>
    </section>

    <!-- Chatico Section -->
    <section class="chatico-section">
      <div class="chatico-card content-narrow">
        <div class="chatico-header">
          <div class="chatico-avatar">
            <a 
              href="https://wa.me/573160231524?text=%C2%BFCu%C3%A1ndo+recogen+la+basura+en+mi+casa%3F" 
              target="_blank"
              @click="trackChaticoClick"
            >
              <img :src="`${baseUrl}images/chatico.jpg`" alt="Chatico Logo" />
            </a>
          </div>
          <div class="chatico-title">
            <h3>¿No sabes cuándo pasa el camión?</h3>
          </div>
        </div>
        <div class="chatico-body">
          <p>Escríbele a <strong>Chatico</strong> al número <strong>3160231524</strong> o consulta en el portal oficial.</p>
          <div class="chatico-actions">
            <a 
              href="https://wa.me/573160231524?text=%C2%BFCu%C3%A1ndo+recogen+la+basura+en+mi+casa%3F" 
              target="_blank" 
              class="btn btn-primary" 
              id="btn-wa-chatico"
              @click="trackChaticoClick"
            >
              ¡Hablar con Chatico!
            </a>
            <a href="https://bogota.gov.co/mi-ciudad/habitat/consulta-de-dias-y-horarios-de-recoleccion-de-basura-en-bogota" target="_blank" class="btn btn-outline">
              Consultar días y horarios
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Tips Section -->
    <section class="tips-section">
      <div class="tips-grid content-narrow">
        <div class="tip-card">
          <div class="tip-icon">📍</div>
          <div class="tip-content">
            <h3>Consulta tu horario</h3>
            <p>Conoce el día y la hora exacta para sacar la basura en tu barrio.</p>
          </div>
        </div>

        <div class="tip-card">
          <div class="tip-icon">⏰</div>
          <div class="tip-content">
            <h3>Saca a tiempo</h3>
            <p>Evita dejar residuos en la calle antes de tiempo. Contribuye al orden.</p>
          </div>
        </div>

        <div class="tip-card">
          <div class="tip-icon">🔔</div>
          <div class="tip-content">
            <h3>Activa recordatorios</h3>
            <p>Recibe alertas para no olvidar el horario de recolección.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Map Section -->
    <section class="map-section">
      <div class="section-header">
        <h2 class="section-title">Mapa de recolección</h2>
        <p>Consulta geográficamente las zonas y horarios de aseo en la ciudad.</p>
      </div>
      <div class="map-container">
        <iframe class="BtaAseoIframe-block-map" frameborder="0" scrolling="no" allowfullscreen="" src="https://mapas.bogota.gov.co/?&amp;e=-74.28869889699816,4.582225178134931,-73.99035142385402,4.725945244826054,4686&amp;b=7256&amp;show_menu=true&amp;show_list=true&amp;open_menu=true&amp;show_search=true&amp;show_legend=false"></iframe>
      </div>
    </section>

    <footer class="app-footer">
      <p>2026 &middot; La Basura a Tiempo &middot; Bogotá</p>
    </footer>
  </main>
</template>

<style scoped>
.app-view {
  max-width: 1200px;
  margin: 0 auto;
  min-height: 100vh;
  background: transparent;
  color: white;
}

/* Hero Section Reference Style */
.hero-reference {
  position: relative;
  height: 350px;
  background-image: url('/images/residuos-2.jpg');
  background-size: cover;
  background-position: center left;
  display: flex;
  align-items: center;
  overflow: hidden;
  border-bottom: 4px solid var(--primary);
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, rgba(17, 30, 27, 0.2) 0%, rgba(17, 30, 27, 0.7) 50%, rgba(17, 30, 27, 0.95) 100%);
}

.hero-container {
  position: relative;
  z-index: 2;
  width: 100%;
  padding: 0 40px;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  text-align: right;
}

.hero-branding {
  position: absolute;
  top: 10px;
  left: 10px;
  z-index: 5;
}

.hero-logo {
  height: 50px;
  filter: drop-shadow(0 2px 4px rgba(0,0,0,0.5));
}

.hero-text-content {
  max-width: 500px;
}

.hero-question {
  color: var(--primary);
  font-size: 2.2rem;
  font-weight: 700;
  margin-bottom: -5px;
  text-transform: none;
}

.white-text {
  color: white;
}

.hero-main-title {
  color: var(--primary);
  font-size: 3.2rem;
  line-height: 0.85;
  margin: 15px 0;
  font-weight: 900;
  letter-spacing: -2px;
}

.hero-subtitle {
  color: white;
  font-size: 2.8rem;
  font-weight: 700;
  margin-top: -5px;
  text-transform: none;
}

/* Utilities */
.content-narrow {
  max-width: 900px;
  margin: 0 auto;
}

/* Sections */
.intro-section {
  padding: 40px 20px;
}

.card {
  background: var(--card-bg);
  padding: 30px;
  border-radius: 24px;
  border: 1px solid rgba(184, 217, 53, 0.1);
  backdrop-filter: blur(10px);
}

.intro-text {
  font-size: 1.25rem;
  line-height: 1.6;
  color: #e0e0e0;
}

.highlight {
  color: var(--primary);
  font-size: 1.4rem;
}

/* Chatico Section */
.chatico-section {
  padding: 0 20px 40px;
}

.chatico-card {
  background: rgba(255, 255, 255, 0.03);
  border-radius: 30px;
  padding: 30px;
  border: 1px dashed rgba(255, 255, 255, 0.1);
}

.chatico-header {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 20px;
}

.chatico-avatar img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 4px solid var(--primary);
  box-shadow: 0 8px 24px rgba(184, 217, 53, 0.2);
}

.chatico-title h3 {
  font-size: 1.5rem;
  color: white;
  text-transform: none;
}

.chatico-body p {
  font-size: 1.1rem;
  color: var(--text-muted);
  margin-bottom: 24px;
}

.chatico-actions {
  display: flex;
  gap: 16px;
}

/* Tips Section */
.tips-section {
  padding: 0 20px 60px;
}

.tips-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
}

.tip-card {
  background: var(--card-bg);
  padding: 24px;
  border-radius: 20px;
  transition: all 0.3s ease;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.tip-card:hover {
  transform: translateY(-5px);
  background: rgba(255, 255, 255, 0.07);
  border-color: var(--primary);
}

.tip-icon {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.tip-card h3 {
  font-size: 1.2rem;
  color: var(--primary);
  margin-bottom: 10px;
  text-transform: none;
}

.tip-card p {
  font-size: 0.95rem;
  color: var(--text-muted);
  line-height: 1.4;
}

/* Buttons */
.btn {
  padding: 14px 28px;
  border-radius: 14px;
  font-weight: 700;
  text-decoration: none;
  font-size: 1rem;
  transition: all 0.3s ease;
  display: inline-block;
  text-align: center;
}

.btn-primary {
  background: var(--primary);
  color: #111e1b;
}

.btn-primary:hover {
  filter: brightness(1.1);
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(184, 217, 53, 0.2);
}

.btn-outline {
  border: 2px solid rgba(255, 255, 255, 0.2);
  color: white;
}

.btn-outline:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: white;
}

.app-footer {
  text-align: center;
  padding: 40px;
  color: var(--text-muted);
  font-size: 0.9rem;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

/* Map Section */
.map-section {
  padding: 0 20px 60px;
}

.section-header {
  text-align: center;
  margin-bottom: 30px;
}

.section-title {
  color: var(--primary);
  font-size: 1.8rem;
  margin-bottom: 10px;
}

.map-container {
  width: 100%;
  height: 600px;
  border-radius: 24px;
  overflow: hidden;
  border: 1px solid rgba(184, 217, 53, 0.2);
  box-shadow: 0 20px 40px rgba(0,0,0,0.3);
  background: #000;
}

.BtaAseoIframe-block-map {
  width: 100%;
  height: 100%;
}

@media (max-width: 600px) {
  .hero-reference {
    height: 380px;
    background-position: center center;
  }

  .hero-overlay {
    background: linear-gradient(0deg, rgba(17, 30, 27, 0.95) 0%, rgba(17, 30, 27, 0.6) 100%);
  }

  .hero-container {
    padding: 0 24px;
    align-items: center;
    text-align: center;
    margin-top: 60px;
  }

  .hero-question {
    font-size: 1.4rem;
  }

  .hero-main-title {
    font-size: 2.6rem;
  }

  .hero-subtitle {
    font-size: 1.9rem;
  }

  .chatico-header {
    flex-direction: column;
    text-align: center;
  }

  .chatico-actions {
    flex-direction: column;
  }
  
  .hero-branding {
    top: 20px;
    left: 20px;
    transform: none;
  }

  .map-container {
    height: 450px;
  }
}
</style>
