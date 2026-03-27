<script setup>
</script>

<template>
  <main class="app-view">
    <!-- Hero Section -->
    <header class="hero">
      <div class="hero-content">
        <h1 class="hero-title">La Basura a Tiempo</h1>
        <p class="hero-subtitle">¡Que el camión no te deje la basura! Saca tus bolsas justo a tiempo para mantener nuestras calles impecables y hermosas.</p>
      </div>
    </header>

    <!-- Chatico Section -->
    <section class="chatico-compact">
      <div class="chatico-avatar">
        <img src="/images/chatico.jpg" alt="Chatico Logo" />
      </div>
      <div class="chatico-info">
        <p>Escríbeme por WhatsApp para conocer ahora mismo los horarios de recolección de basura en tu barrio. ¡Saca tu bolsa justo a tiempo!</p>
        <a href="https://wa.me/573160231524?text=%C2%BFCu%C3%A1ndo+recogen+la+basura+en+mi+casa%3F" target="_blank" class="btn btn-primary">¡Hablar con Chatico!</a>
      </div>
    </section>

    <!-- Tips Section -->
    <section class="tips-section">
      <h2 class="section-title">¡Únete al equipo!</h2>
      <div class="tips-list">
        <div class="tip-item">
          <span class="tip-dot"></span>
          <div class="tip-text">
            <h4>Sincroniza tu bolsa 🕒</h4>
            <p>Saca la basura <strong>solo minutos antes</strong> de que pase el camión. ¡Evitemos que la calle se vea desordenada!</p>
          </div>
        </div>
        <div class="tip-item">
          <span class="tip-dot"></span>
          <div class="tip-text">
            <h4>¡Calle limpia, ciudad feliz! ✨</h4>
            <p>Si todos sacamos la basura a tiempo, evitamos malos olores y mantenemos las aceras despejadas para caminar.</p>
          </div>
        </div>
        <div class="tip-item">
          <span class="tip-dot"></span>
          <div class="tip-text">
            <h4>Separa con amor ♻️</h4>
            <p>Recuerda: bolsa blanca para lo que se recicla y negra para lo demás. ¡El planeta te lo agradece!</p>
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
  padding-bottom: 40px;
}

/* Hero Section */
.hero {
  padding: 80px 24px 60px;
  background: white;
  text-align: left;
}

.hero-title {
  color: var(--primary);
  font-size: 4rem;
  line-height: 0.9;
  margin-bottom: 24px;
  letter-spacing: -2px;
}

.hero-subtitle {
  font-size: 1.4rem;
  color: var(--text-muted);
  max-width: 500px;
  line-height: 1.4;
}

/* Chatico Compact with Avatar */
.chatico-compact {
  padding: 40px 24px;
  background: var(--background);
  border-radius: 32px;
  margin: 0 16px;
  display: flex;
  gap: 24px;
  align-items: center;
}

.chatico-avatar {
  flex-shrink: 0;
}

.chatico-avatar img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid white;
  box-shadow: 0 8px 16px rgba(0,0,0,0.08);
}

.chatico-compact h3 {
  font-size: 2rem;
  color: var(--text);
  margin-bottom: 8px;
}

.chatico-compact p {
  color: var(--text-muted);
  margin-bottom: 20px;
  font-size: 1rem;
  line-height: 1.4;
}

/* Tips Section Simplified */
.tips-section {
  padding: 80px 24px;
}

.section-title {
  font-size: 2.2rem;
  margin-bottom: 40px;
  color: var(--primary);
}

.tips-list {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.tip-item {
  display: flex;
  gap: 20px;
  align-items: flex-start;
}

.tip-dot {
  width: 14px;
  height: 14px;
  background: var(--secondary);
  border-radius: 4px;
  margin-top: 8px;
  flex-shrink: 0;
  transform: rotate(45deg);
}

.tip-text h4 {
  font-size: 1.4rem;
  margin-bottom: 8px;
  font-weight: 500;
}

.tip-text p {
  font-size: 1.1rem;
  color: var(--text-muted);
  line-height: 1.5;
}

/* Buttons */
.btn {
  display: inline-block;
  padding: 16px 30px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 700;
  font-size: 1rem;
  background: var(--primary);
  color: white;
  box-shadow: 0 10px 20px rgba(0, 138, 14, 0.15);
  transition: all 0.2s;
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 15px 25px rgba(0, 138, 14, 0.25);
}

@media (max-width: 768px) {
  .hero {
    padding: 60px 24px 20px;
  }

  .hero-subtitle {
     display: none;
  }

  .hero-title {
    font-size: 3rem;
    margin-bottom: 0;
  }

  .chatico-compact {
    margin-top: 0;
    padding: 30px 20px;
    flex-direction: column;
    text-align: center;
    gap: 16px;
  }

  .chatico-avatar img {
    width: 80px;
    height: 80px;
  }

  .chatico-compact h3 {
    font-size: 1.6rem;
  }

  .tips-section {
    padding: 40px 24px;
  }

  .section-title {
    font-size: 1.8rem;
    margin-bottom: 30px;
  }
}
</style>
