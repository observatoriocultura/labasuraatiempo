<script setup>
const baseUrl = import.meta.env.BASE_URL
</script>

<template>
  <main class="app-view">
    <!-- Hero Section -->
    <header class="hero">
      <div class="hero-content">
        <img :src="`${baseUrl}images/bogota-sobre-rojo.png`" alt="Bogotá" class="hero-logo" />
        <h1 class="hero-title">La Basura a Tiempo</h1>
      </div>
    </header>

    <!-- Intro Section -->
    <section class="intro-section">
      <p class="intro-text">
        <b>Sabemos que te importa Bogotá</b>
        <br>
        Por eso si quieres que la ciudad esté limpia y agradable, saca la basura en el momento en que inicia la franja de recolección y en el día correcto.
      </p>
    </section>

    <!-- Chatico Section -->
    <section class="chatico-compact">
      <div class="chatico-avatar">
        <a href="https://wa.me/573160231524?text=%C2%BFCu%C3%A1ndo+recogen+la+basura+en+mi+casa%3F" target="_blank">
          <img :src="`${baseUrl}images/chatico.jpg`" alt="Chatico Logo" />
        </a>
      </div>
      <div class="chatico-info">
        <p>¿No sabes cuándo pasa el camión? Escríbele a Chatico al número <strong>3160231524</strong> o busca en <a href="https://www.labasuraatiempo.com" target="_blank">www.labasuraatiempo.com</a> y consulta el horario de recolección en tu barrio.</p>
        <a href="https://wa.me/573160231524?text=%C2%BFCu%C3%A1ndo+recogen+la+basura+en+mi+casa%3F" target="_blank" class="btn btn-whatsapp">¡Hablar con Chatico!</a>
      </div>
    </section>

    <!-- Tips Section -->
    <section class="tips-section">
      <div class="tips-list">
        <div class="tip-card">
          <div class="tip-content">
            <h3>Consulta el horario de recolección en tu barrio</h3>
            <p>Ingresa tu ubicación y conoce el día y la hora exacta para sacar la basura correctamente.</p>
          </div>
        </div>

        <div class="tip-card">
          <div class="tip-content">
            <h3>Saca la basura en el momento adecuado</h3>
            <p>Evita dejar residuos en la calle antes de tiempo y contribuye a mantener tu barrio limpio.</p>
          </div>
        </div>

        <div class="tip-card">
          <div class="tip-content">
            <h3>Activa recordatorios y no lo olvides</h3>
            <p>Recibe alertas para sacar la basura justo cuando pasa el camión de recolección.</p>
          </div>
        </div>
      </div>
    </section>

  </main>
</template>

<style scoped>
.app-view {
  max-width: 600px;
  margin: 0 auto;
  min-height: 100vh;
  padding-bottom: 20px;
}

/* Hero Section */
.hero {
  padding: 40px 24px 30px;
  text-align: center;
  background-color: var(--primary);
  color: white;
}

.hero-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.hero-logo {
  height: 70px;
  width: auto;
  object-fit: contain;
}

.hero-title {
  color: white;
  text-transform: uppercase;
  font-weight: 800;
  font-size: 2.4rem;
  line-height: 1.1;
  letter-spacing: -1px;
  text-align: right;
  flex: 1;
}

/* Intro Section */
.intro-section {
  padding: 30px 24px 10px;
  background-color: transparent;
  text-align: center;
}

.intro-text {
  font-size: 1.1rem;
  color: var(--text);
  max-width: 500px;
  line-height: 1.4;
  margin: 0 auto;
}

/* Chatico Compact with Avatar */
.chatico-compact {
  padding: 20px 20px;
  background: var(--background);
  border-radius: 20px;
  margin: 0 16px;
  display: flex;
  gap: 16px;
  align-items: center;
}

.chatico-avatar {
  flex-shrink: 0;
}

.chatico-avatar img {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid white;
  box-shadow: 0 4px 10px rgba(0,0,0,0.08);
}

.chatico-compact h3 {
  font-size: 1.4rem;
  color: var(--text);
  margin-bottom: 4px;
}

.chatico-compact p {
  color: var(--text-muted);
  margin-bottom: 12px;
  font-size: 0.95rem;
  line-height: 1.3;
}

/* Tips Section Simplified */
.tips-section {
  padding: 24px 24px 10px;
}

.section-title {
  font-size: 1.6rem;
  margin-bottom: 20px;
  color: var(--primary);
  text-align: center;
}

.tips-list {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.tip-card {
  display: flex;
  background: transparent;
  padding: 16px 0;
  align-items: flex-start;
  border-bottom: 1px solid rgba(0,0,0,0.06);
}

.tip-card:last-child {
  border-bottom: none;
}

.tip-content {
  width: 100%;
}

.tip-content h3 {
  font-size: 1.15rem;
  font-weight: bold;
  margin-bottom: 6px;
  color: var(--primary);
  line-height: 1.3;
}

.tip-content p {
  font-size: 0.9rem;
  color: var(--text-muted);
  line-height: 1.4;
}

/* Buttons */
.btn {
  display: inline-block;
  padding: 12px 24px;
  border-radius: 10px;
  text-decoration: none;
  font-weight: 700;
  font-size: 0.95rem;
  color: white;
  transition: all 0.2s;
}

.btn-whatsapp {
  background: #21C063;
  box-shadow: 0 6px 14px rgba(33, 192, 99, 0.2);
}

.btn-whatsapp:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(33, 192, 99, 0.3);
}

@media (max-width: 768px) {
  .hero {
    padding: 20px 20px 10px;
  }

  .intro-text {
    font-size: 0.95rem;
  }

  .hero-logo {
    height: 50px;
  }

  .hero-title {
    font-size: 1.8rem;
    margin-bottom: 0;
  }

  .chatico-compact {
    margin-top: 0;
    padding: 16px;
    flex-direction: column;
    text-align: center;
    gap: 12px;
  }

  .chatico-avatar img {
    width: 60px;
    height: 60px;
  }

  .chatico-compact h3 {
    font-size: 1.2rem;
  }

  .tips-section {
    padding: 16px 20px;
  }

  .section-title {
    font-size: 1.4rem;
    margin-bottom: 16px;
  }
}
</style>
